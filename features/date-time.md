# Date and Time

Calcify includes powerful date and time calculation features for working with dates, durations, and time zones.

## Current Date and Time

### Keywords

```
today                   →  2025-11-03
now                     →  2025-11-03 14:30:45
```

### Date Components

```
today.year              →  2025
today.month             →  11
today.day               →  3
today.dayOfWeek         →  Monday

now.hour                →  14
now.minute              →  30
now.second              →  45
```

## Date Arithmetic

### Adding Time

```
today + 1 day           →  2025-11-04
today + 7 days          →  2025-11-10
today + 2 weeks         →  2025-11-17
today + 1 month         →  2025-12-03
today + 1 year          →  2026-11-03

now + 1 hour            →  2025-11-03 15:30:45
now + 30 minutes        →  2025-11-03 15:00:45
now + 45 seconds        →  2025-11-03 14:31:30
```

### Subtracting Time

```
today - 1 day           →  2025-11-02
today - 1 week          →  2025-10-27
today - 1 month         →  2025-10-03
today - 1 year          →  2024-11-03

now - 2 hours           →  2025-11-03 12:30:45
now - 15 minutes        →  2025-11-03 14:15:45
```

## Date Differences

### Days Between Dates

```
2025-12-25 - today      →  52 days
today - 2025-01-01      →  307 days

// Absolute difference
abs(2025-01-01 - today) →  307 days
```

### Time Differences

```
// Hours between times
17:00 - 14:30           →  2.5 hours
now - 09:00             →  5.5 hours

// Minutes between times
14:30 - 13:45           →  45 minutes
```

## Specific Dates

### Date Formats

```
// ISO format (YYYY-MM-DD)
2025-11-03

// US format (MM/DD/YYYY)
11/03/2025

// European format (DD.MM.YYYY)
03.11.2025

// Written format
November 3, 2025
Nov 3, 2025
```

### Specific Times

```
// 24-hour format
14:30:00
14:30

// 12-hour format
2:30 PM
2:30 pm
```

## Practical Examples

### Age Calculator

```
birthdate = 1990-05-15
age = (today - birthdate) / 365.25
→  35.46 years

// In days
today - birthdate       →  12921 days
```

### Project Planning

```
start_date = 2025-11-03
duration = 45 days
end_date = start_date + duration
→  2025-12-18

// Working days (5-day week)
working_days = duration * (5/7)
→  32.14 working days
```

### Countdown Timer

```
// Days until Christmas
christmas = 2025-12-25
countdown = christmas - today
→  52 days

// Weeks until event
weeks = countdown / 7
→  7.43 weeks
```

### Event Duration

```
start = 2025-11-03 09:00
end = 2025-11-03 17:30
duration = end - start
→  8.5 hours

// In minutes
duration * 60           →  510 minutes
```

### Deadline Tracking

```
deadline = 2025-11-15
days_left = deadline - today
→  12 days

// Business days (rough estimate)
business_days = days_left * (5/7)
→  8.57 days
```

### Time Zone Conversion

```
// Local time to UTC
local = 14:30
utc_offset = -5 hours
utc = local - utc_offset
→  19:30 UTC

// UTC to another timezone
utc = 19:30
tokyo_offset = +9 hours
tokyo = utc + tokyo_offset
→  04:30 (next day)
```

## Duration Calculations

### Work Hours

```
// Daily hours
start = 09:00
end = 17:00
lunch = 1 hour
work_hours = end - start - lunch
→  7 hours

// Weekly hours
weekly = work_hours * 5
→  35 hours

// Annual hours
annual = weekly * 52
→  1820 hours
```

### Travel Time

```
// Flight duration
departure = 10:30
arrival = 16:45
duration = arrival - departure
→  6.25 hours (6h 15m)

// With timezone change
departure = 10:30
arrival = 14:45
time_diff = 2 hours
actual_duration = arrival - departure - time_diff
→  2.25 hours
```

### Meeting Duration

```
start = 14:00
end = 15:30
duration = end - start
→  1.5 hours

// In minutes
duration * 60           →  90 minutes
```

## Date Ranges

### Days in Month

```
// November 2025
days_in_month = 30

// Calculate for any month
// January, March, May, July, August, October, December
days = 31

// April, June, September, November
days = 30

// February (leap year check)
year = 2024
is_leap = (year % 4 == 0) && (year % 100 != 0 || year % 400 == 0)
days = is_leap ? 29 : 28
```

