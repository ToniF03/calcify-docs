# Mathematical Functions Reference

Complete reference of all mathematical functions available in Calcify.

## Function Categories

- [Arithmetic](#arithmetic)
- [Trigonometry](#trigonometry)
- [Exponential & Logarithmic](#exponential--logarithmic)
- [Rounding](#rounding)
- [Statistical](#statistical)
- [Utility](#utility)
- [Random](#random)

---

## Arithmetic

### abs(x)

Returns the absolute value of x.

**Syntax:** `abs(number)`

**Examples:**

```
abs(-10)                →  10
abs(5)                  →  5
abs(-3.14)              →  3.14
```

---

### sign(x)

Returns the sign of x: 1 for positive, -1 for negative, 0 for zero.

**Syntax:** `sign(number)`

**Examples:**

```
sign(10)                →  1
sign(-5)                →  -1
sign(0)                 →  0
```

---

### min(x, y, ...)

Returns the minimum value from the arguments.

**Syntax:** `min(number1, number2, ...)`

**Examples:**

```
min(5, 10)              →  5
min(3, 7, 2, 9)         →  2
min(-5, 0, 5)           →  -5
```

---

### max(x, y, ...)

Returns the maximum value from the arguments.

**Syntax:** `max(number1, number2, ...)`

**Examples:**

```
max(5, 10)              →  10
max(3, 7, 2, 9)         →  9
max(-5, 0, 5)           →  5
```

---

### clamp(x, min, max)

Constrains x to be between min and max.

**Syntax:** `clamp(value, min, max)`

**Examples:**

```
clamp(5, 0, 10)         →  5
clamp(-5, 0, 10)        →  0
clamp(15, 0, 10)        →  10
```

---

## Trigonometry

### sin(x)

Sine of x (x in degrees by default).

**Syntax:** `sin(angle_in_degrees)`

**Examples:**

```
sin(0)                  →  0
sin(30)                 →  0.5
sin(90)                 →  1
sin(180)                →  0
```

---

### cos(x)

Cosine of x (x in degrees by default).

**Syntax:** `cos(angle_in_degrees)`

**Examples:**

```
cos(0)                  →  1
cos(60)                 →  0.5
cos(90)                 →  0
cos(180)                →  -1
```

---

### tan(x)

Tangent of x (x in degrees by default).

**Syntax:** `tan(angle_in_degrees)`

**Examples:**

```
tan(0)                  →  0
tan(45)                 →  1
tan(60)                 →  1.732
```

---

### asin(x)

Arc sine (inverse sine) of x, returns angle in degrees.

**Syntax:** `asin(value)`
**Domain:** -1 ≤ x ≤ 1

**Examples:**

```
asin(0)                 →  0
asin(0.5)               →  30
asin(1)                 →  90
```

---

### acos(x)

Arc cosine (inverse cosine) of x, returns angle in degrees.

**Syntax:** `acos(value)`
**Domain:** -1 ≤ x ≤ 1

**Examples:**

```
acos(1)                 →  0
acos(0.5)               →  60
acos(0)                 →  90
```

---

### atan(x)

Arc tangent (inverse tangent) of x, returns angle in degrees.

**Syntax:** `atan(value)`

**Examples:**

```
atan(0)                 →  0
atan(1)                 →  45
atan(1.732)             →  60
```

---

### atan2(y, x)

Arc tangent of y/x, returns angle in degrees, using signs to determine quadrant.

**Syntax:** `atan2(y, x)`

**Examples:**

```
atan2(1, 1)             →  45
atan2(1, -1)            →  135
atan2(-1, -1)           →  -135
```

---

### sinh(x)

Hyperbolic sine of x.

**Syntax:** `sinh(number)`

**Examples:**

```
sinh(0)                 →  0
sinh(1)                 →  1.175
sinh(2)                 →  3.627
```

---

### cosh(x)

Hyperbolic cosine of x.

**Syntax:** `cosh(number)`

**Examples:**

```
cosh(0)                 →  1
cosh(1)                 →  1.543
cosh(2)                 →  3.762
```

---

### tanh(x)

Hyperbolic tangent of x.

**Syntax:** `tanh(number)`

**Examples:**

```
tanh(0)                 →  0
tanh(1)                 →  0.762
tanh(2)                 →  0.964
```

---

## Exponential & Logarithmic

### exp(x)

Returns e raised to the power of x (e^x).

**Syntax:** `exp(power)`

**Examples:**

```
exp(0)                  →  1
exp(1)                  →  2.718
exp(2)                  →  7.389
```

---

### log(x) or log(x, base)

Common logarithm (base 10) or logarithm with custom base.

**Syntax:** `log(number)` or `log(number, base)`
**Domain:** x > 0

**Examples:**

```
log(10)                 →  1
log(100)                →  2
log(1000)               →  3
log(8, 2)               →  3 (log base 2)
```

---

### ln(x)

Natural logarithm (base e).

**Syntax:** `ln(number)`
**Domain:** x > 0

**Examples:**

```
ln(1)                   →  0
ln(e)                   →  1
ln(10)                  →  2.303
```

---

### log2(x)

Logarithm base 2.

**Syntax:** `log2(number)`
**Domain:** x > 0

**Examples:**

```
log2(2)                 →  1
log2(8)                 →  3
log2(1024)              →  10
```

---

### log10(x)

Logarithm base 10 (same as log(x)).

**Syntax:** `log10(number)`
**Domain:** x > 0

**Examples:**

```
log10(10)               →  1
log10(100)              →  2
log10(1000)             →  3
```

---

### pow(x, y)

Returns x raised to the power of y (x^y).

**Syntax:** `pow(base, exponent)` or use `^` operator

**Examples:**

```
pow(2, 3)               →  8
pow(10, 2)              →  100
pow(5, 0)               →  1
2 ^ 3                   →  8
```

---

### sqrt(x)

Square root of x.

**Syntax:** `sqrt(number)`
**Domain:** x ≥ 0

**Examples:**

```
sqrt(4)                 →  2
sqrt(16)                →  4
sqrt(2)                 →  1.414
sqrt(100)               →  10
```

---

### cbrt(x)

Cube root of x.

**Syntax:** `cbrt(number)`

**Examples:**

```
cbrt(8)                 →  2
cbrt(27)                →  3
cbrt(-8)                →  -2
```

---

### root(x, n)

nth root of x.

**Syntax:** `root(number, n)`

**Examples:**

```
root(16, 4)             →  2 (4th root)
root(32, 5)             →  2 (5th root)
root(100, 2)            →  10 (square root)
```

---

## Rounding

### round(x) or round(x, decimals)

Rounds to nearest integer or specified decimal places.

**Syntax:** `round(number)` or `round(number, decimals)`

**Examples:**

```
round(3.4)              →  3
round(3.5)              →  4
round(3.14159, 2)       →  3.14
round(123.456, 1)       →  123.5
```

---

### floor(x)

Rounds down to nearest integer.

**Syntax:** `floor(number)`

**Examples:**

```
floor(3.9)              →  3
floor(3.1)              →  3
floor(-2.5)             →  -3
```

---

### ceil(x)

Rounds up to nearest integer.

**Syntax:** `ceil(number)`

**Examples:**

```
ceil(3.1)               →  4
ceil(3.9)               →  4
ceil(-2.5)              →  -2
```

---

### trunc(x)

Truncates decimal part, returns integer part.

**Syntax:** `trunc(number)`

**Examples:**

```
trunc(3.9)              →  3
trunc(-3.9)             →  -3
trunc(5.5)              →  5
```

---

## Statistical

### sum(x, y, ...)

Sum of all arguments.

**Syntax:** `sum(number1, number2, ...)`

**Examples:**

```
sum(1, 2, 3, 4, 5)      →  15
sum(10, 20, 30)         →  60
```

---

### avg(x, y, ...) or mean(x, y, ...)

Average (arithmetic mean) of arguments.

**Syntax:** `avg(number1, number2, ...)` or `mean(...)`

**Examples:**

```
avg(1, 2, 3, 4, 5)      →  3
mean(10, 20, 30)        →  20
avg(5, 10, 15)          →  10
```

---

### median(x, y, ...)

Middle value when sorted.

**Syntax:** `median(number1, number2, ...)`

**Examples:**

```
median(1, 2, 3, 4, 5)   →  3
median(1, 2, 3, 4)      →  2.5
median(10, 5, 15)       →  10
```

---

### mode(x, y, ...)

Most frequently occurring value.

**Syntax:** `mode(number1, number2, ...)`

**Examples:**

```
mode(1, 2, 2, 3, 4)     →  2
mode(5, 5, 5, 3, 3)     →  5
```

---

### stdev(x, y, ...)

Standard deviation of values.

**Syntax:** `stdev(number1, number2, ...)`

**Examples:**

```
stdev(1, 2, 3, 4, 5)    →  1.414
stdev(10, 20, 30)       →  8.165
```

---

### var(x, y, ...)

Variance of values.

**Syntax:** `var(number1, number2, ...)`

**Examples:**

```
var(1, 2, 3, 4, 5)      →  2
var(10, 20, 30)         →  66.667
```

---

## Utility

### fact(x)

Factorial of x (x!).

**Syntax:** `fact(number)`
**Domain:** x ≥ 0, integer

**Examples:**

```
fact(0)                 →  1
fact(5)                 →  120
10!                     →  3628800
```

---

### perm(n, k)

Permutations: number of ways to arrange k items from n items.

**Syntax:** `perm(n, k)`
**Formula:** n! / (n-k)!

**Examples:**

```
perm(5, 3)              →  60
perm(10, 2)             →  90
```

---

### comb(n, k)

Combinations: number of ways to choose k items from n items.

**Syntax:** `comb(n, k)`
**Formula:** n! / (k! × (n-k)!)

**Examples:**

```
comb(5, 3)              →  10
comb(10, 2)             →  45
comb(52, 5)             →  2598960
```

---

### gcd(x, y)

Greatest common divisor of x and y.

**Syntax:** `gcd(number1, number2)`

**Examples:**

```
gcd(12, 18)             →  6
gcd(100, 50)            →  50
gcd(17, 19)             →  1
```

---

### lcm(x, y)

Least common multiple of x and y.

**Syntax:** `lcm(number1, number2)`

**Examples:**

```
lcm(12, 18)             →  36
lcm(4, 6)               →  12
lcm(7, 5)               →  35
```

---

## Random

### random()

Random number between 0 and 1.

**Syntax:** `random()`

**Examples:**

```
random()                →  0.742 (example)
random() * 100          →  74.2
```

---

### random(max) or random(min, max)

Random integer in specified range.

**Syntax:** `random(max)` or `random(min, max)`

**Examples:**

```
random(10)              →  7 (0 to 10)
random(1, 100)          →  42 (1 to 100)
random(5, 15)           →  11 (5 to 15)
```

---

## Constants

### pi

The mathematical constant π (pi).

**Value:** 3.14159265359

**Examples:**

```
pi                      →  3.14159
2 * pi                  →  6.28319
pi * 10^2               →  314.159
```

---

### e

Euler's number, the base of natural logarithms.

**Value:** 2.71828182846

**Examples:**

```
e                       →  2.71828
e^2                     →  7.38906
ln(e)                   →  1
```

---

### phi

The golden ratio.

**Value:** 1.61803398875

**Examples:**

```
phi                     →  1.61803
phi^2                   →  2.61803
```

---

### tau

Tau, equal to 2π.

**Value:** 6.28318530718

**Examples:**

```
tau                     →  6.28319
tau / 2                 →  3.14159 (pi)
```

---

## Function Chaining

You can nest and chain functions:

```
sqrt(abs(-16))          →  4
log(exp(2))             →  2
round(sqrt(50), 2)      →  7.07
max(min(10, 20), 5)     →  10
```

---

**See Also:**

- [Advanced Math Guide](../features/advanced-math.md)
- [Basic Calculations](../features/basic-calculations.md)
- [Quick Start](../quick-start.md)
