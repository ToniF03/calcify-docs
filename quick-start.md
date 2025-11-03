# Quick Start Guide

Get up and running with Calcify in just a few minutes!

## Your First Calculation

1. **Launch Calcify**
   
   - Open Calcify from your Start Menu or desktop shortcut

2. **Type Your Expression**
   
   ```
   2 + 2
   ```
   
   - The result appears automatically: `4`

3. **Try More Complex Expressions**
   
   ```
   (10 + 5) * 3 / 2
   ```
   
   - Result: `22.5`

That's it! Calcify evaluates expressions as you type.

## Basic Operations

### Arithmetic Operations

```
Addition:       5 + 3       →  8
Subtraction:    10 - 4      →  6
Multiplication: 6 * 7       →  42
Division:       15 / 3      →  5
Exponent:       2 ^ 8       →  256
Modulo:         17 % 5      →  2
```

### Order of Operations

Calcify follows standard mathematical order (PEMDAS):

```
5 + 3 * 2       →  11    (not 16)
(5 + 3) * 2     →  16    (parentheses first)
2 ^ 3 * 4       →  32    (exponents first)
```

## Unit Conversions

### Length Conversion

Type the value with the unit, then the target unit:

```
10 cm to inches     →  3.937 inches
5 miles to km       →  8.047 kilometers
100 feet to meters  →  30.48 meters
```

### Weight Conversion

```
150 pounds to kg    →  68.04 kilograms
2 tons to pounds    →  4000 pounds
500 grams to oz     →  17.64 ounces
```

### Temperature Conversion

```
25 °C to °F         →  77 °Fahrenheit
100 °F to °C        →  37.78 °Celsius
0 K to °C           →  -273.15 °Celsius
```

### Data Size Conversion

```
1024 MB to GB       →  1 gigabyte
500 KB to MB        →  0.488 megabytes
1 TB to GB          →  1024 gigabytes
```

## Currency Conversion

Calcify uses real-time exchange rates:

```
100 USD to EUR      →  92.45 EUR (example rate)
50 GBP to USD       →  63.75 USD (example rate)
1000 JPY to USD     →  6.85 USD (example rate)
```

> **Note**: Exchange rates are fetched from the internet and update automatically.

## Working with Dates

### Date Calculations

```
today + 30 days         →  [30 days from now]
2025-12-25 - today      →  [days until Christmas]
now + 2 hours           →  [current time + 2 hours]
```

### Date Formatting

```
today                   →  2025-11-02
now                     →  2025-11-02 14:30:45
```

## Mathematical Functions

### Common Functions

```
sqrt(16)                →  4
abs(-10)                →  10
round(3.7)              →  4
floor(3.9)              →  3
ceil(3.1)               →  4
```

### Trigonometry

```
sin(90)                 →  1
cos(0)                  →  1
tan(45)                 →  1
```

### Logarithms

```
log(100)                →  2 (base 10)
ln(2.718)               →  1 (natural log)
```

## Using Variables

### Define Variables

```
x = 10
y = 20
x + y                   →  30
```

### Reuse in Calculations

```
price = 100
tax = price * 0.08
total = price + tax     →  108
```

## Smart Features

### Auto-Calculation

As you move your cursor (caret) through your work, Calcify automatically calculates the value at that position.

**Example:**

```
100 + 50 = 150
200 - 75 = 125
300 * 2 = 600
```

Place your cursor on any line, and the result appears instantly.

### Drag and Drop

You can drag supported file types directly onto the Calcify window:

- `.txt` files
- `.calc` files (Calcify format)
- Other text-based files

The file will open automatically if supported.

## Keyboard Shortcuts

Speed up your workflow with these shortcuts:

| Shortcut           | Action           |
| ------------------ | ---------------- |
| `Ctrl + N`         | New file         |
| `Ctrl + O`         | Open file        |
| `Ctrl + S`         | Save file        |
| `Ctrl + Shift + S` | Save As          |
| `Ctrl + Z`         | Undo             |
| `Ctrl + Y`         | Redo             |
| `Ctrl + F`         | Find             |
| `Ctrl + H`         | Find and Replace |
| `Ctrl + ,`         | Open Settings    |
| `F1`               | Help             |

## Switching Themes

Calcify supports both light and dark themes:

1. Click the **Settings** icon (gear) in the toolbar
2. Go to **Appearance**
3. Select **Light** or **Dark** theme
4. The theme changes immediately

Or use the theme toggle button in the toolbar.

## Tips for Beginners

1. **Use Parentheses** - Make complex expressions clearer: `(a + b) * (c + d)`
2. **Check Units** - Always specify units for conversions: `10 km to miles`
3. **Save Your Work** - Use `Ctrl + S` to save calculations you want to keep
4. **Experiment** - Try different functions and conversions to learn
5. **Use Comments** - Add notes with `//` at the start of a line

## Example Session

Here's a practical example of using Calcify:

```
// Calculate project budget
materials = 2500 USD
labor = 3000 USD
overhead = (materials + labor) * 0.15
total = materials + labor + overhead

// Result: total = 6325 USD

// Convert to EUR for client
total to EUR
// Result: ~5837.81 EUR

// Calculate weekly cost
total / 4 weeks
// Result: 1581.25 USD per week
```

## Next Steps

Now that you know the basics, explore more features:

- [User Interface Guide](user-interface.md) - Learn all interface elements
- [Unit Conversions](features/unit-conversions.md) - Complete conversion guide
- [Advanced Math](features/advanced-math.md) - Explore mathematical functions
- [Keyboard Shortcuts](reference/keyboard-shortcuts.md) - Speed up your workflow

---

**Ready to learn more?** Check out the [full documentation](README.md) or join our [Discord community](https://discord.gg/MfHHgYtWub)!
