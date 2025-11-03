# Building from Source

Learn how to compile Calcify yourself from the source code.

## Prerequisites

### Required Software

1. **Visual Studio 2019 or later**
   
   - Download: [Visual Studio Community](https://visualstudio.microsoft.com/downloads/)
   - Free for individual developers

2. **Components to Install:**
   
   - .NET desktop development workload
   - .NET Framework 4.5.2 SDK or higher
   - Windows SDK

3. **Optional Tools:**
   
   - Git (for cloning the repository)
   - WiX Toolset (for creating installer)

### System Requirements

- **OS:** Windows 7 or later
- **RAM:** 4 GB minimum, 8 GB recommended
- **Disk Space:** 10 GB free space
- **.NET Framework:** 4.5.2 or higher

## Getting the Source Code

### Option 1: Clone with Git

```powershell
git clone https://github.com/ToniF03/Calcify.git
cd Calcify
```

### Option 2: Download ZIP

1. Go to [GitHub repository](https://github.com/ToniF03/Calcify)
2. Click **Code** → **Download ZIP**
3. Extract the ZIP file
4. Navigate to the extracted folder

## Project Structure

```
Calcify/
├── Calcify.sln              # Visual Studio solution
├── Calcify/                 # Main application project
│   ├── MainWindow.xaml      # Main window UI
│   ├── MainWindow.xaml.cs   # Main window code
│   ├── App.xaml             # Application entry point
│   ├── Classes/             # Utility classes
│   └── Resources/           # Images, icons, etc.
├── Update/                  # Auto-updater project
├── setup/                   # Installer project (WiX)
└── packages/                # NuGet packages
```

## Building with Visual Studio

### Step 1: Open the Solution

1. Open **Visual Studio**
2. Click **File** → **Open** → **Project/Solution**
3. Navigate to `Calcify.sln`
4. Click **Open**

### Step 2: Restore NuGet Packages

1. Right-click the solution in **Solution Explorer**
2. Select **Restore NuGet Packages**
3. Wait for packages to download

**Required Packages:**

- AvalonEdit 6.1.3.50
- Newtonsoft.Json 13.0.1
- Microsoft.UI.Xaml 2.7.0

### Step 3: Select Build Configuration

**Debug Configuration:**

- For development and testing
- Includes debug symbols
- No optimizations

**Release Configuration:**

- For production builds
- Optimized code
- Smaller file size

**To Select:**

1. Click dropdown at top (shows "Debug" or "Release")
2. Select desired configuration

### Step 4: Build the Project

**Method 1: Menu**

- Click **Build** → **Build Solution** (`Ctrl + Shift + B`)

**Method 2: Keyboard**

- Press `F6` or `Ctrl + Shift + B`

**Method 3: Right-click**

- Right-click solution in Solution Explorer
- Select **Build**

### Step 5: Run the Application

**Debug Mode:**

- Press `F5` to start with debugging
- Or click **Debug** → **Start Debugging**

**Release Mode:**

- Press `Ctrl + F5` to start without debugging
- Or click **Debug** → **Start Without Debugging**

## Build Output

After successful build, the executable is located at:

**Debug:**

```
Calcify\bin\Debug\Calcify.exe
```

**Release:**

```
Calcify\bin\Release\Calcify.exe
```

## Building from Command Line

### Using MSBuild

**Prerequisites:**

- Visual Studio Developer Command Prompt
- Or MSBuild in PATH

**Commands:**

```powershell
# Navigate to solution directory
cd C:\path\to\Calcify

# Restore NuGet packages
nuget restore Calcify.sln

# Build Debug configuration
msbuild Calcify.sln /p:Configuration=Debug

# Build Release configuration
msbuild Calcify.sln /p:Configuration=Release

# Clean build
msbuild Calcify.sln /t:Clean /p:Configuration=Release
msbuild Calcify.sln /t:Build /p:Configuration=Release
```

### Using PowerShell Script

Create `build.ps1`:

```powershell
# Restore packages
& nuget restore Calcify.sln

# Build solution
& msbuild Calcify.sln /p:Configuration=Release /p:Platform="Any CPU" /v:minimal

# Check if build succeeded
if ($LASTEXITCODE -eq 0) {
    Write-Host "Build succeeded!" -ForegroundColor Green
    Write-Host "Output: Calcify\bin\Release\Calcify.exe"
} else {
    Write-Host "Build failed!" -ForegroundColor Red
    exit 1
}
```

Run with:

```powershell
.\build.ps1
```

## Creating an Installer

### Prerequisites

Install **WiX Toolset:**

1. Download from [WiX Toolset website](https://wixtoolset.org/)
2. Install WiX v3.11 or later
3. Restart Visual Studio

### Build Installer

1. Open `setup\setup.wixproj` in Visual Studio
2. Build the **Release** configuration first
3. Right-click `setup` project
4. Select **Build**

**Output:**

```
setup\bin\Debug\Calcify-Setup.msi
```

### Installer Customization

Edit `setup\Product.wxs` to customize:

- Installation directory
- Start menu shortcuts
- File associations
- Registry entries

## Troubleshooting Build Issues

### Missing NuGet Packages

**Problem:** Build fails with "package not found" errors

**Solution:**

```powershell
# Clear NuGet cache
nuget locals all -clear

# Restore packages
nuget restore Calcify.sln
```

---

### AvalonEdit Error

**Problem:** `Could not load file or assembly 'AvalonEdit'`

**Solution:**

1. Right-click solution → **Manage NuGet Packages**
2. Reinstall AvalonEdit package
3. Rebuild solution

---

### XAML Build Errors

**Problem:** Errors in `.xaml` files

**Solution:**

1. Clean solution: **Build** → **Clean Solution**
2. Close Visual Studio
3. Delete `bin` and `obj` folders
4. Reopen solution and rebuild

---

### .NET Framework Error

**Problem:** `The reference assemblies for framework ".NETFramework,Version=v4.5.2" were not found`

**Solution:**

1. Install .NET Framework 4.5.2 Developer Pack
2. Or change target framework in project properties

---

### MSBuild Not Found

**Problem:** `'msbuild' is not recognized`

**Solution:**

- Use Visual Studio Developer Command Prompt

- Or add MSBuild to PATH:
  
  ```
  C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\MSBuild\Current\Bin
  ```

---

## Development Tips

### Hot Reload

1. Make code changes while debugging
2. Press `Ctrl + Shift + F5` to restart
3. Or use **Edit and Continue** feature

### Debug Symbols

Include `.pdb` files for stack traces:

- Automatically generated in Debug mode
- Enable in Release: Project Properties → Build → Advanced → Debug Info

### Code Analysis

Enable static analysis:

1. Project Properties → Code Analysis
2. Select ruleset
3. Build to see warnings

### Performance Profiling

1. **Debug** → **Performance Profiler**
2. Select CPU Usage
3. Click **Start**
4. Use application
5. Stop and analyze results

## Continuous Integration

### GitHub Actions Example

Create `.github/workflows/build.yml`:

```yaml
name: Build Calcify

on: [push, pull_request]

jobs:
  build:
    runs-on: windows-latest

    steps:
    - uses: actions/checkout@v2

    - name: Setup MSBuild
      uses: microsoft/setup-msbuild@v1

    - name: Setup NuGet
      uses: NuGet/setup-nuget@v1

    - name: Restore packages
      run: nuget restore Calcify.sln

    - name: Build solution
      run: msbuild Calcify.sln /p:Configuration=Release

    - name: Upload artifact
      uses: actions/upload-artifact@v2
      with:
        name: Calcify-Build
        path: Calcify/bin/Release/
```

## Contributing Your Build

After successfully building:

1. Test thoroughly on your system
2. Check for warnings in build output
3. Run in Debug mode to catch issues
4. Submit pull request if fixing bugs

See [Contributing Guide](contributing.md) for details.

## Advanced Build Options

### Custom Build Configuration

Create new configuration:

1. **Build** → **Configuration Manager**
2. Click **Active solution configuration** → **New**
3. Name it (e.g., "Debug-x64")
4. Copy settings from existing configuration

### Conditional Compilation

Use preprocessor directives:

```csharp
#if DEBUG
    Console.WriteLine("Debug mode");
#elif RELEASE
    Console.WriteLine("Release mode");
#endif
```

### Post-Build Events

Automate tasks after build:

1. Project Properties → Build Events
2. Add commands to **Post-build event**

Example:

```batch
xcopy "$(TargetDir)*.*" "C:\Deploy\" /Y
```

---

**See Also:**

- [Contributing Guide](contributing.md)
- [Architecture Overview](architecture.md)
- [API Reference](api-reference.md)
