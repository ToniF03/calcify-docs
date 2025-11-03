# Troubleshooting Guide

Solutions to common problems and errors in Calcify.

## Installation Issues

### Windows SmartScreen Warning

**Problem:** "Windows protected your PC" message when installing

**Cause:** Unsigned executable triggers Windows SmartScreen

**Solution:**
1. Click **More info**
2. Click **Run anyway**
3. This is safe - Calcify is open-source and verified

**Prevention:**
- Download only from official sources (GitHub releases)
- Verify file hash if concerned

---

### .NET Framework Error

**Problem:** Error message about missing .NET Framework

**Full Error:** "This application requires .NET Framework 4.5.2 or higher"

**Solution:**
1. Check installed version:
   - Press `Win + R`
   - Type `regedit`
   - Navigate to: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`
   - Check "Release" value
2. If missing or outdated:
   - Download [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework)
   - Install and restart computer

---

### Installation Fails Mid-Process

**Problem:** Installer stops or crashes during installation

**Solutions:**

**1. Run as Administrator**
- Right-click installer
- Select "Run as administrator"

**2. Free up disk space**
- Ensure at least 100 MB free on C: drive
- Clear temporary files

**3. Disable antivirus temporarily**
- Some antivirus programs block installation
- Re-enable after installation

**4. Check Windows Installer service**
- Press `Win + R`
- Type `services.msc`
- Find "Windows Installer"
- Ensure it's running

**5. Try portable version**
- Download portable ZIP instead
- No installation required

---

### Can't Uninstall Previous Version

**Problem:** Error when trying to uninstall old version

**Solution:**

**Method 1: Windows Settings**
```
Settings → Apps → Apps & features → Calcify → Uninstall
```

**Method 2: Use Microsoft Troubleshooter**
1. Download [Microsoft Program Install/Uninstall Troubleshooter](https://support.microsoft.com/en-us/windows/fix-problems-that-block-programs-from-being-installed-or-removed-cca7d1b6-65a9-3d98-426b-e9f927e1eb4d)
2. Run and follow prompts

**Method 3: Manual removal**
1. Delete installation folder: `C:\Program Files\Calcify`
2. Delete appdata: `%APPDATA%\Calcify`
3. Remove registry entries (advanced users only)

---

## Startup Issues

### Application Won't Start

**Problem:** Double-clicking Calcify.exe does nothing

**Diagnostic Steps:**

**1. Check if running**
- Press `Ctrl + Shift + Esc` (Task Manager)
- Look for `Calcify.exe` in Processes
- If found, end task and try again

**2. Check Windows Event Viewer**
- Press `Win + R`, type `eventvwr`
- Navigate to: Windows Logs → Application
- Look for Calcify errors

**3. Run from command line**
```powershell
cd "C:\Program Files\Calcify"
.\Calcify.exe
```
- Note any error messages

**Solutions:**

**Missing DLL:**
```
Error: Could not load file or assembly 'AvalonEdit'
```
Solution: Reinstall Calcify

**Access Denied:**
```
Error: Access to path denied
```
Solution: Run as administrator

**Corrupted installation:**
- Uninstall completely
- Delete `C:\Program Files\Calcify`
- Delete `%APPDATA%\Calcify`
- Reinstall

---

### Crashes on Startup

**Problem:** Calcify opens briefly then crashes

**Common Causes:**

**1. Corrupted settings**

Solution:
```powershell
# Rename settings file
cd %APPDATA%\Calcify
ren settings.json settings.json.backup
```
Restart Calcify (will use defaults)

**2. Corrupted auto-save file**

Solution:
```powershell
cd %APPDATA%\Calcify
del autosave.calc
```

**3. Incompatible display driver**

Solution:
- Update graphics drivers
- Try compatibility mode:
  - Right-click Calcify.exe
  - Properties → Compatibility
  - Check "Run in compatibility mode for Windows 7"

---

### "Side-by-side configuration error"

**Problem:** Error about side-by-side configuration

**Full Error:** "The application has failed to start because its side-by-side configuration is incorrect"

**Solution:**
1. Install [Visual C++ Redistributables](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads)
2. Install both x86 and x64 versions
3. Restart computer

---

## Calculation Issues

### Wrong Results

**Problem:** Calculations give unexpected results

**Common Mistakes:**

**1. Order of operations**
```
Wrong:  10 + 5 * 2 = 30  ❌
Actual: 10 + 5 * 2 = 20  ✓  (multiplication first)
Fix:    (10 + 5) * 2 = 30  ✓
```

**2. Integer division**
```
Problem: 5 / 2 = 2  ❌  (should be 2.5)
```
Solution: Ensure decimal places setting > 0

**3. Floating-point precision**
```
Problem: 0.1 + 0.2 = 0.30000000000000004
```
Solution: Increase decimal places or use round()

**4. Angle units**
```
Problem: sin(90) returns wrong value
```
Solution: Check Settings → Angle Unit (Degrees vs Radians)

---

### Division by Zero

**Problem:** Error when dividing by zero

**Error Message:** "Cannot divide by zero"

**Example:**
```
10 / 0      →  Error
10 / (5-5)  →  Error
```

**Prevention:**
- Check denominators
- Use if-then logic (when supported)

---

### Syntax Errors

**Problem:** "Invalid expression" or "Syntax error"

**Common Causes:**

**1. Mismatched parentheses**
```
Wrong: (10 + 5 * 2
Right: (10 + 5) * 2
```

**2. Double operators**
```
Wrong: 10 ++ 5
Right: 10 + 5
```

**3. Missing operand**
```
Wrong: 10 +
Right: 10 + 5
```

**4. Invalid characters**
```
Wrong: 10 $ 5
Right: 10 * 5
```

---

### Function Not Recognized

**Problem:** "Unknown function" error

**Check:**
1. Function name spelling: `sqrt` not `squareroot`
2. Function exists: See [Math Functions](../reference/math-functions.md)
3. Correct syntax: `sqrt(16)` not `sqrt 16`

---

## Unit Conversion Issues

### Unit Not Recognized

**Problem:** "Unknown unit" error

**Solutions:**

**1. Check spelling**
```
Wrong: kilometers
Right: kilometer, km
```

**2. Check aliases**
- See [Supported Units](../reference/supported-units.md)
- Most units have multiple names

**3. Check case**
- Units are case-insensitive
- `KM`, `km`, `Km` all work

---

### Incompatible Units

**Problem:** "Cannot convert between these units"

**Example:**
```
10 km to kg  →  Error (length to weight)
```

**Solution:**
- Ensure units are same type (length to length, weight to weight)
- See [Unit Conversions](../features/unit-conversions.md) for compatible units

---

### "to" Keyword Missing

**Problem:** Conversion doesn't work

**Wrong:**
```
10 km miles  →  Error
```

**Right:**
```
10 km to miles  →  6.21 miles
```

Always include `to` between units.

---

## Currency Conversion Issues

### Exchange Rates Not Updating

**Problem:** Currency conversions use old rates

**Solutions:**

**1. Check internet connection**
- Ensure you're connected
- Try accessing https://api.frankfurter.app in browser

**2. Manual update**
- Settings → Calculations → Update Exchange Rates Now

**3. Check firewall**
- Ensure Calcify can access internet
- Whitelist `api.frankfurter.app`

**4. Check update time**
- Settings shows when rates were last fetched
- Default update interval: 3 hours

---

### Currency Code Not Recognized

**Problem:** "Unknown currency" error

**Solution:**
- Use 3-letter ISO codes: USD, EUR, GBP, JPY
- See [Currency Conversion](../features/currency-conversion.md) for supported currencies
- Check spelling

---

### Offline Currency Conversions

**Problem:** Can't convert currencies offline

**Explanation:**
- First conversion requires internet
- After that, cached rates are used
- Rates update when online

**Status:**
- Settings shows rate age
- Warning if rates are outdated

---

## File Issues

### Can't Open File

**Problem:** Error opening .calc or .txt file

**Solutions:**

**1. File in use**
- Close file in other programs
- Close duplicate Calcify windows

**2. Permission denied**
- Check file permissions
- Move to Documents folder
- Try running Calcify as administrator

**3. Corrupted file**
- Open in Notepad to verify it's readable
- Try copying content to new file

**4. Unsupported format**
- Calcify opens text-based files only
- Convert binary files to text first

---

### Can't Save File

**Problem:** Error when saving

**Solutions:**

**1. Permission denied**
```
Error: Access to path denied
```
- Try saving to Documents folder
- Run as administrator
- Check file isn't read-only

**2. Disk full**
- Free up disk space
- Save to different drive

**3. Invalid filename**
```
Wrong: file*.calc  (asterisk not allowed)
Right: file.calc
```

**4. Path too long**
- Windows limits paths to 260 characters
- Use shorter file/folder names
- Save closer to root (C:\Calculations)

---

### Auto-Save Not Working

**Problem:** Files don't auto-save

**Check:**

**1. Auto-save enabled**
- Settings → General → Auto-Save (should be checked)

**2. Check interval**
- Settings → General → Auto-Save Interval
- Default: 5 minutes

**3. Check save location**
- Settings → Backup and Restore → Auto-Backup Location
- Ensure folder exists and is writable

**4. File must be saved once manually**
- Auto-save only works for previously saved files
- New files must be manually saved first

---

## Performance Issues

### Slow Performance

**Problem:** Calcify is sluggish or unresponsive

**Solutions:**

**1. Disable auto-calculate**
- Settings → Calculations → Auto-Calculate → Off
- Manually calculate with F5

**2. Reduce history**
- Settings → Advanced → Maximum History → Lower value
- Restart Calcify

**3. Close large files**
- Files >1 MB can be slow
- Split into smaller files

**4. Performance mode**
- Settings → Advanced → Performance Mode → On
- Disables animations and effects

**5. Update graphics drivers**
- WPF uses GPU acceleration
- Outdated drivers can cause slowness

**6. Check system resources**
- Close other programs
- Check Task Manager for high CPU/RAM usage

---

### High Memory Usage

**Problem:** Calcify uses excessive RAM

**Normal Usage:** 50-150 MB

**High Usage Causes:**

**1. Large files**
- Each character uses memory
- Consider splitting large files

**2. Long history**
- Reduce in Settings → Advanced → Maximum History

**3. Memory leak (bug)**
- Report on GitHub with:
  - Memory usage (from Task Manager)
  - How long Calcify was running
  - What operations were performed

---

### Freezing/Hanging

**Problem:** Calcify stops responding

**Immediate Fix:**
- Press `Ctrl + S` if possible (may save)
- Force close: Task Manager → End Task

**Prevention:**

**1. Avoid infinite loops**
```
Don't: recursive calculations without exit
```

**2. Calculation timeout**
- Settings → Advanced → Calculation Timeout
- Prevents infinite calculations

**3. Save frequently**
- Enable auto-save
- Manually save with Ctrl + S

---

## Display Issues

### Blurry Text

**Problem:** Text appears fuzzy or blurry

**Cause:** DPI scaling on high-resolution displays

**Solution:**

**1. Disable DPI scaling**
- Right-click Calcify.exe
- Properties → Compatibility
- Check "Override high DPI scaling"
- Select "Application"

**2. Adjust Windows scaling**
- Settings → System → Display
- Change scaling to 100% (may make UI small)

**3. Use different font**
- Settings → Appearance → Font Family
- Try different monospace fonts

---

### UI Elements Not Visible

**Problem:** Buttons, menus missing or cut off

**Solutions:**

**1. Increase window size**
- Drag window edges
- Maximize window

**2. Reset window position**
```powershell
# Delete window state file
cd %APPDATA%\Calcify
del windowstate.json
```

**3. Check resolution**
- Minimum: 1024x768
- Recommended: 1920x1080

**4. Check monitor scaling**
- May clip UI at >150% scaling
- Reduce to 125% or 100%

---

### Theme Not Applying

**Problem:** Theme doesn't change or looks wrong

**Solutions:**

**1. Restart Calcify**
- Theme changes may require restart

**2. Reset settings**
- Settings → Advanced → Reset All Settings

**3. Check Windows theme**
- If using "System" theme in Calcify
- Follows Windows light/dark mode

**4. Corrupted theme file**
- Reinstall Calcify

---

## Settings Issues

### Settings Not Saving

**Problem:** Changes revert after restarting

**Solutions:**

**1. Click Save/OK**
- Ensure you click Save button
- Don't just close Settings window

**2. File permissions**
- Settings file: `%APPDATA%\Calcify\settings.json`
- Ensure folder is writable
- Try running as administrator

**3. Settings file corrupted**
```powershell
cd %APPDATA%\Calcify
del settings.json
```
Restart Calcify (creates new settings)

---

### Can't Access Settings

**Problem:** Settings window won't open

**Solutions:**

**1. Try keyboard shortcut**
- Press `Ctrl + ,`

**2. Corrupted settings**
- Delete `%APPDATA%\Calcify\settings.json`
- Restart Calcify

**3. Reinstall**
- Uninstall Calcify
- Reinstall fresh copy

---

## Update Issues

### Update Check Fails

**Problem:** "Cannot check for updates" error

**Solutions:**

**1. Check internet connection**
- Ensure connected
- Try accessing https://github.com in browser

**2. Firewall blocking**
- Allow Calcify through firewall
- Whitelist GitHub domains

**3. Disable update check**
- Settings → General → Check for Updates → Never

**4. Manual update**
- Download latest from [GitHub Releases](https://github.com/ToniF03/Calcify/releases)

---

### Update Fails to Install

**Problem:** Update downloads but won't install

**Solutions:**

**1. Run as administrator**
- Close Calcify
- Run update as administrator

**2. Antivirus blocking**
- Temporarily disable antivirus
- Re-enable after update

**3. Manual update**
- Download installer from GitHub
- Uninstall old version
- Install new version

---

## Getting Help

If these solutions don't help:

1. **Check GitHub Issues**
   - [Open Issues](https://github.com/ToniF03/Calcify/issues)
   - Someone may have same problem

2. **Discord Community**
   - [Join Discord](https://discord.gg/MfHHgYtWub)
   - Ask for help

3. **Report Bug**
   - [Create new issue](https://github.com/ToniF03/Calcify/issues/new)
   - Include:
     - Error message
     - Steps to reproduce
     - Windows version
     - Calcify version
     - Screenshots

4. **Check Logs**
   - Location: `%APPDATA%\Calcify\logs\`
   - Include in bug report

---

**See Also:**
- [FAQ](faq.md) - Common questions
- [User Guide](../user-interface.md) - How to use Calcify
- [GitHub Issues](https://github.com/ToniF03/Calcify/issues) - Report problems
