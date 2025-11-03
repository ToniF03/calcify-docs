# Basic Calculations

Learn how to perform arithmetic and basic mathematical operations in Calcify.

## Arithmetic Operations

### Addition

```
2 + 2                   →  4
10 + 5 + 3              →  18
-5 + 10                 →  5
0.5 + 0.25              →  0.75
```

### Subtraction

```
10 - 3                  →  7
5 - 8                   →  -3
100 - 25 - 10           →  65
3.5 - 1.2               →  2.3
```

### Multiplication

```
5 * 6                   →  30
-3 * 4                  →  -12
2 * 3 * 4               →  24
0.5 * 10                →  5
```

### Division

```
10 / 2                  →  5
7 / 2                   →  3.5
100 / 4                 →  25
1 / 3                   →  0.333...
```

### Exponentiation

```
2 ^ 3                   →  8
10 ^ 2                  →  100
5 ^ 0                   →  1
2 ^ -1                  →  0.5
```

### Modulo (Remainder)

```
10 % 3                  →  1
17 % 5                  →  2
100 % 7                 →  2
8 % 2                   →  0
```

## Order of Operations

Calcify follows the standard mathematical order of operations (PEMDAS/BODMAS):

1. **P**arentheses / **B**rackets
2. **E**xponents / **O**rders
3. **M**ultiplication and **D**ivision (left to right)
4. **A**ddition and **S**ubtraction (left to right)

### Examples

```
// Multiplication before addition
5 + 3 * 2               →  11    (not 16)

// Parentheses override default order
(5 + 3) * 2             →  16

// Exponents before multiplication
2 ^ 3 * 4               →  32    (not 4096)

// Division and multiplication, left to right
10 / 2 * 3              →  15

// Complex expression
(10 + 5) * 3 - 8 / 2    →  41
```

## Using Parentheses

Parentheses help clarify expressions and override order of operations:

```
// Without parentheses
10 + 5 * 2              →  20

// With parentheses
(10 + 5) * 2            →  30

// Nested parentheses
((10 + 5) * 2) - 3      →  27

// Multiple groups
(5 + 3) * (10 - 2)      →  64
```

## Working with Negative Numbers

```
-5 + 10                 →  5
-3 * -4                 →  12
10 - -5                 →  15
(-5) ^ 2                →  25
-(5 + 3)                →  -8
```

## Decimal Numbers

Calcify handles decimal numbers with precision:

```
0.1 + 0.2               →  0.3
3.14159 * 2             →  6.28318
10.5 / 2                →  5.25
1.5 ^ 2                 →  2.25
```

### Rounding

Control decimal places in Settings:

```
// 2 decimal places (default)
10 / 3                  →  3.33

// 5 decimal places
10 / 3                  →  3.33333

// No decimal places
10 / 3                  →  3
```

## Large Numbers

Calcify can handle very large numbers:

```
1000000 * 1000000       →  1000000000000
2 ^ 20                  →  1048576
999999999 + 1           →  1000000000
```

### Scientific Notation

For very large or small numbers:

```
1.5e6                   →  1500000
3.2e-3                  →  0.0032
1e9 * 2                 →  2000000000
```

## Thousands Separator

Enable in Settings for easier reading:

```
// Without separator
1000000                 →  1000000

// With separator
1000000                 →  1,000,000
```

## Percentages

Calculate percentages easily:

```
// Find percentage of a number
10% of 100              →  10
25% of 200              →  50
15% of 80               →  12

// Add percentage
100 + 10%               →  110
50 + 25%                →  62.5

// Subtract percentage
100 - 10%               →  90
200 - 25%               →  150

// Percentage increase/decrease
(150 - 100) / 100 * 100 →  50%
```

## Constants

Use built-in mathematical constants:

```
pi                      →  3.14159265359
e                       →  2.71828182846
phi                     →  1.61803398875 (golden ratio)
```

### Using Constants

```
2 * pi                  →  6.28318530718
e ^ 2                   →  7.38905609893
pi * 10 ^ 2             →  314.159265359
```

## Variables

Store values for reuse:

### Defining Variables

```
x = 10
y = 20
z = x + y               →  30
```

### Using Variables

```
price = 100
tax = 8.5%
total = price + (price * tax / 100)
→  108.5
```

### Multiple Calculations

```
a = 5
b = 10
c = 15

a + b                   →  15
b * c                   →  150
(a + b) * c             →  225
```

## Comments

Add notes to your calculations:

```
// This is a comment
10 + 5                  →  15

/* Multi-line
   comment */
20 * 3                  →  60
```

## Absolute Value

Get the absolute (positive) value:

```
abs(-10)                →  10
abs(5)                  →  5
abs(-3.14)              →  3.14
```

## Rounding Functions

### Round

Round to nearest integer:

```
round(3.4)              →  3
round(3.5)              →  4
round(3.6)              →  4
round(-2.5)             →  -2
```

### Floor

Round down to nearest integer:

```
floor(3.9)              →  3
floor(3.1)              →  3
floor(-2.5)             →  -3
```

### Ceiling

Round up to nearest integer:

```
ceil(3.1)               →  4
ceil(3.9)               →  4
ceil(-2.5)              →  -2
```

## Min and Max

Find minimum or maximum values:

```
min(5, 10)              →  5
min(3, 7, 2, 9)         →  2
max(5, 10)              →  10
max(3, 7, 2, 9)         →  9
```

## Power and Roots

### Square Root

```
sqrt(16)                →  4
sqrt(2)                 →  1.41421356237
sqrt(100)               →  10
```

### Cube Root

```
cbrt(8)                 →  2
cbrt(27)                →  3
cbrt(64)                →  4
```

### Nth Root

```
root(16, 4)             →  2  (4th root of 16)
root(32, 5)             →  2  (5th root of 32)
```

## Factorial

Calculate factorials:

```
fact(5)                 →  120
fact(0)                 →  1
fact(10)                →  3628800
```

## Random Numbers

Generate random numbers:

```
random()                →  0.xxx (between 0 and 1)
random(10)              →  x (integer between 0 and 10)
random(5, 10)           →  x (integer between 5 and 10)
```

## Practical Examples

### Calculate Tip

```
bill = 50
tip_percent = 15
tip = bill * tip_percent / 100
total = bill + tip

// Result: tip = 7.5, total = 57.5
```

### Area of Circle

```
radius = 5
area = pi * radius ^ 2

// Result: area = 78.54
```

### Compound Interest

```
principal = 1000
rate = 5
years = 10
amount = principal * (1 + rate/100) ^ years

// Result: amount = 1628.89
```

### Average

```
values = [10, 20, 30, 40, 50]
sum = 10 + 20 + 30 + 40 + 50
average = sum / 5

// Result: average = 30
```

## Tips

1. **Use Parentheses** - Make complex expressions clearer
2. **Store Intermediate Results** - Use variables for multi-step calculations
3. **Check Order** - Remember PEMDAS when writing expressions
4. **Use Constants** - Take advantage of `pi`, `e`, etc.
5. **Add Comments** - Document your work for future reference

## Common Mistakes

### Missing Parentheses

```
// Wrong
10 + 5 * 2              →  20 (not 30)

// Correct
(10 + 5) * 2            →  30
```

### Division by Zero

```
10 / 0                  →  Error: Division by zero
```

### Negative Exponents

```
// Parentheses needed for negative base
-2 ^ 2                  →  -4
(-2) ^ 2                →  4
```

---

**Next Steps:**
- Learn about [Unit Conversions](unit-conversions.md)
- Explore [Advanced Math Functions](advanced-math.md)
- See [Mathematical Functions Reference](../reference/math-functions.md)
