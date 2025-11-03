# Currency Conversion

Calcify provides real-time currency conversion using live exchange rates from the internet.

## Basic Syntax

```
[amount] [source_currency] to [target_currency]
```

**Examples:**
```
100 USD to EUR
50 GBP to USD
1000 JPY to EUR
```

## Supported Currencies

Calcify supports all major world currencies including:

### Major Currencies

| Code | Currency |
|------|----------|
| USD | US Dollar |
| EUR | Euro |
| GBP | British Pound |
| JPY | Japanese Yen |
| CHF | Swiss Franc |
| CAD | Canadian Dollar |
| AUD | Australian Dollar |
| NZD | New Zealand Dollar |
| CNY | Chinese Yuan |
| INR | Indian Rupee |

### Other Currencies

- **AED** - UAE Dirham
- **ARS** - Argentine Peso
- **BRL** - Brazilian Real
- **CZK** - Czech Koruna
- **DKK** - Danish Krone
- **HKD** - Hong Kong Dollar
- **HUF** - Hungarian Forint
- **IDR** - Indonesian Rupiah
- **ILS** - Israeli Shekel
- **KRW** - South Korean Won
- **MXN** - Mexican Peso
- **MYR** - Malaysian Ringgit
- **NOK** - Norwegian Krone
- **PHP** - Philippine Peso
- **PLN** - Polish Zloty
- **RUB** - Russian Ruble
- **SEK** - Swedish Krona
- **SGD** - Singapore Dollar
- **THB** - Thai Baht
- **TRY** - Turkish Lira
- **ZAR** - South African Rand

...and many more!

## Examples

### Simple Conversions

```
100 USD to EUR          →  92.45 EUR
50 GBP to USD           →  63.75 USD
1000 JPY to USD         →  6.85 USD
500 EUR to GBP          →  433.50 GBP
```

### Cross-Currency Conversions

```
100 AUD to CAD          →  88.50 CAD
1000 CNY to INR         →  11450 INR
50 CHF to SEK           →  565 SEK
```

### Large Amounts

```
10000 USD to EUR        →  9245 EUR
1000000 JPY to USD      →  6850 USD
5000 GBP to AUD         →  9625 AUD
```

## Exchange Rate Updates

### Automatic Updates

Calcify automatically fetches the latest exchange rates:
- **On Startup** - Rates update when you launch Calcify
- **Periodic Updates** - Every 1-6 hours (configurable)
- **Manual Refresh** - Force update in Settings

### Update Interval

Configure in **Settings** → **Calculations**:
- 1 hour (most current, requires internet)
- 3 hours (balanced, default)
- 6 hours (less frequent)
- 12 hours (minimal updates)
- 24 hours (daily)

### Offline Mode

When internet is unavailable:
- Calcify uses the last fetched rates
- A warning indicates the data age
- Conversions still work with cached rates

## Practical Examples

### Travel Planning

```
// Convert budget to local currency
budget = 2000 USD
budget to EUR           →  1849 EUR
budget to JPY           →  292000 JPY

// Daily allowance
daily = budget / 14
daily to GBP            →  102.14 GBP
```

### Shopping

```
// Compare prices
price_us = 99.99 USD
price_uk = 79.99 GBP

price_us to GBP         →  78.74 GBP
// UK price is higher by ~1.25 GBP
```

### Investment Tracking

```
// Portfolio value
stocks = 5000 USD
bonds = 3000 EUR
crypto = 500 GBP

// Convert all to USD
bonds to USD            →  3245.50 USD
crypto to USD           →  637.50 USD

total_usd = stocks + 3245.50 + 637.50
→  8883 USD
```

### Business

```
// Invoice conversion
invoice = 10000 EUR
invoice to USD          →  10815 USD
invoice to GBP          →  8670 GBP
invoice to JPY          →  1580000 JPY
```

### Salary Comparison

```
// Job offers
offer_london = 60000 GBP
offer_nyc = 85000 USD
offer_tokyo = 10000000 JPY

// Convert all to USD
offer_london to USD     →  76500 USD
offer_tokyo to USD      →  68500 USD

// NYC offer is highest
```

