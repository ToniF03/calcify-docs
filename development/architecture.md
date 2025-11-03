# Architecture Overview

Technical overview of Calcify's architecture and design.

## High-Level Architecture

```
┌─────────────────────────────────────────────────┐
│              User Interface (XAML)              │
│         MainWindow, Settings, Dialogs           │
└──────────────────┬──────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────┐
│           Presentation Layer (WPF)              │
│       Event Handlers, Data Binding, MVVM        │
└──────────────────┬──────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────┐
│            Business Logic Layer                 │
│    Calculation Engine, Parser, Evaluator        │
└──────────────────┬──────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────┐
│              Utility Classes                    │
│   Math, Unit Conversion, Currency, Date/Time    │
└──────────────────┬──────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────┐
│            External Services                    │
│   File I/O, Network (Exchange Rates), Registry  │
└─────────────────────────────────────────────────┘
```

## Technology Stack

### Core Technologies

- **Framework:** .NET Framework 4.5.2+
- **UI Framework:** WPF (Windows Presentation Foundation)
- **Language:** C# 7.0+
- **IDE:** Visual Studio 2019+

### NuGet Packages

| Package | Version | Purpose |
|---------|---------|---------|
| AvalonEdit | 6.1.3.50 | Text editor component |
| Newtonsoft.Json | 13.0.1 | JSON parsing |
| Microsoft.UI.Xaml | 2.7.0 | Modern UI controls |

## Project Structure

### Main Application (`Calcify/`)

```
Calcify/
├── App.xaml                    # Application definition
├── App.xaml.cs                 # Application startup logic
├── MainWindow.xaml             # Main window UI
├── MainWindow.xaml.cs          # Main window code-behind
├── DialogWindow.xaml           # Dialog windows
├── Settings.xaml               # Settings window
├── About.xaml                  # About dialog
│
├── Classes/                    # Core classes
│   ├── Math.cs                 # Math functions
│   ├── RegistryWatcher.cs      # Registry monitoring
│   └── SyntaxFile.cs           # Syntax highlighting
│
├── Resources/                  # Assets
│   ├── Icons/                  # Application icons
│   └── Fonts/                  # Custom fonts
│
└── Properties/                 # Project properties
    ├── AssemblyInfo.cs         # Assembly metadata
    ├── Resources.resx          # Embedded resources
    └── Settings.settings       # User settings
```

### Update Project (`Update/`)

Separate project for auto-update functionality:

```
Update/
├── MainWindow.xaml             # Update UI
├── MainWindow.xaml.cs          # Update logic
└── App.xaml                    # Updater app
```

### Setup Project (`setup/`)

WiX installer project for creating MSI packages.

## Key Components

### 1. Text Editor (AvalonEdit)

**File:** `MainWindow.xaml`

**Purpose:** Provides the main text editing area

**Features:**
- Syntax highlighting
- Line numbering
- Code folding
- Auto-completion
- Undo/redo

**Integration:**
```csharp
// TextEditor from AvalonEdit
<avalonedit:TextEditor 
    Name="textEditor"
    FontFamily="Consolas"
    FontSize="12"
    ShowLineNumbers="True"
    WordWrap="True" />
```

---

### 2. Calculation Engine

**File:** `Classes/Math.cs`

**Purpose:** Parse and evaluate mathematical expressions

**Components:**

**Parser:**
- Tokenizes input string
- Builds expression tree
- Handles operator precedence
- Resolves variables

**Evaluator:**
- Traverses expression tree
- Computes results
- Handles functions
- Manages units/conversions

**Flow:**
```
Input String → Tokenizer → Parser → Expression Tree → Evaluator → Result
```

**Example:**
```csharp
public static double Evaluate(string expression)
{
    // 1. Tokenize
    var tokens = Tokenize(expression);
    
    // 2. Parse
    var tree = Parse(tokens);
    
    // 3. Evaluate
    return Evaluate(tree);
}
```

---

### 3. Unit Conversion System

**File:** `Classes/Math.cs`

**Purpose:** Handle unit conversions

**Design Pattern:** Dictionary-based lookup

**Structure:**
```csharp
// Unit definitions
Dictionary<string, double> unitConversions = new Dictionary<string, double>
{
    // Length
    { "km_to_m", 1000 },
    { "m_to_km", 0.001 },
    { "mi_to_km", 1.60934 },
    // ... more conversions
};

// Conversion method
public static double Convert(double value, string fromUnit, string toUnit)
{
    string key = $"{fromUnit}_to_{toUnit}";
    if (unitConversions.ContainsKey(key))
    {
        return value * unitConversions[key];
    }
    // Handle reverse or chained conversions
}
```

---

### 4. Currency Converter

**File:** `MainWindow.xaml.cs`

**Purpose:** Real-time exchange rate conversion

**API:** Frankfurter API (`https://api.frankfurter.app`)

**Caching Strategy:**
- Fetch on startup
- Cache for configured interval (default: 3 hours)
- Fallback to cached rates if offline

**Implementation:**
```csharp
private async Task<Dictionary<string, double>> FetchExchangeRates()
{
    using (var client = new HttpClient())
    {
        string json = await client.GetStringAsync(
            "https://api.frankfurter.app/latest");
        
        var rates = JsonConvert.DeserializeObject<ExchangeRates>(json);
        
        // Cache rates
        SaveRatesToCache(rates);
        
        return rates.Rates;
    }
}
```

---

