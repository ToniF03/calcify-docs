# Advanced Math Functions

Calcify includes a comprehensive set of mathematical functions for scientific and engineering calculations.

## Trigonometric Functions

### Basic Trigonometry

```
sin(90)                 →  1
cos(0)                  →  1
tan(45)                 →  1

sin(30)                 →  0.5
cos(60)                 →  0.5
tan(30)                 →  0.577
```

### Inverse Trigonometry

```
asin(1)                 →  90 (degrees)
acos(1)                 →  0
atan(1)                 →  45

asin(0.5)               →  30
acos(0.5)               →  60
atan(0.577)             →  30
```

### Hyperbolic Functions

```
sinh(1)                 →  1.175
cosh(1)                 →  1.543
tanh(1)                 →  0.762

asinh(1)                →  0.881
acosh(2)                →  1.317
atanh(0.5)              →  0.549
```

### Radians vs Degrees

```
// Degrees (default)
sin(90)                 →  1

// Convert to radians
sin(pi/2)               →  1
sin(90 deg to rad)      →  1

// Use radians directly
sinr(pi/2)              →  1
cosr(pi)                →  -1
tanr(pi/4)              →  1
```

## Logarithmic Functions

### Common Logarithm (base 10)

```
log(100)                →  2
log(1000)               →  3
log(1)                  →  0
log(10)                 →  1
```

### Natural Logarithm (base e)

```
ln(e)                   →  1
ln(1)                   →  0
ln(2.718)               →  1
ln(10)                  →  2.303
```

### Custom Base Logarithm

```
log(8, 2)               →  3  (log base 2 of 8)
log(1000, 10)           →  3  (log base 10 of 1000)
log(27, 3)              →  3  (log base 3 of 27)
```

### Exponential Function

```
exp(1)                  →  2.718 (e^1)
exp(2)                  →  7.389 (e^2)
exp(0)                  →  1
exp(-1)                 →  0.368
```

## Power and Root Functions

### Power

```
pow(2, 3)               →  8
pow(10, 2)              →  100
pow(5, 0)               →  1
pow(2, -1)              →  0.5

// Using ^ operator
2 ^ 3                   →  8
10 ^ 2                  →  100
```

### Square Root

```
sqrt(16)                →  4
sqrt(2)                 →  1.414
sqrt(100)               →  10
sqrt(0.25)              →  0.5
```

### Cube Root

```
cbrt(8)                 →  2
cbrt(27)                →  3
cbrt(64)                →  4
cbrt(-8)                →  -2
```

### Nth Root

```
root(16, 4)             →  2  (4th root of 16)
root(32, 5)             →  2  (5th root of 32)
root(729, 3)            →  9  (cube root)
```

## Rounding Functions

### Round

```
round(3.4)              →  3
round(3.5)              →  4
round(3.6)              →  4
round(-2.5)             →  -2
round(3.14159, 2)       →  3.14  (2 decimal places)
```

### Floor

```
floor(3.9)              →  3
floor(3.1)              →  3
floor(-2.5)             →  -3
floor(5.999)            →  5
```

### Ceiling

```
ceil(3.1)               →  4
ceil(3.9)               →  4
ceil(-2.5)              →  -2
ceil(5.001)             →  6
```

### Truncate

```
trunc(3.9)              →  3
trunc(-3.9)             →  -3
trunc(5.5)              →  5
```

## Absolute Value and Sign

### Absolute Value

```
abs(-10)                →  10
abs(10)                 →  10
abs(-3.14)              →  3.14
abs(0)                  →  0
```

### Sign Function

```
sign(10)                →  1
sign(-5)                →  -1
sign(0)                 →  0
```

## Min and Max

### Minimum

```
min(5, 10)              →  5
min(3, 7, 2, 9)         →  2
min(-5, 0, 5)           →  -5
```

### Maximum

```
max(5, 10)              →  10
max(3, 7, 2, 9)         →  9
max(-5, 0, 5)           →  5
```

## Factorial and Combinatorics

### Factorial

```
fact(5)                 →  120
fact(0)                 →  1
fact(10)                →  3628800
fact(3)                 →  6
```

### Permutations

```
perm(5, 3)              →  60  (5!/(5-3)!)
perm(10, 2)             →  90
```

### Combinations

```
comb(5, 3)              →  10  (5!/(3!*(5-3)!))
comb(10, 2)             →  45
comb(52, 5)             →  2598960  (poker hands)
```

## Statistical Functions

### Sum

```
sum(1, 2, 3, 4, 5)      →  15
sum(10, 20, 30)         →  60
```

### Average (Mean)

```
avg(1, 2, 3, 4, 5)      →  3
avg(10, 20, 30)         →  20
mean(5, 10, 15)         →  10
```

### Median

```
median(1, 2, 3, 4, 5)   →  3
median(1, 2, 3, 4)      →  2.5
median(10, 5, 15)       →  10
```

### Mode

```
mode(1, 2, 2, 3, 4)     →  2
mode(5, 5, 5, 3, 3)     →  5
```

### Standard Deviation

```
stdev(1, 2, 3, 4, 5)    →  1.414
stdev(10, 20, 30)       →  8.165
```

