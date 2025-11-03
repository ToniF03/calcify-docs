# Supported Units Reference

Complete list of all units supported in Calcify for conversions.

## Length / Distance

| Unit          | Aliases                         | Symbol | Metric Value  |
| ------------- | ------------------------------- | ------ | ------------- |
| Kilometer     | km, kilometer, kilometers       | km     | 1000 m        |
| Meter         | m, meter, meters                | m      | 1 m           |
| Decimeter     | dm, decimeter, decimeters       | dm     | 0.1 m         |
| Centimeter    | cm, centimeter, centimeters     | cm     | 0.01 m        |
| Millimeter    | mm, millimeter, millimeters     | mm     | 0.001 m       |
| Micrometer    | μm, um, micrometer, micrometers | μm     | 0.000001 m    |
| Nanometer     | nm, nanometer, nanometers       | nm     | 0.000000001 m |
| Mile          | mi, mile, miles                 | mi     | 1609.34 m     |
| Yard          | yd, yard, yards                 | yd     | 0.9144 m      |
| Foot          | ft, foot, feet                  | ft     | 0.3048 m      |
| Inch          | in, inch, inches                | in     | 0.0254 m      |
| Nautical Mile | nmi, nautical mile              | nmi    | 1852 m        |

**Examples:**

```
10 km to miles
100 feet to meters
5 inches to cm
```

## Weight / Mass

| Unit       | Aliases                       | Symbol | Metric Value   |
| ---------- | ----------------------------- | ------ | -------------- |
| Metric Ton | t, ton, tons, metric ton      | t      | 1000 kg        |
| Kilogram   | kg, kilogram, kilograms       | kg     | 1 kg           |
| Gram       | g, gram, grams                | g      | 0.001 kg       |
| Milligram  | mg, milligram, milligrams     | mg     | 0.000001 kg    |
| Microgram  | μg, ug, microgram, micrograms | μg     | 0.000000001 kg |
| Long Ton   | lt, long ton                  | lt     | 1016.05 kg     |
| Short Ton  | tn, short ton                 | tn     | 907.185 kg     |
| Stone      | st, stone                     | st     | 6.35029 kg     |
| Pound      | lb, lbs, pound, pounds        | lb     | 0.453592 kg    |
| Ounce      | oz, ounce, ounces             | oz     | 0.0283495 kg   |
| Carat      | ct, carat, carats             | ct     | 0.0002 kg      |

**Examples:**

```
150 pounds to kg
500 grams to oz
2 tons to kg
```

## Temperature

| Unit       | Aliases            | Symbol | Notes                |
| ---------- | ------------------ | ------ | -------------------- |
| Celsius    | °C, C, celsius     | °C     | Metric standard      |
| Fahrenheit | °F, F, fahrenheit  | °F     | Imperial standard    |
| Kelvin     | K, kelvin          | K      | Absolute zero at 0 K |
| Rankine    | °R, R, Ra, rankine | °R     | Absolute Fahrenheit  |
| Réaumur    | °Re, Re, reaumur   | °Re    | Historical           |

**Formulas:**

- °F = (°C × 9/5) + 32
- K = °C + 273.15
- °R = °F + 459.67

**Examples:**

```
25 °C to °F
100 °F to °C
0 K to °C
```

## Data Size

| Unit     | Aliases                 | Symbol | Binary Value |
| -------- | ----------------------- | ------ | ------------ |
| Bit      | b, bit, bits            | b      | 1 bit        |
| Byte     | B, byte, bytes          | B      | 8 bits       |
| Kilobyte | KB, kilobyte, kilobytes | KB     | 1024 bytes   |
| Megabyte | MB, megabyte, megabytes | MB     | 1024 KB      |
| Gigabyte | GB, gigabyte, gigabytes | GB     | 1024 MB      |
| Terabyte | TB, terabyte, terabytes | TB     | 1024 GB      |
| Petabyte | PB, petabyte, petabytes | PB     | 1024 TB      |
| Exabyte  | EB, exabyte, exabytes   | EB     | 1024 PB      |

**Note:** Uses binary (base-1024) not decimal (base-1000)

**Examples:**

