# Frequently Asked Questions (FAQ)

Common questions and answers about Calcify.

## General Questions

### What is Calcify?

Calcify is a powerful calculator application for Windows that goes beyond basic arithmetic. It supports:
- Mathematical expressions and functions
- Unit conversions (length, weight, temperature, etc.)
- Currency conversion with live exchange rates
- Date and time calculations
- Variables and multi-line calculations

---

### Is Calcify free?

Yes, Calcify is completely free and open-source under the MIT License.

---

### What operating systems does Calcify support?

Calcify runs on Windows 7 or later, including:
- Windows 7, 8, 8.1, 10, 11
- Windows Server 2008 R2 and later

Calcify does not currently support macOS or Linux.

---

### How is Calcify different from the Windows Calculator?

Calcify offers several advantages:
- **Text-based interface** - Type calculations like in a text editor
- **Multi-line calculations** - Work on multiple problems at once
- **Variables** - Store and reuse values
- **Unit conversions** - Built into expressions
- **File support** - Save and load your calculations
- **Extensible** - Open-source, can be customized

---

## Installation & Setup

### Do I need administrator rights to install Calcify?

Yes, the installer requires administrator privileges. However, you can use the portable version without admin rights.

---

### Can I install Calcify on a USB drive?

Yes! Download the portable version, which doesn't require installation. Just extract to your USB drive and run `Calcify.exe`.

---

### How do I uninstall Calcify?

**Windows Settings:**
1. Open Settings (`Win + I`)
2. Go to Apps → Apps & features
3. Find Calcify and click Uninstall

**Control Panel:**
1. Open Control Panel
2. Programs → Programs and Features
3. Right-click Calcify → Uninstall

---

### Can I have multiple versions installed?

No, installing a new version will replace the previous one. However, you can use the portable version alongside an installed version.

---

## Using Calcify

### How do I save my calculations?

Press `Ctrl + S` or click File → Save. Calcify saves files in `.calc` format (which is just plain text).

---

### Can I open my old calculator files?

Yes, Calcify can open:
- `.calc` files (native format)
- `.txt` files (plain text)
- Any text-based format

Simply drag and drop or use File → Open.

---

### How do I insert comments?

Use `//` for single-line comments:

```
// This is a comment
10 + 5    // This calculates 15
```

---

### Can I use variables?

Yes! Simply assign values:

```
x = 10
y = 20
result = x + y    // 30
```

---

### How do I convert units?

Use the `to` keyword:

```
10 km to miles
100 pounds to kg
25 °C to °F
```

See [Unit Conversions Guide](../features/unit-conversions.md) for all supported units.

---

### How often are currency exchange rates updated?

By default, rates update every 3 hours. You can change this in Settings → Calculations → Currency Update Frequency, or manually update via Settings.

---

### Can I use Calcify offline?

Yes! All features work offline except:
- Currency conversions (uses last fetched rates)
- Automatic update checks

---

### How do I change the theme?

**Method 1:** Click the theme toggle button (🌓) in the toolbar

**Method 2:** Settings → Appearance → Theme

**Method 3:** Press `Ctrl + T`

---

### Can I change the font size?

Yes, in Settings → Appearance → Font Size, or use:
- `Ctrl + +` to zoom in
- `Ctrl + -` to zoom out
- `Ctrl + 0` to reset

---

### How do I print my calculations?

Press `Ctrl + P` or File → Print. You can preview before printing.

---

## Features

### What mathematical functions are supported?

Calcify supports:
- **Basic:** +, -, *, /, ^, %
- **Trigonometry:** sin, cos, tan, asin, acos, atan
- **Logarithms:** log, ln, log2
- **Powers/Roots:** sqrt, cbrt, pow
- **Rounding:** round, floor, ceil
- **Statistical:** avg, median, stdev
- **More:** abs, min, max, factorial

See [Math Functions Reference](../reference/math-functions.md) for complete list.

---

### Can I calculate with dates?

Yes! Calcify supports date arithmetic:

```
today + 30 days
2025-12-25 - today
now + 2 hours
```

See [Date and Time Guide](../features/date-time.md).

---

### What currencies are supported?

Calcify supports 30+ major currencies including:
- USD, EUR, GBP, JPY, CHF
- CAD, AUD, NZD, CNY, INR
- And many more!

See [Currency Conversion Guide](../features/currency-conversion.md).

---

### Can I do hexadecimal or binary conversions?

Currently, Calcify focuses on decimal numbers. Hex/binary support may be added in future versions.

---

### Does Calcify support custom functions?

Not yet, but this is planned for a future release. Follow the project on GitHub for updates.

---

## Troubleshooting

### Calcify won't start

**Try these steps:**

1. **Restart your computer**
2. **Check .NET Framework** - Ensure .NET 4.5.2+ is installed
3. **Run as Administrator** - Right-click → Run as administrator
4. **Reinstall** - Uninstall and reinstall Calcify
5. **Check compatibility** - Right-click Calcify.exe → Properties → Compatibility → Run in Windows 7 mode

