# Contributing to Calcify

Thank you for your interest in contributing to Calcify! This guide will help you get started.

## Ways to Contribute

### 1. Report Bugs

Found a bug? Help us fix it!

**Before Reporting:**
- Check [existing issues](https://github.com/ToniF03/Calcify/issues)
- Try with the latest version
- Verify it's reproducible

**How to Report:**
1. Go to [GitHub Issues](https://github.com/ToniF03/Calcify/issues)
2. Click **New Issue**
3. Select **Bug Report** template
4. Fill in all sections:
   - Description of the bug
   - Steps to reproduce
   - Expected behavior
   - Actual behavior
   - Screenshots (if applicable)
   - System information (Windows version, Calcify version)

**Example Bug Report:**
```markdown
## Bug Description
Currency conversion returns incorrect results

## Steps to Reproduce
1. Type: 100 USD to EUR
2. Press Enter

## Expected Behavior
Should show ~92 EUR (current rate)

## Actual Behavior
Shows 0 EUR

## Environment
- Calcify Version: 1.2.3
- Windows Version: Windows 10 21H2
- .NET Version: 4.8
```

---

### 2. Suggest Features

Have an idea to improve Calcify?

**Before Suggesting:**
- Check [existing feature requests](https://github.com/ToniF03/Calcify/issues?q=is%3Aissue+label%3Aenhancement)
- Ensure it aligns with Calcify's purpose
- Consider if others would benefit

**How to Suggest:**
1. Go to [GitHub Issues](https://github.com/ToniF03/Calcify/issues)
2. Click **New Issue**
3. Select **Feature Request** template
4. Describe:
   - The problem it solves
   - Proposed solution
   - Alternative solutions considered
   - Additional context

**Example Feature Request:**
```markdown
## Feature Description
Add support for hexadecimal/binary number conversions

## Problem
Users working with programming often need to convert between number bases

## Proposed Solution
Implement functions like:
- hex(255) → 0xFF
- bin(10) → 0b1010
- dec(0xFF) → 255

## Use Case
Developers, computer science students, embedded programmers

## Priority
Low to Medium
```

---

### 3. Improve Documentation

Documentation is always welcome!

**What to Document:**
- Fix typos and errors
- Add examples
- Clarify confusing sections
- Translate to other languages
- Add tutorials

**How to Contribute:**
1. Fork the repository
2. Edit files in `docs/` folder
3. Submit a pull request

---

### 4. Submit Code

Want to contribute code? Great!

## Getting Started

### Fork and Clone

1. **Fork** the repository on GitHub
2. **Clone** your fork:
   ```powershell
   git clone https://github.com/YOUR-USERNAME/Calcify.git
   cd Calcify
   ```

3. **Add upstream remote:**
   ```powershell
   git remote add upstream https://github.com/ToniF03/Calcify.git
   ```

### Create a Branch

Always create a new branch for your work:

```powershell
# Update main branch
git checkout master
git pull upstream master

# Create feature branch
git checkout -b feature/your-feature-name

# Or for bug fixes
git checkout -b fix/bug-description
```

**Branch Naming:**
- `feature/feature-name` - New features
- `fix/bug-description` - Bug fixes
- `docs/what-changed` - Documentation
- `refactor/what-changed` - Code refactoring
- `test/what-added` - Adding tests

### Make Changes

1. **Follow coding standards** (see below)
2. **Test your changes** thoroughly
3. **Update documentation** if needed
4. **Add comments** to complex code

### Commit Changes

Write clear commit messages:

```powershell
git add .
git commit -m "Add feature: hex/binary conversion support"
```

**Commit Message Format:**
```
<type>: <short summary>

<detailed description>

Fixes #<issue-number>
```

**Types:**
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Formatting (no code change)
- `refactor:` Code restructuring
- `test:` Adding tests
- `chore:` Maintenance

**Example:**
```
feat: Add hexadecimal number conversion

Implement hex(), bin(), and dec() functions for number base conversion.
Users can now convert between decimal, hexadecimal, and binary.

Fixes #123
```

### Push Changes

```powershell
git push origin feature/your-feature-name
```

### Create Pull Request

1. Go to your fork on GitHub
2. Click **Compare & pull request**
3. Fill in the PR template:
   - Description of changes
   - Related issues
   - Testing performed
   - Screenshots (if UI changes)
4. Click **Create pull request**

## Code Standards

### C# Coding Style

Follow Microsoft C# coding conventions:

**Naming Conventions:**
```csharp
// Classes: PascalCase
public class CalculationEngine { }

// Methods: PascalCase
public void CalculateResult() { }

// Properties: PascalCase
public string ResultText { get; set; }

// Private fields: camelCase with underscore
private string _internalValue;

// Parameters: camelCase
public void SetValue(string newValue) { }

// Local variables: camelCase
string localVariable = "value";

// Constants: PascalCase
public const int MaxValue = 100;
```

**Formatting:**
```csharp
// Braces on new line (Allman style)
if (condition)
{
    DoSomething();
}

// Indentation: 4 spaces (not tabs)
public class Example
{
    public void Method()
    {
        if (true)
        {
            Console.WriteLine("Indented");
        }
    }
}

// Spacing
int x = 5;  // Space around operators
Method(a, b);  // Space after commas
```

**Comments:**
```csharp
/// <summary>
/// Calculate the sum of two numbers
/// </summary>
/// <param name="a">First number</param>
/// <param name="b">Second number</param>
/// <returns>Sum of a and b</returns>
public int Add(int a, int b)
{
    return a + b;
}

// Single-line comment for brief explanation

/* Multi-line comment
   for longer explanations
   that span multiple lines */
```

### XAML Style

```xml
<!-- Formatting -->
<Window x:Class="Calcify.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        Title="Calcify">
    
    <Grid>
        <TextBox Name="EditorTextBox"
                 FontFamily="Consolas"
                 FontSize="12"
                 Background="White" />
    </Grid>
</Window>
```

### Best Practices

1. **Keep it simple** - Don't over-engineer
2. **Single responsibility** - One function, one purpose
3. **DRY** - Don't Repeat Yourself
4. **Meaningful names** - Self-documenting code
5. **Error handling** - Handle exceptions gracefully
6. **Performance** - Avoid unnecessary operations
7. **Comments** - Explain "why", not "what"

## Testing

### Manual Testing

Before submitting:

1. **Build in Release mode** - Ensure no warnings
2. **Test all affected features** - Verify functionality
3. **Test edge cases** - Empty inputs, large numbers, etc.
4. **Test on clean install** - Fresh Windows VM if possible
5. **Check UI** - No visual glitches
6. **Test keyboard shortcuts** - All shortcuts work

### Test Checklist

- [ ] Code compiles without errors
- [ ] Code compiles without warnings
- [ ] Feature works as expected
- [ ] No regressions (old features still work)
- [ ] UI is responsive
- [ ] No performance issues
- [ ] Documentation updated
- [ ] Comments added to complex code

## Pull Request Guidelines

### PR Template

```markdown
## Description
Brief description of changes

## Related Issue
Fixes #123

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring

## Testing
Describe testing performed:
- Test case 1
- Test case 2

## Screenshots
(if applicable)

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review performed
- [ ] Comments added to complex code
- [ ] Documentation updated
- [ ] No new warnings
- [ ] Tested locally
```

### Review Process

1. **Automated checks** - CI builds and tests
2. **Code review** - Maintainer reviews code
3. **Feedback** - Address any comments
4. **Approval** - Once approved, will be merged
5. **Merge** - Maintainer merges to main branch

## Community Guidelines

### Be Respectful

- Be kind and courteous
- Accept constructive criticism
- Focus on the code, not the person
- Assume good intentions

### Be Patient

- Maintainers are volunteers
- Reviews take time
- Be willing to iterate

### Be Helpful

- Help other contributors
- Answer questions in issues
- Share knowledge

## Recognition

Contributors are credited in:
- CONTRIBUTORS.md file
- Release notes
- About dialog in application

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Questions?

- **Discord:** [Join our community](https://discord.gg/MfHHgYtWub)
- **Email:** [Contact maintainer](mailto:contact@example.com)
- **Issues:** [Ask on GitHub](https://github.com/ToniF03/Calcify/issues)

---

**Thank you for contributing to Calcify! 🎉**