```
1024 MB to GB
500 GB to TB
1 TB to GB
```

## Time

| Unit        | Aliases                           | Symbol | Seconds         |
| ----------- | --------------------------------- | ------ | --------------- |
| Century     | c, century, centuries             | c      | 3,153,600,000   |
| Decade      | decade, decades                   | -      | 315,360,000     |
| Year        | yr, year, years                   | yr     | 31,536,000      |
| Month       | mth, month, months                | -      | 2,628,000 (avg) |
| Week        | wk, week, weeks                   | wk     | 604,800         |
| Day         | d, day, days                      | d      | 86,400          |
| Hour        | h, hr, hour, hours                | h      | 3,600           |
| Minute      | min, minute, minutes              | min    | 60              |
| Second      | s, sec, second, seconds           | s      | 1               |
| Millisecond | ms, millisecond, milliseconds     | ms     | 0.001           |
| Microsecond | μs, us, microsecond, microseconds | μs     | 0.000001        |
| Nanosecond  | ns, nanosecond, nanoseconds       | ns     | 0.000000001     |

**Examples:**

```
1 hour to minutes
90 minutes to hours
1 week to days
```

## Angle

| Unit           | Aliases                 | Symbol | Value         |
| -------------- | ----------------------- | ------ | ------------- |
| Degree         | deg, degree, degrees, ° | °      | 1/360 circle  |
| Radian         | rad, radian, radians    | rad    | π/180 degrees |
| Gradian        | gon, grad, gradian      | gon    | 1/400 circle  |
| Milliradian    | mil, milliradian        | mil    | 1/1000 radian |
| Angular Minute | arcmin, angular minute  | '      | 1/60 degree   |
| Angular Second | arcsec, angular second  | "      | 1/60 arcmin   |
| Turn           | turn, revolution        | -      | 360 degrees   |

**Examples:**

```
180 deg to rad
pi rad to deg
90 deg to grad
```

## Frequency

| Unit      | Aliases        | Symbol | Hertz             |
| --------- | -------------- | ------ | ----------------- |
| Hertz     | Hz, hertz      | Hz     | 1                 |
| Kilohertz | kHz, kilohertz | kHz    | 1,000             |
| Megahertz | MHz, megahertz | MHz    | 1,000,000         |
| Gigahertz | GHz, gigahertz | GHz    | 1,000,000,000     |
| Terahertz | THz, terahertz | THz    | 1,000,000,000,000 |

**Examples:**

```
1000 Hz to kHz
2.4 GHz to MHz
440 Hz to kHz
```

## Volume

| Unit             | Aliases                         | Symbol | Liters     |
| ---------------- | ------------------------------- | ------ | ---------- |
| Liter            | l, L, liter, liters             | L      | 1          |
| Milliliter       | ml, mL, milliliter, milliliters | mL     | 0.001      |
| Gallon (US)      | gal, gallon, gallons            | gal    | 3.78541    |
| Gallon (UK)      | gal UK, imperial gallon         | gal    | 4.54609    |
| Quart            | qt, quart, quarts               | qt     | 0.946353   |
| Pint             | pt, pint, pints                 | pt     | 0.473176   |
| Cup              | cup, cups                       | cup    | 0.236588   |
| Fluid Ounce      | fl oz, fluid ounce              | fl oz  | 0.0295735  |
| Tablespoon       | tbsp, tablespoon                | tbsp   | 0.0147868  |
| Teaspoon         | tsp, teaspoon                   | tsp    | 0.00492892 |
| Cubic Meter      | m³, m3, cubic meter             | m³     | 1000       |
| Cubic Centimeter | cm³, cm3, cc, cubic cm          | cm³    | 0.001      |

**Examples:**

```
1 gallon to liters
500 ml to cups
1 liter to fl oz
```

## Area

| Unit              | Aliases               | Symbol | Square Meters |
| ----------------- | --------------------- | ------ | ------------- |
| Square Kilometer  | km², km2, square km   | km²    | 1,000,000     |
| Square Meter      | m², m2, square m      | m²     | 1             |
| Square Centimeter | cm², cm2, square cm   | cm²    | 0.0001        |
| Hectare           | ha, hectare, hectares | ha     | 10,000        |
| Acre              | acre, acres           | ac     | 4046.86       |
| Square Mile       | mi², mi2, square mile | mi²    | 2,589,988     |
| Square Yard       | yd², yd2, square yard | yd²    | 0.836127      |
| Square Foot       | ft², ft2, square foot | ft²    | 0.092903      |
| Square Inch       | in², in2, square inch | in²    | 0.00064516    |

