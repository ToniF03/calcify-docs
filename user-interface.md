# User Interface Guide

Learn about Calcify's clean and intuitive interface.

## Overview

Calcify features a minimal, distraction-free design that puts your calculations front and center.

## Main Components

### 1. Menu Bar

Located at the top of the window with the following menus:

#### File Menu

- **New** (`Ctrl + N`) - Create a new calculation file
- **Open** (`Ctrl + O`) - Open an existing file
- **Save** (`Ctrl + S`) - Save current file
- **Save As** (`Ctrl + Shift + S`) - Save with a new name
- **Recent Files** - Quick access to recently opened files
- **Exit** (`Alt + F4`) - Close Calcify

#### Edit Menu

- **Undo** (`Ctrl + Z`) - Undo last action
- **Redo** (`Ctrl + Y`) - Redo last undone action
- **Cut** (`Ctrl + X`) - Cut selected text
- **Copy** (`Ctrl + C`) - Copy selected text
- **Paste** (`Ctrl + V`) - Paste from clipboard
- **Select All** (`Ctrl + A`) - Select all text
- **Find** (`Ctrl + F`) - Find text
- **Replace** (`Ctrl + H`) - Find and replace

#### View Menu

- **Theme** - Switch between Light and Dark themes
- **Font Size** - Adjust editor font size
- **Line Numbers** - Toggle line number display
- **Word Wrap** - Toggle word wrapping
- **Zoom In** (`Ctrl + +`) - Increase zoom
- **Zoom Out** (`Ctrl + -`) - Decrease zoom
- **Reset Zoom** (`Ctrl + 0`) - Reset to 100%

#### Help Menu

- **Documentation** (`F1`) - Open this documentation
- **Keyboard Shortcuts** - View all shortcuts
- **Check for Updates** - Check for new versions
- **About Calcify** - Version and license information

### 2. Toolbar

Quick access buttons for common actions:

| Icon | Action   | Shortcut   |
| ---- | -------- | ---------- |
| 📄   | New file | `Ctrl + N` |
| 💾   | Save     | `Ctrl + S` |
| 📂   | Open     | `Ctrl + O` |
| ✂️   | Cut      | `Ctrl + X` |
| 📋   | Copy     | `Ctrl + C` |
| 📄   | Paste    | `Ctrl + V` |
| ↩️   | Undo     | `Ctrl + Z` |
| ↪️   | Redo     | `Ctrl + Y` |
| 🔍   | Find     | `Ctrl + F` |
| ⚙️   | Settings | `Ctrl + ,` |

### 3. Editor Area

The main text editor where you write your calculations:

#### Features

- **Syntax Highlighting** - Different colors for numbers, operators, and keywords
- **Auto-Completion** - Suggestions for functions and units
- **Line Numbers** - Optional line numbering on the left
- **Real-time Results** - Calculations update as you type
- **Multi-line Support** - Work with multiple calculations at once

#### Editor Behavior

- Click anywhere to position the cursor
- Double-click to select a word
- Triple-click to select a line
- Drag to select multiple lines
- Right-click for context menu

### 4. Status Bar

Located at the bottom, showing:

- **Line Number** - Current line position (`Ln: X`)
- **Column Number** - Current column position (`Col: X`)
- **Status** - Current state (Ready, Calculating, Saving, etc.)
- **Encoding** - File encoding (usually UTF-8)
- **File Status** - Modified indicator (asterisk * if unsaved)

## Working with Files

### Creating a New File

1. Click **File** → **New** (or press `Ctrl + N`)
2. Start typing your calculations
3. Save when ready with `Ctrl + S`

### Opening Files

**Method 1: Menu**

1. Click **File** → **Open** (or press `Ctrl + O`)
2. Browse to your file
3. Click **Open**

**Method 2: Drag and Drop**

1. Drag a file from Windows Explorer
2. Drop it onto the Calcify window
3. The file opens automatically

**Method 3: Recent Files**

1. Click **File** → **Recent Files**
2. Select from the list

### Saving Files

**Save Current File:**

- Press `Ctrl + S`
- File saves to current location

**Save As New File:**

