# Changelog

All notable changes to Calcify are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned Features

- Hexadecimal and binary number conversion
- Custom function definitions
- Plotting and graphing capabilities
- Plugin system for extensions
- Mobile/tablet companion app
- Cloud sync for settings and files
- More language translations
- Scientific calculator mode
- Matrix operations
- Complex number support

---

## [1.2.0] - 2024-12-15

### Added

- Currency conversion with real-time exchange rates
- Support for 30+ international currencies
- Frankfurter API integration for exchange rates
- Auto-update exchange rates (configurable interval)
- Manual rate refresh option in settings
- Date and time calculations
- `today`, `now` keywords for current date/time
- Date arithmetic (add/subtract days, months, years)
- Date difference calculations
- Performance mode for slower systems
- Backup and restore settings feature
- Export/import calculations to JSON
- Command palette (`Ctrl + Shift + P`)

### Changed

- Improved calculation engine performance (30% faster)
- Updated AvalonEdit to version 6.1.3.50
- Refined dark theme colors for better contrast
- Optimized memory usage for large files
- Enhanced auto-complete suggestions
- Better error messages for invalid expressions

### Fixed

- Fixed division by zero crash
- Corrected temperature conversion formulas
- Fixed auto-save not working for untitled files
- Resolved memory leak in syntax highlighter
- Fixed theme not applying on startup
- Corrected time zone handling in date calculations
- Fixed crash when opening corrupted files

---

## [1.1.5] - 2024-09-20

### Added

- Angle unit selection (degrees/radians/gradians)
- Hyperbolic trigonometric functions (sinh, cosh, tanh)
- Statistical functions (median, mode, variance)
- Drag and drop file support
- Recent files list (up to 20 files)
- Print preview feature
- Copy result shortcut (`Ctrl + Shift + C`)

### Changed

- Improved syntax highlighting performance
- Updated UI icons to modern style
- Enhanced autocomplete speed
- Better keyboard shortcut organization

### Fixed

- Fixed logarithm domain errors
- Corrected square root of negative numbers error
- Fixed autocomplete not showing for some functions
- Resolved crash when printing empty document
- Fixed settings window not closing properly

---

## [1.1.0] - 2024-06-10

### Added

- Unit conversion system
- Support for length, weight, temperature conversions
- Data size conversions (KB, MB, GB, TB)
- Time conversions (seconds, minutes, hours, etc.)
- Angle conversions (degrees, radians)
- Frequency conversions (Hz, kHz, MHz, GHz)
- Auto-save functionality
- Configurable auto-save interval
- Syntax highlighting for calculations
- Dark theme support
- Theme toggle button in toolbar
- Line numbering option
- Word wrap toggle

### Changed

- Improved parser for better expression handling
- Enhanced error reporting with line numbers
- Refined UI layout and spacing
- Updated About dialog with license info

### Fixed

- Fixed crash on very long expressions
- Corrected operator precedence issues
- Fixed parentheses matching errors
- Resolved file association problems on Windows 11
- Fixed UI scaling on high DPI displays

---

## [1.0.5] - 2024-03-15

### Added

- Keyboard shortcuts reference (`Ctrl + K Ctrl + S`)
- Find and replace functionality
- Go to line feature (`Ctrl + G`)
- Duplicate line command (`Ctrl + D`)
- Delete line command (`Ctrl + L`)
- Block comment toggle

### Changed

- Improved responsiveness on slower computers
- Faster file loading for large documents
- Better memory management
- Updated .NET Framework to 4.8

### Fixed

- Fixed find next/previous bugs
- Corrected undo/redo stack issues
- Fixed cursor position after find/replace
- Resolved clipboard paste formatting issues

---

## [1.0.0] - 2024-01-01

### Initial Release

#### Features

- Basic arithmetic operations (+, -, *, /, ^, %)
- Mathematical functions (sin, cos, tan, sqrt, log, etc.)
- Variable support
- Multi-line calculations
- Save and load calculation files (.calc format)
- Syntax highlighting
- Light theme
- Settings window
- Auto-update checker
- Portable version available

#### Supported Platforms

- Windows 7 SP1 and later
- .NET Framework 4.5.2 or higher

#### Functions

- Trigonometry: sin, cos, tan, asin, acos, atan
- Logarithms: log, ln, log10
- Powers and roots: sqrt, cbrt, pow
- Rounding: round, floor, ceil
- Statistical: sum, avg, min, max
- Utility: abs, sign, factorial

---

## Version History Summary

| Version | Release Date | Major Features                              |
| ------- | ------------ | ------------------------------------------- |
| 1.2.0   | 2024-12-15   | Currency conversion, date/time calculations |
| 1.1.5   | 2024-09-20   | Advanced trig functions, statistics         |
| 1.1.0   | 2024-06-10   | Unit conversions, dark theme                |
| 1.0.5   | 2024-03-15   | Find/replace, keyboard shortcuts            |
| 1.0.0   | 2024-01-01   | Initial release                             |

---

## Legend

- **Added** - New features
- **Changed** - Changes to existing functionality
- **Deprecated** - Soon-to-be removed features
- **Removed** - Removed features
- **Fixed** - Bug fixes
- **Security** - Security vulnerability fixes

---

## Upgrading

### From 1.1.x to 1.2.0

- All settings are preserved
- Currency conversion requires internet connection
- New date/time features available immediately
- Performance mode improves speed on older systems

### From 1.0.x to 1.1.0

- Settings are migrated automatically
- Theme preference is preserved
- Unit conversion syntax: `value unit to unit`
- All previous calculations remain compatible

---

## Deprecation Notice

None currently. All features are actively supported.

---

## Known Issues

### Version 1.2.0

- Currency conversion may be slow on first run (fetching rates)
- Very large date ranges (>1000 years) may have precision issues
- Performance mode disables some visual effects

### Version 1.1.5

- Hyperbolic functions use radians regardless of angle setting
- Print preview may be slow for documents >100 pages

---

## Future Plans

### Version 1.3.0 (Planned Q2 2025)

- Hex/binary number support
- Bitwise operations
- Custom function definitions
- Multi-cursor editing
- Code folding
- Mini-map view
- Complete UI redesign
- Plugin system
- Mobile companion app (?)
- Matrix operations
- Complex number support

---

## Contributing

Want to help shape the future of Calcify?

- **Report bugs:** [GitHub Issues](https://github.com/ToniF03/Calcify/issues)
- **Suggest features:** [Feature Requests](https://github.com/ToniF03/Calcify/issues/new?template=feature_request.md)
- **Submit code:** See [Contributing Guide](../development/contributing.md)
- **Join discussion:** [Discord Community](https://discord.gg/MfHHgYtWub)

---

## Links

- **GitHub:** https://github.com/ToniF03/Calcify
- **Homepage:** https://tonif03.github.io/prod/calcify
- **Releases:** https://github.com/ToniF03/Calcify/releases
- **Documentation:** https://github.com/ToniF03/Calcify/tree/master/docs

---

**Note:** This changelog is generated for documentation purposes. Actual release dates and version numbers may vary based on the real project status.
