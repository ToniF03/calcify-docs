# API Reference

Code documentation for developers extending or integrating with Calcify.

## Namespaces

### Calcify
Main application namespace containing windows and application logic.

### Calcify.Classes
Utility classes for calculations, conversions, and system operations.

---

## Core Classes

### Math Class

Mathematical operations and expression evaluation.

**Namespace:** `Calcify.Classes`

#### Methods

##### Evaluate(string expression)
Evaluates a mathematical expression and returns the result.

**Signature:**
```csharp
public static double Evaluate(string expression)
```

**Parameters:**
- `expression` (string): Mathematical expression to evaluate

**Returns:** `double` - Calculated result

**Throws:**
- `FormatException` - Invalid expression format
- `DivideByZeroException` - Division by zero
- `OverflowException` - Result too large

**Example:**
```csharp
double result = Math.Evaluate("2 + 2");  // 4.0
double complex = Math.Evaluate("sin(30) * 100");  // 50.0
```

---

##### ConvertUnit(double value, string fromUnit, string toUnit)
Converts a value from one unit to another.

**Signature:**
```csharp
public static double ConvertUnit(double value, string fromUnit, string toUnit)
```

**Parameters:**
- `value` (double): Value to convert
- `fromUnit` (string): Source unit code (e.g., "km", "pounds")
- `toUnit` (string): Target unit code (e.g., "miles", "kg")

**Returns:** `double` - Converted value

**Throws:**
- `ArgumentException` - Unknown unit or incompatible units

**Example:**
```csharp
double miles = Math.ConvertUnit(10, "km", "miles");  // 6.21371
double kg = Math.ConvertUnit(150, "pounds", "kg");  // 68.0389
```

---

##### Sqrt(double x)
Calculates the square root.

**Signature:**
```csharp
public static double Sqrt(double x)
```

**Parameters:**
- `x` (double): Number to find square root of

**Returns:** `double` - Square root of x

**Throws:**
- `ArgumentException` - If x is negative

**Example:**
```csharp
double result = Math.Sqrt(16);  // 4.0
```

---

##### Sin(double angleDegrees)
Calculates sine of an angle in degrees.

**Signature:**
```csharp
public static double Sin(double angleDegrees)
```

**Parameters:**
- `angleDegrees` (double): Angle in degrees

**Returns:** `double` - Sine value

**Example:**
```csharp
double result = Math.Sin(30);  // 0.5
double result2 = Math.Sin(90);  // 1.0
```

---

##### Cos(double angleDegrees)
Calculates cosine of an angle in degrees.

**Signature:**
```csharp
public static double Cos(double angleDegrees)
```

**Parameters:**
- `angleDegrees` (double): Angle in degrees

**Returns:** `double` - Cosine value

**Example:**
```csharp
double result = Math.Cos(0);  // 1.0
double result2 = Math.Cos(60);  // 0.5
```

---

##### Log(double x, double base = 10)
Calculates logarithm of x with specified base.

**Signature:**
```csharp
public static double Log(double x, double base = 10)
```

**Parameters:**
- `x` (double): Number to find logarithm of
- `base` (double, optional): Logarithm base (default: 10)

**Returns:** `double` - Logarithm value

**Throws:**
- `ArgumentException` - If x ≤ 0

**Example:**
```csharp
double result = Math.Log(100);  // 2.0 (log base 10)
double result2 = Math.Log(8, 2);  // 3.0 (log base 2)
```

---

### RegistryWatcher Class

Monitors Windows Registry for changes.

**Namespace:** `Calcify.Classes`

#### Constructor

```csharp
public RegistryWatcher(string keyPath, int pollInterval = 1000)
```

**Parameters:**
- `keyPath` (string): Registry key path to monitor
- `pollInterval` (int, optional): Polling interval in milliseconds (default: 1000)

#### Methods

##### Start()
Starts monitoring the registry key.

**Signature:**
```csharp
public void Start()
```

