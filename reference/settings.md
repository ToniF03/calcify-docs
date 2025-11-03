# Settings Reference

Complete guide to all settings and configuration options in Calcify.

## Accessing Settings

- **Keyboard:** Press `Ctrl + ,`
- **Menu:** Click **File** → **Settings**
- **Toolbar:** Click the ⚙️ (gear) icon

## General Settings

### Auto-Save

**Description:** Automatically save files at regular intervals

**Options:**

- Enabled / Disabled

**Default:** Enabled

**Note:** Prevents data loss from crashes or power failures

---

### Auto-Save Interval

**Description:** How often to auto-save (when enabled)

**Options:**

- 1 minute
- 2 minutes
- 5 minutes (default)
- 10 minutes
- 15 minutes

**Default:** 5 minutes

---

### Check for Updates

**Description:** Automatically check for new versions

**Options:**

- On Startup (default)
- Daily
- Weekly
- Never

**Default:** On Startup

---

### Recent Files Count

**Description:** Number of recent files to remember

**Options:** 0-20

**Default:** 10

---

## Appearance Settings

### Theme

**Description:** Color scheme for the interface

**Options:**

- Light - White background, dark text
- Dark - Dark background, light text
- System - Follow Windows theme

**Default:** System

**Shortcut:** `Ctrl + T` to toggle

---

### Font Size

**Description:** Text size in the editor

**Range:** 8-32 points

**Default:** 12 pt

**Shortcuts:**

- `Ctrl + +` to increase
- `Ctrl + -` to decrease
- `Ctrl + 0` to reset

---

### Line Height

**Description:** Spacing between lines

**Options:**

- Compact (1.0)
- Normal (1.2) - default
- Comfortable (1.5)
- Spacious (2.0)

**Default:** Normal (1.2)

---

### Show Line Numbers

**Description:** Display line numbers in the margin

**Options:** Enabled / Disabled

**Default:** Enabled

---

### Highlight Current Line

**Description:** Highlight the line containing the cursor

**Options:** Enabled / Disabled

**Default:** Enabled

---

### Show Whitespace

**Description:** Display spaces and tabs with visible characters

**Options:** Enabled / Disabled

**Default:** Disabled

**Note:** Useful for debugging indentation issues

---

### Bracket Matching

**Description:** Highlight matching brackets/parentheses

**Options:** Enabled / Disabled

**Default:** Enabled

---

## Editor Settings

### Tab Size

**Description:** Number of spaces per tab character

**Options:**

- 2 spaces
- 4 spaces (default)
- 8 spaces

**Default:** 4 spaces

---

### Insert Spaces

**Description:** Insert spaces instead of tab characters

**Options:** Enabled / Disabled

**Default:** Enabled

**Note:** Recommended for consistency across editors

---

### Auto-Close Brackets

**Description:** Automatically insert closing bracket/parenthesis

**Options:** Enabled / Disabled

**Default:** Enabled

**Example:** Type `(` and `)` is inserted automatically

---

### Auto-Complete

**Description:** Show suggestions while typing

**Options:**

- Enabled (default)
- Disabled

**Default:** Enabled

**Trigger:** Automatic or `Ctrl + Space`

---

### Auto-Complete Delay

**Description:** Delay before showing suggestions

**Options:** 0-1000 milliseconds

**Default:** 300 ms

---

### Syntax Highlighting

**Description:** Color-code different elements

**Options:** Enabled / Disabled

**Default:** Enabled

**Note:** Improves readability

---

## Calculation Settings

### Decimal Places

**Description:** Number of decimal places in results

**Options:** 0-10

**Default:** 2

**Examples:**

- 0 decimal places: `3`
- 2 decimal places: `3.14`
- 5 decimal places: `3.14159`

---

### Use Thousands Separator

**Description:** Add commas to large numbers

**Options:** Enabled / Disabled

**Default:** Enabled

**Examples:**

- Enabled: `1,000,000`
- Disabled: `1000000`

---

### Thousands Separator

**Description:** Character used as thousands separator

**Options:**

- Comma (,) - default for US/UK
- Period (.) - default for Europe
- Space ( ) - international standard