### 5. Syntax Highlighting

**File:** `Classes/SyntaxFile.cs`

**Purpose:** Color-code syntax in editor

**Based on:** AvalonEdit's highlighting system

**Configuration:**
```xml
<SyntaxDefinition name="Calcify">
  <RuleSet>
    <!-- Numbers -->
    <Rule color="Number">
      \b\d+(\.\d+)?\b
    </Rule>
    
    <!-- Operators -->
    <Rule color="Operator">
      [+\-*/^%]
    </Rule>
    
    <!-- Functions -->
    <Rule color="Function">
      \b(sin|cos|tan|sqrt|log)\b
    </Rule>
    
    <!-- Comments -->
    <Rule color="Comment">
      //.*$
    </Rule>
  </RuleSet>
</SyntaxDefinition>
```

---

### 6. Settings Management

**File:** `Properties/Settings.settings`

**Purpose:** Persist user preferences

**Storage:** Application data folder
- Path: `%APPDATA%\Calcify\settings.json`

**Access:**
```csharp
// Read setting
string theme = Properties.Settings.Default.Theme;

// Write setting
Properties.Settings.Default.Theme = "Dark";
Properties.Settings.Default.Save();
```

---

### 7. Registry Watcher

**File:** `Classes/RegistryWatcher.cs`

**Purpose:** Monitor registry changes (file associations)

**Pattern:** Polling-based watcher

**Usage:**
```csharp
var watcher = new RegistryWatcher(@"HKEY_CLASSES_ROOT\.calc");
watcher.ValueChanged += (s, e) => {
    // Handle registry change
};
watcher.Start();
```

---

## Design Patterns

### MVVM (Model-View-ViewModel)

**View:** XAML files (`MainWindow.xaml`)
**ViewModel:** Code-behind (`MainWindow.xaml.cs`)
**Model:** Data classes (`Math.cs`, etc.)

**Data Binding:**
```xml
<TextBlock Text="{Binding ResultText}" />
```

```csharp
public string ResultText
{
    get => _resultText;
    set
    {
        _resultText = value;
        OnPropertyChanged(nameof(ResultText));
    }
}
```

---

### Singleton Pattern

Used for global state management:

```csharp
public class SettingsManager
{
    private static SettingsManager _instance;
    
    public static SettingsManager Instance
    {
        get
        {
            if (_instance == null)
                _instance = new SettingsManager();
            return _instance;
        }
    }
    
    private SettingsManager() { }
}
```

---

### Strategy Pattern

For different calculation strategies:

```csharp
interface ICalculationStrategy
{
    double Calculate(double a, double b);
}

class AddStrategy : ICalculationStrategy
{
    public double Calculate(double a, double b) => a + b;
}

class MultiplyStrategy : ICalculationStrategy
{
    public double Calculate(double a, double b) => a * b;
}
```

---

## Data Flow

### User Input to Result

1. **User types** in AvalonEdit text editor
2. **TextChanged event** fires
3. **Parser** tokenizes input
4. **Evaluator** computes result
5. **Result displayed** in UI (inline or status bar)

### Calculation Pipeline

```
Input: "10 km to miles"
  ↓
Tokenizer: ["10", "km", "to", "miles"]
  ↓
Parser: {value: 10, fromUnit: "km", toUnit: "miles"}
  ↓
Unit Converter: 10 * 0.621371 = 6.21371
  ↓
Formatter: "6.21 miles"
  ↓
Output: Display to user
```

## Threading Model

### UI Thread
- Handles all UI updates
- User interactions
- Event handlers

### Background Threads
- Currency rate fetching
- File operations
- Auto-save

**Example:**
```csharp
await Task.Run(() =>
{
    // Background work
    var result = CalculateComplex();
    
    // Update UI on UI thread
    Dispatcher.Invoke(() =>
    {
        ResultText = result.ToString();
    });
});
```

## Error Handling

### Strategy
1. **Try-Catch blocks** for expected errors
2. **Validation** before operations
3. **User-friendly messages**
4. **Logging** for debugging

### Example:
```csharp
try
{
    result = Evaluate(expression);
}
catch (DivideByZeroException)
{
    ShowError("Cannot divide by zero");
}
catch (FormatException)
{
    ShowError("Invalid number format");
}
catch (Exception ex)
{
    Log.Error(ex);
    ShowError("Calculation error");
}
```

## Performance Considerations

### Optimizations

1. **Lazy Evaluation** - Compute only when needed
2. **Caching** - Store frequently used results
3. **Debouncing** - Delay calculations while typing
4. **Async Operations** - Non-blocking UI

### Example - Debounced Calculation:
```csharp
private DispatcherTimer _calculationTimer;

private void TextEditor_TextChanged(object sender, EventArgs e)
{
    _calculationTimer?.Stop();
    _calculationTimer = new DispatcherTimer
    {
        Interval = TimeSpan.FromMilliseconds(300)
    };
    _calculationTimer.Tick += (s, args) =>
    {
        Calculate();
        _calculationTimer.Stop();
    };
    _calculationTimer.Start();
}
```

## Security Considerations

### Input Validation
- Sanitize all user input
- Prevent code injection
- Limit expression complexity
- Timeout long calculations

### Network Security
- HTTPS for API calls
- Validate SSL certificates
- Handle network errors gracefully

---

**See Also:**
- [Building from Source](building.md)
- [API Reference](api-reference.md)
- [Contributing Guide](contributing.md)