**Example:**
```csharp
var watcher = new RegistryWatcher(@"HKEY_CLASSES_ROOT\.calc");
watcher.Start();
```

---

##### Stop()
Stops monitoring the registry key.

**Signature:**
```csharp
public void Stop()
```

---

#### Events

##### ValueChanged
Fired when the monitored registry value changes.

**Signature:**
```csharp
public event EventHandler ValueChanged
```

**Example:**
```csharp
watcher.ValueChanged += (sender, e) => {
    Console.WriteLine("Registry value changed!");
};
```

---

### SyntaxFile Class

Manages syntax highlighting definitions.

**Namespace:** `Calcify.Classes`

#### Methods

##### LoadSyntax(string filePath)
Loads syntax highlighting definition from file.

**Signature:**
```csharp
public static IHighlightingDefinition LoadSyntax(string filePath)
```

**Parameters:**
- `filePath` (string): Path to syntax definition file

**Returns:** `IHighlightingDefinition` - Highlighting definition

**Example:**
```csharp
var syntax = SyntaxFile.LoadSyntax("calcify.xshd");
textEditor.SyntaxHighlighting = syntax;
```

---

## Main Window

### MainWindow Class

Main application window.

**Namespace:** `Calcify`

**Base Class:** `Window`

#### Properties

##### TextEditor
Gets the main text editor control.

**Type:** `ICSharpCode.AvalonEdit.TextEditor`

**Access:** Read-only

**Example:**
```csharp
string text = MainWindow.TextEditor.Text;
```

---

##### CurrentFile
Gets or sets the currently open file path.

**Type:** `string`

**Access:** Read/Write

---

#### Methods

##### NewFile()
Creates a new blank file.

**Signature:**
```csharp
public void NewFile()
```

**Example:**
```csharp
mainWindow.NewFile();
```

---

##### OpenFile(string filePath)
Opens a file for editing.

**Signature:**
```csharp
public void OpenFile(string filePath)
```

**Parameters:**
- `filePath` (string): Path to file to open

**Example:**
```csharp
mainWindow.OpenFile(@"C:\calculations\myfile.calc");
```

---

##### SaveFile()
Saves the current file.

**Signature:**
```csharp
public bool SaveFile()
```

**Returns:** `bool` - True if saved successfully

---

##### SaveFileAs(string filePath)
Saves the current file to a new location.

**Signature:**
```csharp
public bool SaveFileAs(string filePath)
```

**Parameters:**
- `filePath` (string): Path to save file to

**Returns:** `bool` - True if saved successfully

---

## Settings

### Settings Class

Application settings storage.

**Namespace:** `Calcify.Properties`

#### Properties

All settings are accessible via `Settings.Default`:

```csharp
// Theme
string theme = Settings.Default.Theme;  // "Light" or "Dark"

// Font
string fontFamily = Settings.Default.FontFamily;
int fontSize = Settings.Default.FontSize;

// Calculations
int decimalPlaces = Settings.Default.DecimalPlaces;
bool useThousandsSeparator = Settings.Default.UseThousandsSeparator;

// Auto-save
bool autoSave = Settings.Default.AutoSave;
int autoSaveInterval = Settings.Default.AutoSaveInterval;
```

#### Methods

##### Save()
Persists settings to disk.

**Signature:**
```csharp
public void Save()
```

**Example:**
```csharp
Settings.Default.Theme = "Dark";
Settings.Default.Save();
```

---

##### Reset()
Resets all settings to defaults.

**Signature:**
```csharp
public void Reset()
```

---

## Extension Methods

### StringExtensions

Extension methods for string manipulation.

#### ToDouble()
Parses string to double with error handling.

**Signature:**
```csharp
public static double ToDouble(this string str)
```

**Example:**
```csharp
double value = "3.14".ToDouble();
```

---

## Interfaces

### ICalculationEngine

Interface for calculation engines.

```csharp
public interface ICalculationEngine
{
    double Evaluate(string expression);
    bool TryEvaluate(string expression, out double result);
}
```