**Default:** Comma (,)

---

### Decimal Separator

**Description:** Character used as decimal point

**Options:**

- Period (.) - default for US/UK
- Comma (,) - default for Europe

**Default:** Period (.)

---

### Angle Unit

**Description:** Default unit for trigonometric functions

**Options:**

- Degrees (default)
- Radians
- Gradians

**Default:** Degrees

---

### Default Currency

**Description:** Base currency for conversions

**Options:** Any supported currency (USD, EUR, GBP, etc.)

**Default:** USD

---

### Currency Update Frequency

**Description:** How often to fetch exchange rates

**Options:**

- 1 hour
- 3 hours (default)
- 6 hours
- 12 hours
- 24 hours
- Manual only

**Default:** 3 hours

---

### Update Exchange Rates Now

**Description:** Manually fetch latest rates

**Action:** Button to force update

---

### Auto-Calculate

**Description:** Calculate results as you type

**Options:** Enabled / Disabled

**Default:** Enabled

**Note:** Disable for large documents to improve performance

---

## Advanced Settings

### Maximum History

**Description:** Number of undo/redo operations to remember

**Options:** 10-1000

**Default:** 100

---

### Clear Recent Files

**Description:** Remove all recent files from history

**Action:** Button to clear

---

### Reset All Settings

**Description:** Restore all settings to defaults

**Action:** Button to reset

**Warning:** Cannot be undone

---

## File Associations

### Associate .calc Files

**Description:** Open .calc files with Calcify by default

**Options:** Enabled / Disabled

**Default:** Enabled (during installation)

---

## Backup and Restore

### Auto-Backup Location

**Description:** Folder for automatic backups

**Default:** `%APPDATA%\Calcify\Backups`

**Action:** Button to browse and change

---

### Backup Frequency

**Description:** How often to create backups

**Options:**

- Every save
- Hourly
- Daily (default)
- Weekly
- Never

**Default:** Daily

---

## Privacy Settings

### Check for Updates Automatically

**Description:** Allow automatic update checks

**Options:** Enabled / Disabled

**Default:** Enabled

---

## Keyboard Shortcuts

### View All Shortcuts

**Action:** Opens keyboard shortcuts reference

---

## Import/Export Settings

### Export Settings

**Description:** Save current settings to a file

**Action:** Button to export

**File Format:** `.json`

**Use Case:** Backup or transfer settings to another computer

---

### Import Settings

**Description:** Load settings from a file

**Action:** Button to import

**Warning:** Overwrites current settings

---

## Configuration File

Settings are stored in:

**Location:** `%APPDATA%\Calcify\settings.json`

**Format:** JSON

**Example:**

```json
{
  "theme": "dark",
  "fontSize": 12,
  "decimalPlaces": 2,
  "autoSave": true,
  "autoSaveInterval": 5
}
```

**Note:** You can manually edit this file while Calcify is closed

---

## Best Practices

1. **Enable Auto-Save** - Prevent data loss
2. **Choose Comfortable Font Size** - Reduce eye strain
3. **Use Dark Theme in Low Light** - Better for extended use
4. **Set Appropriate Decimal Places** - Match your needs
5. **Enable Auto-Complete** - Speed up workflow
6. **Regular Backups** - Export settings periodically
7. **Update Exchange Rates** - Keep currency conversions current

---

## Troubleshooting Settings

### Settings Not Saving

**Problem:** Changes don't persist

**Solutions:**

1. Check file permissions on `%APPDATA%\Calcify`
2. Run as Administrator
3. Delete `settings.json` and restart (resets to defaults)

---

### Settings Corrupted

**Problem:** Error loading settings

**Solutions:**

1. Reset to defaults via Settings
2. Delete `settings.json` file
3. Restore from backup

---

### Missing Options

**Problem:** Some settings not visible

**Solutions:**

1. Update to latest version
2. Check if running in compatibility mode
3. Ensure not in limited user account

---

**See Also:**

- [Keyboard Shortcuts](keyboard-shortcuts.md)
- [User Interface Guide](../user-interface.md)
- [Troubleshooting](../help/troubleshooting.md)
