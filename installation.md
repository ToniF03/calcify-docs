# Installation Guide

This guide will walk you through installing Calcify on your Windows system.

## System Requirements

### Minimum Requirements

- **Operating System**: Windows 7 or later
- **RAM**: 512 MB
- **Disk Space**: 50 MB
- **Display**: 1024x768 resolution or higher
- **.NET Framework**: 4.5 or higher (usually pre-installed on Windows 8+)

### Recommended Requirements

- **Operating System**: Windows 10/11
- **RAM**: 1 GB or more
- **Display**: 1920x1080 resolution or higher
- **.NET Framework**: 4.7 or higher

## Installation Steps

### Option 1: Install from Release (Recommended)

1. **Download the Installer**
   - Visit the [Releases page](https://github.com/ToniF03/Calcify/releases/latest)
   - Download the latest `Calcify-Setup.exe` or `Calcify-Setup.msi`

2. **Run the Installer**
   - Double-click the downloaded installer
   - If Windows SmartScreen appears, click "More info" → "Run anyway"

3. **Follow Installation Wizard**
   - Accept the license agreement
   - Choose installation directory (default: `C:\Program Files\Calcify`)
   - Select Start Menu folder
   - Click "Install"

4. **Launch Calcify**
   - Check "Launch Calcify" on the final screen
   - Or find Calcify in your Start Menu

### Option 2: Portable Version

1. **Download Portable ZIP**
   - Visit the [Releases page](https://github.com/ToniF03/Calcify/releases/latest)
   - Download `Calcify-Portable.zip`

2. **Extract Files**
   - Extract the ZIP file to your preferred location
   - No installation required

3. **Run Calcify**
   - Double-click `Calcify.exe` in the extracted folder
   - Create a desktop shortcut if desired

## Installing .NET Framework

If you don't have .NET Framework 4.5 or higher:

1. **Check Current Version**
   - Press `Win + R`
   - Type `regedit` and press Enter
   - Navigate to: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`
   - Check the "Release" value

2. **Download .NET Framework**
   - Visit [Microsoft .NET Framework Download](https://dotnet.microsoft.com/download/dotnet-framework)
   - Download .NET Framework 4.8 (latest version)
   - Run the installer
   - Restart your computer if prompted

## Updating Calcify

### Automatic Updates

Calcify checks for updates automatically on startup. When an update is available:

1. A notification will appear in the application
2. Click "Download Update"
3. The updater will download and install the new version
4. Restart Calcify when prompted

### Manual Update

1. Download the latest version from the [Releases page](https://github.com/ToniF03/Calcify/releases/latest)
2. Run the installer (it will update your existing installation)
3. Your settings and preferences will be preserved

## Uninstalling Calcify

### Using Windows Settings

1. Open Windows Settings (`Win + I`)
2. Go to "Apps" → "Apps & features"
3. Find "Calcify" in the list
4. Click "Uninstall"
5. Follow the prompts

### Using Control Panel

1. Open Control Panel
2. Go to "Programs" → "Programs and Features"
3. Find "Calcify" in the list
4. Right-click and select "Uninstall"
5. Follow the uninstall wizard

## Troubleshooting Installation

### Issue: .NET Framework Error

**Problem**: Error message about missing .NET Framework

**Solution**: Install .NET Framework 4.5 or higher (see section above)

### Issue: Windows SmartScreen Warning

**Problem**: "Windows protected your PC" warning

**Solution**: 
1. Click "More info"
2. Click "Run anyway"
3. This is a false positive due to unsigned executable

### Issue: Insufficient Permissions

**Problem**: "Access Denied" or "Administrator Required" error

**Solution**: Right-click the installer and select "Run as Administrator"

### Issue: Installation Fails

**Problem**: Installation process fails or stops

**Solution**:
1. Ensure you have at least 100 MB free disk space
2. Close all other programs
3. Disable antivirus temporarily
4. Try running the installer as Administrator

## Next Steps

After installation, check out:
- [Quick Start Guide](quick-start.md) - Get started with Calcify
- [User Interface](user-interface.md) - Learn the interface
- [Basic Calculations](features/basic-calculations.md) - Start calculating!

---

**Need help?** Join our [Discord community](https://discord.gg/MfHHgYtWub) or [open an issue](https://github.com/ToniF03/Calcify/issues).