## Using with Variables

```
// Set base amount
amount = 1000

// Convert to multiple currencies
amount USD to EUR
amount USD to GBP
amount USD to JPY
amount USD to CAD
```

## Combining with Math

```
// Calculate with conversion
(500 USD + 300 EUR to USD) * 1.1
→  (500 + 324.75) * 1.1
→  907.23 USD

// Percentage of budget
budget = 5000 USD
spent = 1200 EUR to USD
remaining = budget - spent
percentage = (spent / budget) * 100
→  26.1% spent
```

## Formatting Options

### Decimal Places

Set in **Settings** → **Calculations**:

```
// 2 decimal places (default)
100 USD to EUR          →  92.45 EUR

// 4 decimal places
100 USD to EUR          →  92.4500 EUR

// No decimals
100 USD to EUR          →  92 EUR
```

### Thousands Separator

Enable in **Settings**:

```
// Without separator
10000 USD to JPY        →  1460000 JPY

// With separator
10000 USD to JPY        →  1,460,000 JPY
```

## Exchange Rate Information

### Rate Source

Calcify uses the **Frankfurter API** for exchange rates:
- Free and open-source
- Updated daily from European Central Bank
- Reliable and accurate
- No API key required

### Base Currency

Rates are based on EUR (Euro) from the ECB:
- All conversions go through EUR
- Updated daily at ~16:00 CET
- Historical accuracy

## Tips

1. **Check Rate Age** - Verify rates are current in Settings
2. **Internet Required** - First conversion needs internet
3. **Use Variables** - Store amounts for multiple conversions
4. **Round Appropriately** - Set decimal places for your needs
5. **Cache Rates** - Offline mode uses last update

## Limitations

### Update Frequency

- Rates update once per day (via ECB)
- Real-time trading rates not available
- Minor delays in volatile markets

### Currency Coverage

- Most major currencies supported
- Some exotic currencies may be unavailable
- Cryptocurrencies not included

### Accuracy

- Rates are indicative, not trading rates
- Bank/exchange fees not included
- Use for estimation, not official transactions

## Common Issues

### No Internet Connection

**Problem:** Cannot fetch exchange rates

**Solution:**
- Connect to internet
- Rates from last update will be used
- Check age indicator in Settings

### Outdated Rates

**Problem:** Rates seem old

**Solution:**
- Go to Settings → Calculations
- Click "Update Exchange Rates Now"
- Check your internet connection

### Unknown Currency Code

**Problem:** Currency code not recognized

**Solution:**
- Verify the 3-letter ISO code (USD, EUR, etc.)
- Check spelling
- See supported currencies list above

## Advanced Usage

### Multi-Currency Portfolio

```
// Define holdings
usd_cash = 5000 USD
eur_stocks = 10000 EUR
gbp_bonds = 3000 GBP
jpy_savings = 500000 JPY

// Convert all to USD
eur_stocks to USD       →  10815 USD
gbp_bonds to USD        →  3825 USD
jpy_savings to USD      →  3425 USD

// Total in USD
total = 5000 + 10815 + 3825 + 3425
→  23065 USD
```

### Currency Arbitrage

```
// Check for arbitrage opportunities
usd_eur = 1 USD to EUR
eur_gbp = 1 EUR to GBP
gbp_usd = 1 GBP to USD

// Full circle
result = usd_eur * eur_gbp * gbp_usd
// Should equal ~1.0 (no arbitrage)
```

### Historical Comparison

```
// Current rate
current = 100 USD to EUR

// Compare with yesterday's note
yesterday = 92.50 EUR
change = current - yesterday
change_percent = (change / yesterday) * 100
```

## API Information

For developers interested in the exchange rate source:

**Frankfurter API**
- Endpoint: `https://api.frankfurter.app`
- Data: European Central Bank (ECB)
- Update: Daily at ~16:00 CET
- Free: No authentication required
- Format: JSON

---

**Next Steps:**
- Learn about [Date and Time Calculations](date-time.md)
- Explore [Advanced Math Functions](advanced-math.md)
- Check [Settings Reference](../reference/settings.md)
