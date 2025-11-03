# Unit Conversions

Calcify supports a wide range of unit conversions for everyday calculations.

## Syntax

The basic syntax for unit conversions is:

```
[value] [source_unit] to [target_unit]
```

**Examples:**
```
10 km to miles
100 pounds to kg
25 °C to °F
```

## Length / Distance

### Metric Units

```
10 km to m              →  10000 meters
1000 m to km            →  1 kilometer
100 cm to m             →  1 meter
1000 mm to m            →  1 meter
```

### Imperial Units

```
1 mile to feet          →  5280 feet
1 yard to feet          →  3 feet
12 inches to feet       →  1 foot
1 foot to inches        →  12 inches
```

### Mixed Conversions

```
10 km to miles          →  6.214 miles
5 miles to km           →  8.047 kilometers
100 feet to meters      →  30.48 meters
10 meters to feet       →  32.808 feet
1 inch to cm            →  2.54 centimeters
10 cm to inches         →  3.937 inches
```

### Supported Length Units

**Metric:**
- Kilometer (km)
- Meter (m)
- Decimeter (dm)
- Centimeter (cm)
- Millimeter (mm)
- Micrometer (μm, um)
- Nanometer (nm)

**Imperial:**
- Mile (mi, mile, miles)
- Yard (yd, yard, yards)
- Foot (ft, foot, feet)
- Inch (in, inch, inches)

## Weight / Mass

### Metric Units

```
1 ton to kg             →  1000 kilograms
1000 g to kg            →  1 kilogram
1000 mg to g            →  1 gram
```

### Imperial Units

```
1 ton to pounds         →  2000 pounds
1 stone to pounds       →  14 pounds
16 oz to pounds         →  1 pound
```

### Mixed Conversions

```
100 kg to pounds        →  220.462 pounds
150 pounds to kg        →  68.039 kilograms
1 kg to oz              →  35.274 ounces
500 g to pounds         →  1.102 pounds
```

### Supported Weight Units

**Metric:**
- Ton (t, ton, tons)
- Kilogram (kg)
- Gram (g)
- Milligram (mg)
- Microgram (μg, ug)

**Imperial:**
- Long Ton (lt)
- Short Ton (tn)
- Stone (st)
- Pound (lb, lbs, pound, pounds)
- Ounce (oz)

## Temperature

### Conversions

```
0 °C to °F              →  32 °Fahrenheit
100 °C to °F            →  212 °Fahrenheit
32 °F to °C             →  0 °Celsius
212 °F to °C            →  100 °Celsius
0 K to °C               →  -273.15 °Celsius
273.15 K to °C          →  0 °Celsius
```

### Supported Temperature Units

- Celsius (°C, C)
- Fahrenheit (°F, F)
- Kelvin (K)
- Rankine (°R, R, Ra)
- Réaumur (°Re, Re)

### Common Temperatures

```
// Freezing point of water
0 °C to °F              →  32 °F
0 °C to K               →  273.15 K

// Boiling point of water
100 °C to °F            →  212 °F
100 °C to K             →  373.15 K

// Room temperature
20 °C to °F             →  68 °F

// Body temperature
37 °C to °F             →  98.6 °F
```

## Data Size

### Binary Conversions

```
1024 bytes to KB        →  1 kilobyte
1024 KB to MB           →  1 megabyte
1024 MB to GB           →  1 gigabyte
1024 GB to TB           →  1 terabyte
```

### Larger Conversions

```
1 TB to GB              →  1024 gigabytes
500 GB to MB            →  512000 megabytes
1000 MB to GB           →  0.977 gigabytes
```

### Supported Data Size Units

- Bit (b, bit, bits)
- Byte (B, byte, bytes)
- Kilobyte (KB, kilobyte)
- Megabyte (MB, megabyte)
- Gigabyte (GB, gigabyte)
- Terabyte (TB, terabyte)
- Petabyte (PB, petabyte)
- Exabyte (EB, exabyte)

### Practical Examples

```
// Download size
5 GB to MB              →  5120 megabytes

// File size
750 MB to GB            →  0.732 gigabytes

// Storage capacity
2 TB to GB              →  2048 gigabytes
```

## Time

### Basic Conversions

```
1 hour to minutes       →  60 minutes
1 minute to seconds     →  60 seconds
1 day to hours          →  24 hours
1 week to days          →  7 days
```

### Larger Time Units

```
1 year to days          →  365 days
1 decade to years       →  10 years
1 century to years      →  100 years
```

### Smaller Time Units