### Variance

```
var(1, 2, 3, 4, 5)      →  2
var(10, 20, 30)         →  66.667
```

## Random Numbers

### Random Float

```
random()                →  0.xxx (between 0 and 1)
random() * 100          →  xx.xxx (between 0 and 100)
```

### Random Integer

```
randint(10)              →  x (integer 0-10)
randint(1, 100)          →  xx (integer 1-100)
randomint(5, 15)           →  x (integer 5-15)
```

## Constants

### Mathematical Constants

```
pi                      →  3.14159265359
e                       →  2.71828182846
phi                     →  1.61803398875 (golden ratio)
tau                     →  6.28318530718 (2*pi)
```

### Using Constants

```
2 * pi                  →  6.283
e ^ 2                   →  7.389
pi * 10 ^ 2             →  314.159
sqrt(2)                 →  1.414
```

## Conversion Functions

### Degrees to Radians

```
180 deg to rad            →  3.14159 (pi)
90 deg to rad(90)         →  1.5708
360 deg to rad            →  6.28319
```

### Radians to Degrees

```
pi rad to deg             →  180
pi/2 rad to deg           →  90
2*pi rad to deg           →  360
```

## Practical Examples

### Physics - Projectile Motion

```
// Initial velocity and angle
v0 = 20              // m/s
angle = 45           // degrees

// Convert to radians
angle_rad = angle deg to rad

// Components
vx = v0 * cos(angle_rad)    →  14.14 m/s
vy = v0 * sin(angle_rad)    →  14.14 m/s

// Maximum height
g = 9.81
h_max = (vy^2) / (2*g)      →  10.19 meters

// Time to max height
t_max = vy / g              →  1.44 seconds

// Total flight time
t_total = 2 * t_max         →  2.88 seconds

// Range
range = vx * t_total        →  40.73 meters
```

### Engineering - Signal Processing

```
// Sine wave
frequency = 50       // Hz
amplitude = 10       // V
time = 0.01         // seconds

signal = amplitude * sin(2 * pi * frequency * time)
→  3.09 V
```

### Finance - Compound Interest

```
principal = 1000
rate = 5            // percent
years = 10

// Compound annually
amount = principal * (1 + rate/100) ^ years
→  1628.89

// Compound monthly
monthly_rate = rate / 12
months = years * 12
amount = principal * (1 + monthly_rate/100) ^ months
→  1647.01
```

### Statistics - Normal Distribution

```
// Z-score
value = 85
mean = 75
stdev = 10

z_score = (value - mean) / stdev
→  1.0

// Approximately 84% of values below this
```

### Geometry - Circle

```
radius = 5

// Circumference
circumference = 2 * pi * radius
→  31.416

// Area
area = pi * radius ^ 2
→  78.540

// Volume of sphere
volume = (4/3) * pi * radius ^ 3
→  523.599
```

### Geometry - Triangle

```
// Sides
a = 3
b = 4
c = 5

// Semi-perimeter
s = (a + b + c) / 2
→  6

// Area (Heron's formula)
area = sqrt(s * (s-a) * (s-b) * (s-c))
→  6

// Check if right triangle
is_right = (a^2 + b^2 == c^2)
→  true
```

### Probability - Combinations

```
// Lottery - choose 6 from 49
total_combinations = comb(49, 6)
→  13,983,816

// Probability of winning
probability = 1 / total_combinations
→  0.0000000715 (0.00000715%)
```

### Computer Science - Binary

```
// Powers of 2
2^8                     →  256
2^16                    →  65536
2^32                    →  4294967296

// Log base 2
log(1024, 2)            →  10
log(65536, 2)           →  16
```

## Complex Expressions

### Nested Functions

```
sqrt(abs(-16))          →  4
log(exp(2))             →  2
sin(asin(0.5))          →  0.5
round(sqrt(50), 2)      →  7.07
```

### Chained Operations

```
value = 10
result = abs(sin(deg2rad(value))) * 100
→  17.36

result = round(log(exp(sqrt(16))), 3)
→  4.000
```

## Tips

1. **Use Parentheses** - Clarify function arguments: `log(100, 10)`
2. **Know Your Units** - Trig functions default to degrees
3. **Check Domains** - Log requires positive numbers
4. **Precision Matters** - Set decimal places in Settings
5. **Use Constants** - `pi`, `e` are built-in

## Common Mistakes

### Wrong Angle Units

```
// Wrong - mixing units
sin(pi)                 →  0.0548 (pi treated as degrees)

// Correct
sin(180)                →  0 (degrees)
sinr(pi)                →  0 (radians)
```

### Division by Zero

```
// Error
tan(90)                 →  Error (approaches infinity)

// Safe
tan(89.9)               →  572.957
```

### Negative Logarithms

```
// Error
log(-10)                →  Error (undefined)

// Safe
log(abs(-10))           →  1
```

---

**Next Steps:**

- Review [Mathematical Functions Reference](../reference/math-functions.md)
- See [Keyboard Shortcuts](../reference/keyboard-shortcuts.md)
- Explore [Settings Options](../reference/settings.md)