### Week Numbers

```
// Week of year
today.weekOfYear        →  44

// Days in current week
days_in_week = 7
```

## Formatting

### Date Formats

```
// Long format
today.format("MMMM dd, yyyy")
→  November 03, 2025

// Short format
today.format("MM/dd/yy")
→  11/03/25

// ISO format
today.format("yyyy-MM-dd")
→  2025-11-03
```

### Time Formats

```
// 24-hour
now.format("HH:mm:ss")  →  14:30:45

// 12-hour with AM/PM
now.format("hh:mm a")   →  02:30 PM

// Time only
now.format("HH:mm")     →  14:30
```

## Business Date Calculations

### Working Days

```
// Exclude weekends (rough estimate)
total_days = 30
working_days = total_days * (5/7)
→  21.43 working days

// Including holidays (manual)
holidays = 2
actual_working_days = working_days - holidays
→  19.43 working days
```

### Business Day Addition

```
// Add 10 business days
start = today
calendar_days = 10 * (7/5)
end_date = start + calendar_days
→  14 days later
```

## Recurring Events

### Weekly Recurrence

```
// Every Monday
start = 2025-11-03
week1 = start
week2 = start + 7 days
week3 = start + 14 days
week4 = start + 21 days
```

### Monthly Recurrence

```
// Same day each month
start = 2025-11-03
month1 = start
month2 = start + 1 month   →  2025-12-03
month3 = start + 2 months  →  2026-01-03
```

### Annual Recurrence

```
// Birthdays, anniversaries
anniversary = 2020-06-15
next_anniversary = anniversary + 5 years
→  2025-06-15
```

## Time Periods

### Quarters

```
// Q1: Jan-Mar
q1_start = 2025-01-01
q1_end = 2025-03-31

// Q2: Apr-Jun
q2_start = 2025-04-01
q2_end = 2025-06-30

// Q3: Jul-Sep
q3_start = 2025-07-01
q3_end = 2025-09-30

// Q4: Oct-Dec
q4_start = 2025-10-01
q4_end = 2025-12-31
```

### Semesters

```
// First semester
s1_start = 2025-01-01
s1_end = 2025-06-30
s1_days = s1_end - s1_start
→  181 days

// Second semester
s2_start = 2025-07-01
s2_end = 2025-12-31
s2_days = s2_end - s2_start
→  184 days
```

## Elapsed Time

### Time Since Event

```
launch_date = 2023-01-15
elapsed = today - launch_date
→  658 days

// In years
years = elapsed / 365.25
→  1.8 years
```

### Time Until Event

```
vacation = 2025-12-20
remaining = vacation - today
→  47 days

// In weeks
weeks = remaining / 7
→  6.71 weeks
```

## Tips

1. **Use ISO Format** - YYYY-MM-DD is clearest: `2025-11-03`
2. **Be Specific** - Include times when precision matters
3. **Account for Leap Years** - Use 365.25 for year calculations
4. **Time Zones** - Remember to adjust for different zones
5. **Business Days** - Account for weekends and holidays manually

## Common Patterns

### Days Until Birthday

```
birthday = 2025-05-15
days_until = birthday - today
→  193 days

weeks_until = days_until / 7
→  27.57 weeks
```

### Age in Days

```
born = 1990-01-01
age_days = today - born
→  13055 days

age_years = age_days / 365.25
→  35.74 years
```

### Project Timeline

```
start = 2025-11-03
phase1 = 30 days
phase2 = 45 days
phase3 = 20 days

phase1_end = start + phase1      →  2025-12-03
phase2_end = phase1_end + phase2 →  2026-01-17
phase3_end = phase2_end + phase3 →  2026-02-06
total = phase3_end - start       →  95 days
```

### Subscription Renewal

```
start_date = 2025-01-01
subscription = 1 year
renewal = start_date + subscription
→  2026-01-01

days_left = renewal - today
→  59 days
```

---

**Next Steps:**
- Explore [Advanced Math Functions](advanced-math.md)
- Check [Keyboard Shortcuts](../reference/keyboard-shortcuts.md)
- Review [Settings Options](../reference/settings.md)