---

### Calculations give wrong results

**Check:**

1. **Order of operations** - Use parentheses to clarify: `(10 + 5) * 2`
2. **Decimal places** - Increase in Settings if needed
3. **Units** - Ensure you're using correct unit names
4. **Syntax** - Check for typos in expressions

---

### Currency conversions don't work

**Solutions:**

1. **Check internet connection** - Required for first update
2. **Update rates manually** - Settings → Update Exchange Rates Now
3. **Check rate age** - Settings shows when rates were last updated
4. **Firewall** - Ensure Calcify can access `api.frankfurter.app`

---

### Files won't save

**Solutions:**

1. **Check permissions** - Ensure you can write to the location
2. **Try different location** - Save to Documents instead
3. **Check disk space** - Ensure sufficient free space
4. **Run as administrator** - May help with permission issues

---

### Syntax highlighting doesn't work

**Solutions:**

1. **Restart Calcify**
2. **Reset settings** - Settings → Advanced → Reset All Settings
3. **Reinstall** - May fix corrupted files

---

### Theme won't change

**Solutions:**

1. **Restart Calcify** after changing theme
2. **Check Windows theme** - If using "System" theme
3. **Reset settings** - Try resetting to defaults

---

## Performance

### Calcify is slow

**Try these:**

1. **Disable auto-calculate** - Settings → Calculations → Auto-Calculate
2. **Reduce history** - Settings → Advanced → Maximum History
3. **Performance mode** - Settings → Advanced → Performance Mode
4. **Close other programs** - Free up system resources

---

### Large files are slow to open

This is normal for very large files (>1 MB). Consider:
- Splitting into smaller files
- Disabling syntax highlighting for large files
- Using Performance Mode

---

## Updates

### How do I update Calcify?

Calcify checks for updates automatically on startup. When available:
1. A notification appears
2. Click "Download Update"
3. Update installs automatically
4. Restart Calcify

**Manual update:**
- Help → Check for Updates
- Or download from [GitHub Releases](https://github.com/ToniF03/Calcify/releases)

---

### Will I lose my settings when updating?

No, settings are preserved across updates.

---

### Can I disable update checks?

Yes, in Settings → General → Check for Updates → Never

However, we recommend keeping automatic updates enabled for bug fixes and new features.

---

## Data & Privacy

### Where are my settings stored?

Settings are stored in:
```
%APPDATA%\Calcify\settings.json
```

You can backup this file to preserve your settings.

---

### Does Calcify collect my data?

Calcify may collect anonymous usage statistics if enabled (opt-in). This includes:
- Which features are used
- Crash reports
- Performance metrics

**No personal data or calculation content is collected.**

Disable in Settings → Privacy → Send Anonymous Usage Data

---

### Where are auto-backups saved?

Auto-backups are stored in:
```
%APPDATA%\Calcify\Backups\
```

Configure in Settings → Backup and Restore

---

## Contributing

### How can I contribute?

See our [Contributing Guide](../development/contributing.md) for:
- Reporting bugs
- Suggesting features
- Submitting code
- Improving documentation

---

### I found a bug. Where do I report it?

Report bugs on [GitHub Issues](https://github.com/ToniF03/Calcify/issues) with:
- Description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable
- Your Windows and Calcify versions

---

### Can I request a feature?

Absolutely! Open a feature request on [GitHub Issues](https://github.com/ToniF03/Calcify/issues) and describe:
- What problem it solves
- How it should work
- Why others would benefit

---

## Licensing

### What license is Calcify under?

Calcify is licensed under the [MIT License](https://opensource.org/licenses/MIT), which allows:
- ✅ Commercial use
- ✅ Modification
- ✅ Distribution
- ✅ Private use

---

### Can I use Calcify in my business?

Yes! The MIT License permits commercial use without restrictions.

---

### Can I modify and redistribute Calcify?

Yes, under the MIT License you can modify and redistribute, provided you include the original license and copyright notice.

---

## Support

### Where can I get help?

- **Documentation:** [Read the docs](../README.md)
- **Discord:** [Join our community](https://discord.gg/MfHHgYtWub)
- **GitHub Issues:** [Report problems](https://github.com/ToniF03/Calcify/issues)
- **Email:** Contact the maintainer

---

### Is there a user manual?

Yes! This documentation serves as the complete user manual. Start with:
- [Quick Start Guide](../quick-start.md)
- [User Interface Guide](../user-interface.md)
- [Features Overview](../features/basic-calculations.md)

---

## Still have questions?

- Check the [Troubleshooting Guide](troubleshooting.md)
- Visit our [Discord community](https://discord.gg/MfHHgYtWub)
- [Open an issue](https://github.com/ToniF03/Calcify/issues) on GitHub

---

**Last Updated:** November 2025