```
1 second to ms          →  1000 milliseconds
1 ms to μs              →  1000 microseconds
1 μs to ns              →  1000 nanoseconds
```

### Supported Time Units

- Century (c, century, centuries)
- Decade (decade, decades)
- Year (yr, year, years)
- Month (mth, month, months)
- Week (wk, week, weeks)
- Day (d, day, days)
- Hour (h, hr, hour, hours)
- Minute (min, minute, minutes)
- Second (s, sec, second, seconds)
- Millisecond (ms, millisecond)
- Microsecond (μs, us, microsecond)
- Nanosecond (ns, nanosecond)

### Practical Time Calculations

```
// Project duration
90 days to weeks        →  12.857 weeks

// Event countdown
48 hours to days        →  2 days

// Processing time
500 ms to seconds       →  0.5 seconds
```

## Angle

### Degree Conversions

```
180 deg to rad          →  3.14159 radians
90 deg to grad          →  100 gradians
360 deg to rad          →  6.28319 radians
```

### Radian Conversions

```
1 rad to deg            →  57.2958 degrees
pi rad to deg           →  180 degrees
2 * pi rad to deg       →  360 degrees
```

### Supported Angle Units

- Degree (deg, degree, degrees, °)
- Radian (rad, radian, radians)
- Gradian (gon, grad, gradian)
- Milliradian (mil, milliradian)
- Angular Minute (arcmin, angular minute)
- Angular Second (arcsec, angular second)

## Frequency

### Conversions

```
1000 Hz to kHz          →  1 kilohertz
1 MHz to Hz             →  1000000 hertz
2.4 GHz to MHz          →  2400 megahertz
```

### Supported Frequency Units

- Hertz (Hz, hertz)
- Kilohertz (kHz, kilohertz)
- Megahertz (MHz, megahertz)
- Gigahertz (GHz, gigahertz)

### Practical Examples

```
// WiFi frequency
2.4 GHz to MHz          →  2400 MHz

// Sound frequency
440 Hz to kHz           →  0.44 kHz

// Processor speed
3.5 GHz to MHz          →  3500 MHz
```

## Multiple Conversions

You can chain conversions:

```
100 cm to m to feet     →  3.281 feet
1000 g to kg to pounds  →  2.205 pounds
24 hours to minutes to seconds
                        →  86400 seconds
```

## Precision

Control decimal precision in Settings:

```
// 2 decimal places
10 km to miles          →  6.21 miles

// 5 decimal places
10 km to miles          →  6.21371 miles

// No decimal places
10 km to miles          →  6 miles
```

## Unit Aliases

Most units have multiple aliases:

```
// All equivalent
10 kilometers to miles
10 km to miles
10 km to mi

// All equivalent
100 kilograms to pounds
100 kg to lbs
100 kg to lb
```

## Practical Examples

### Recipe Conversion

```
2 cups to ml            →  473.176 milliliters
450°F to °C             →  232.222 °Celsius
1 pound to grams        →  453.592 grams
```

### Travel Planning

```
// Distance
500 km to miles         →  310.686 miles

// Speed
100 km/h to mph         →  62.137 mph

// Fuel
50 liters to gallons    →  13.209 gallons
```

### Construction

```
// Room dimensions
12 feet to meters       →  3.658 meters
4 inches to cm          →  10.16 centimeters

// Materials
50 pounds to kg         →  22.68 kilograms
```

### Technology

```
// Storage
256 GB to TB            →  0.25 terabytes

// Speed
100 Mbps to Gbps        →  0.1 gigabits/second

// Display
5.5 inches to cm        →  13.97 centimeters
```

## Tips for Unit Conversions

1. **Use Full Names or Abbreviations** - Both work: `kilometers` or `km`
2. **Check Your Units** - Ensure you're using the right unit type
3. **Use "to" Keyword** - Always include "to" between units
4. **Combine with Math** - `(10 + 5) km to miles` works
5. **Store Results** - `distance_miles = 10 km to miles`

## Common Mistakes

### Missing "to" Keyword

```
// Wrong
10 km miles             →  Error

// Correct
10 km to miles          →  6.214 miles
```

### Incompatible Units

```
// Wrong
10 km to kg             →  Error (length to weight)

// Correct
10 km to miles          →  6.214 miles
```

### Unit Typos

```
// Wrong
10 killometers to miles →  Error (typo)

// Correct
10 kilometers to miles  →  6.214 miles
```

---

**Next Steps:**
- Try [Currency Conversion](currency-conversion.md) for real-time exchange rates
- See [Complete Unit Reference](../reference/supported-units.md)
- Learn about [Advanced Math](advanced-math.md)
