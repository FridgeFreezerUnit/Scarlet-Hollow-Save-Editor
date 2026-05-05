# Contributing to Scarlett Hollow Enhanced Save Editor

Thank you for your interest in contributing! This document explains how to help make this project better.

## Ways to Contribute

### 1. Report Bugs 🐛

Found something broken?

1. Check [existing issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues) to avoid duplicates
2. [Create a new issue](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues/new) with:
   - Clear title describing the problem
   - Steps to reproduce the issue
   - Expected vs actual behavior
   - Screenshots/console errors (press F12 to open browser console)
   - Browser and OS information

### 2. Suggest Features 💡

Have an idea to make the editor better?

1. Check [discussions](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/discussions) and [issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues)
2. [Open an issue](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues/new) with label `enhancement`
3. Describe:
   - What feature you want
   - Why it would be useful
   - How you imagine it working

### 3. Improve Documentation 📚

Found a typo? Confusing explanation? Help us improve!

- Edit markdown files directly in GitHub (click the pencil icon)
- Or fork, make changes, and submit a pull request

### 4. Submit Code 💻

Want to code a feature or fix?

#### Setup

1. **Fork the repository** on GitHub
2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR-USERNAME/Scarlet-Hollow-Save-Editor.git
   cd Scarlet-Hollow-Save-Editor
   ```
3. **Create a branch** for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```

#### Make Changes

- Edit `save-editor-enhanced.html` for main editor features
- Edit `CheatBypass/cheat_bypass.py` for game patching features
- Update `README.md` or create `docs/` files for documentation
- Test thoroughly before submitting!

#### Testing

1. **Backup a save file** from your Scarlett Hollow installation
2. **Load it in the editor** and test your changes
3. **Verify the modified save** still works in the game
4. **Check the browser console** (F12) for any JavaScript errors

#### Submit Pull Request

1. **Commit your changes** with clear messages:
   ```bash
   git add .
   git commit -m "Add feature: description of what you did"
   ```
2. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```
3. **Create a Pull Request** on GitHub:
   - Title: Clear description of changes
   - Description: Why you made this change, any notes for reviewers
   - Link any related issues: `Fixes #123`

## Code Style Guidelines

### HTML/CSS/JavaScript

- Use **2-space indentation** (not tabs)
- Keep lines under 100 characters where reasonable
- Add **comments** for complex logic
- Use **meaningful variable names** (not `x`, `temp`, etc.)
- Format strings clearly:
  ```javascript
  // Good
  const message = `Player: ${playerName}, Traits: ${traitCount}`;
  
  // Avoid
  let m = p + " " + t;
  ```

### Python

- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guide
- Use 4-space indentation
- Add docstrings to functions
- Keep functions focused and short
- Use meaningful names:
  ```python
  # Good
  def find_and_patch_files(directory):
      """Search for anti-cheat code and apply patches."""
      
  # Avoid
  def fp(d):
      # search and patch
  ```

### Documentation

- Write clearly for **non-technical users**
- Explain **why**, not just **what**
- Include examples when helpful
- Link to related sections
- Use proper Markdown formatting

## Testing Checklist

Before submitting a pull request, test:

- ✅ **Load/save works** with real save files
- ✅ **No JavaScript errors** (check F12 console)
- ✅ **Traits are detected correctly** 
- ✅ **Modifications persist** after download
- ✅ **Game loads modified save** without issues
- ✅ **Works offline** (no network requests)
- ✅ **Different browsers** (Chrome, Firefox, Safari if possible)

## Questions?

- **Questions about contributing?** → [Open a discussion](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/discussions)
- **Need to talk privately?** → Check project for contact info
- **Not sure if your idea fits?** → Open an issue or discussion first!

---

## Recognition

All contributors will be:
- Credited in [README.md](./README.md)
- Listed in [VERSION HISTORY](./README.md#-version-history)
- Thanked in commit messages

We appreciate your help making this tool better for everyone! 🙏