**Examples:**

```
1 acre to m²
100 ft² to m²
1 km² to acres
```

## Speed / Velocity

| Unit           | Aliases         | Symbol | m/s           |
| -------------- | --------------- | ------ | ------------- |
| Meter/Second   | m/s, mps        | m/s    | 1             |
| Kilometer/Hour | km/h, kmph, kph | km/h   | 0.277778      |
| Mile/Hour      | mph, mi/h       | mph    | 0.44704       |
| Foot/Second    | ft/s, fps       | ft/s   | 0.3048        |
| Knot           | kn, knot, knots | kn     | 0.514444      |
| Speed of Light | c               | c      | 299,792,458   |
| Mach           | mach            | Ma     | ~343 (varies) |

**Examples:**

```
100 km/h to mph
60 mph to km/h
50 m/s to mph
```

## Pressure

| Unit       | Aliases         | Symbol | Pascals   |
| ---------- | --------------- | ------ | --------- |
| Pascal     | Pa, pascal      | Pa     | 1         |
| Kilopascal | kPa, kilopascal | kPa    | 1,000     |
| Megapascal | MPa, megapascal | MPa    | 1,000,000 |
| Bar        | bar             | bar    | 100,000   |
| Atmosphere | atm, atmosphere | atm    | 101,325   |
| PSI        | psi             | psi    | 6,894.76  |
| Torr       | torr            | torr   | 133.322   |
| mmHg       | mmHg, mm Hg     | mmHg   | 133.322   |

**Examples:**

```
1 atm to psi
100 kPa to bar
30 psi to kPa
```

## Energy

| Unit          | Aliases                | Symbol | Joules      |
| ------------- | ---------------------- | ------ | ----------- |
| Joule         | J, joule               | J      | 1           |
| Kilojoule     | kJ, kilojoule          | kJ     | 1,000       |
| Calorie       | cal, calorie           | cal    | 4.184       |
| Kilocalorie   | kcal, kilocalorie, Cal | kcal   | 4,184       |
| Watt-hour     | Wh, watt-hour          | Wh     | 3,600       |
| Kilowatt-hour | kWh, kilowatt-hour     | kWh    | 3,600,000   |
| Electronvolt  | eV, electronvolt       | eV     | 1.60218e-19 |
| BTU           | btu, BTU               | BTU    | 1,055.06    |

**Examples:**

```
1 kWh to MJ
100 cal to J
1000 BTU to kJ
```

## Power

| Unit       | Aliases        | Symbol | Watts     |
| ---------- | -------------- | ------ | --------- |
| Watt       | W, watt        | W      | 1         |
| Kilowatt   | kW, kilowatt   | kW     | 1,000     |
| Megawatt   | MW, megawatt   | MW     | 1,000,000 |
| Horsepower | hp, horsepower | hp     | 745.7     |
| BTU/hour   | BTU/h, btu/hr  | BTU/h  | 0.293071  |

**Examples:**

```
100 hp to kW
5 kW to hp
1000 W to hp
```

## Using Units in Calcify

### Basic Syntax

```
[value] [source_unit] to [target_unit]
```

### Tips

1. **Case Insensitive** - `KM`, `km`, `Km` all work
2. **Use Aliases** - Most units have multiple names
3. **Combine with Math** - `(10 + 5) km to miles`
4. **Chain Conversions** - `100 cm to m to feet`

### Common Patterns

```
// Multiple values
10 km to miles
20 km to miles
30 km to miles

// With variables
distance = 100
distance km to miles

// In expressions
area = 10 m * 5 m
area to ft²
```

---

**See Also:**

- [Unit Conversions Guide](../features/unit-conversions.md)
- [Currency Conversion](../features/currency-conversion.md)
- [Quick Start Guide](../quick-start.md)