- Press `Ctrl + Shift + S`
- Choose location and name
- Click **Save**

**Supported Formats:**

- `.calc` - Calcify native format (recommended)
- `.txt` - Plain text
- Any text-based format

### File Indicators

- **Clean File** - Title bar shows filename only
- **Modified File** - Asterisk (*) appears: `filename.calc*`

## Context Menu

Right-click in the editor for quick actions:

- **Undo** - Undo last action
- **Redo** - Redo last undone action
- **Cut** - Cut selected text
- **Copy** - Copy selected text
- **Paste** - Paste from clipboard
- **Delete** - Delete selected text
- **Select All** - Select all content

## Themes

Calcify offers two themes for comfortable viewing:

### Light Theme

- White background
- Dark text
- Ideal for bright environments
- Better for printing

### Dark Theme

- Dark background
- Light text
- Reduces eye strain in low light
- Popular for extended use

**Switching Themes:**

1. Click the theme toggle button (🌓) in the toolbar
2. Or go to **Settings** → **Theme**
3. Theme saves automatically for next session

## Settings Window

Access via **Settings** button or `Ctrl + ,`:

### General Settings

- **Language** - Interface language (currently English)
- **Auto-save** - Enable automatic saving
- **Auto-save interval** - How often to auto-save (minutes)
- **Check for updates** - Automatically check for new versions

### Appearance

- **Theme** - Light or Dark
- **Font Size** - Adjust text size (8-32pt)
- **Line Spacing** - Adjust line height
- **Show Line Numbers** - Toggle line numbers

### Editor

- **Tab Size** - Spaces per tab (2, 4, or 8)
- **Show Whitespace** - Display spaces and tabs
- **Highlight Current Line** - Highlight active line
- **Bracket Matching** - Highlight matching brackets

### Calculations

- **Decimal Places** - Result precision (0-10)
- **Use Thousands Separator** - Add commas to large numbers
- **Currency Update** - How often to fetch exchange rates

### Advanced

- **Debug Mode** - Show additional information
- **Clear Recent Files** - Clear recent files list
- **Reset Settings** - Restore default settings

## Keyboard Navigation

Navigate efficiently with the keyboard:

### Cursor Movement

- `←` `→` `↑` `↓` - Move one character/line
- `Ctrl + ←` `→` - Move by word
- `Home` - Start of line
- `End` - End of line
- `Ctrl + Home` - Start of document
- `Ctrl + End` - End of document
- `Page Up` / `Page Down` - Scroll by page

### Text Selection

- `Shift + Arrow keys` - Select text
- `Ctrl + Shift + Arrow` - Select by word
- `Shift + Home` / `End` - Select to line start/end
- `Ctrl + A` - Select all

### Editing

- `Ctrl + D` - Duplicate line
- `Ctrl + L` - Delete line
- `Tab` - Indent
- `Shift + Tab` - Unindent
- `Ctrl + /` - Toggle comment

## Window Controls

### Minimize, Maximize, Close

- Top-right corner has standard Windows controls
- Minimize hides to taskbar
- Maximize fills screen
- Close exits (prompts to save if modified)

### Resizing

- Drag window edges to resize
- Double-click title bar to maximize/restore
- Minimum size: 800x600 pixels

## Tips for Efficient Use

1. **Learn Shortcuts** - Memorize common keyboard shortcuts
2. **Use Themes** - Switch themes based on environment
3. **Auto-save** - Enable auto-save to prevent data loss
4. **Organize Files** - Keep calculation files organized
5. **Customize Settings** - Adjust font size and spacing for comfort
6. **Use Context Menu** - Right-click for quick actions
7. **Split View** - Use Windows Snap to view Calcify alongside other apps

## Accessibility

Calcify supports Windows accessibility features:

- **Screen Readers** - Compatible with NVDA and JAWS
- **High Contrast** - Respects Windows High Contrast mode
- **Keyboard Only** - Full functionality without mouse
- **Scalable Text** - Zoom up to 300% without loss of functionality

---

**Next:** Learn about [Basic Calculations](features/basic-calculations.md) or check out [Keyboard Shortcuts](reference/keyboard-shortcuts.md).