---

### IUnitConverter

Interface for unit conversion.

```csharp
public interface IUnitConverter
{
    double Convert(double value, string fromUnit, string toUnit);
    bool IsValidUnit(string unit);
    string[] GetSupportedUnits();
}
```

---

## Events

### Application Events

#### ApplicationStartup
Fired when application starts.

**Signature:**
```csharp
public event EventHandler ApplicationStartup
```

---

#### ApplicationExit
Fired before application exits.

**Signature:**
```csharp
public event EventHandler ApplicationExit
```

---

### Document Events

#### DocumentChanged
Fired when document content changes.

**Signature:**
```csharp
public event EventHandler<DocumentChangedEventArgs> DocumentChanged
```

**EventArgs:**
```csharp
public class DocumentChangedEventArgs : EventArgs
{
    public string NewText { get; set; }
    public int LineNumber { get; set; }
}
```

---

## Enumerations

### Theme
Available themes.

```csharp
public enum Theme
{
    Light,
    Dark,
    System
}
```

---

### AngleUnit
Angle measurement units.

```csharp
public enum AngleUnit
{
    Degrees,
    Radians,
    Gradians
}
```

---

### DecimalSeparator
Decimal separator character.

```csharp
public enum DecimalSeparator
{
    Period,    // 3.14
    Comma      // 3,14
}
```

---

## Constants

### MathConstants

Mathematical constants.

```csharp
public static class MathConstants
{
    public const double Pi = 3.14159265358979323846;
    public const double E = 2.71828182845904523536;
    public const double Phi = 1.61803398874989484820;  // Golden ratio
    public const double Tau = 6.28318530717958647693;  // 2*Pi
}
```

---

### UnitConstants

Unit conversion factors.

```csharp
public static class UnitConstants
{
    public const double KM_TO_MILES = 0.621371;
    public const double POUNDS_TO_KG = 0.453592;
    public const double CELSIUS_TO_FAHRENHEIT_MULT = 1.8;
    public const double CELSIUS_TO_FAHRENHEIT_ADD = 32;
}
```

---

## Usage Examples

### Basic Calculation
```csharp
using Calcify.Classes;

string expression = "2 + 2 * 3";
double result = Math.Evaluate(expression);
Console.WriteLine(result);  // 8.0
```

### Unit Conversion
```csharp
using Calcify.Classes;

double km = 100;
double miles = Math.ConvertUnit(km, "km", "miles");
Console.WriteLine($"{km} km = {miles} miles");
```

### Opening a File Programmatically
```csharp
var mainWindow = new MainWindow();
mainWindow.OpenFile(@"C:\calculations\test.calc");
mainWindow.Show();
```

### Monitoring Settings Changes
```csharp
Settings.Default.PropertyChanged += (sender, e) =>
{
    if (e.PropertyName == "Theme")
    {
        ApplyTheme(Settings.Default.Theme);
    }
};
```

### Custom Syntax Highlighting
```csharp
var syntax = SyntaxFile.LoadSyntax("custom.xshd");
textEditor.SyntaxHighlighting = syntax;
```

---

## Error Codes

| Code | Name | Description |
|------|------|-------------|
| 1001 | InvalidExpression | Expression syntax error |
| 1002 | DivisionByZero | Attempted division by zero |
| 1003 | UndefinedVariable | Variable not defined |
| 1004 | UnitConversionError | Invalid unit conversion |
| 1005 | FileAccessError | Cannot access file |
| 1006 | NetworkError | Network connection failed |

---

## Best Practices

1. **Always validate input** before passing to `Evaluate()`
2. **Use try-catch** for error handling
3. **Check return values** for Save/Load operations
4. **Call Settings.Save()** after changing settings
5. **Dispose resources** properly (file handles, etc.)

---

**See Also:**
- [Architecture Overview](architecture.md)
- [Building from Source](building.md)
- [Contributing Guide](contributing.md)
