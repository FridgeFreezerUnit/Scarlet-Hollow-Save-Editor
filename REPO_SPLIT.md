# 🔧 Repository Split Guide

## Overview

The Scarlet Hollow Enhanced Save Editor has been split into **two separate repositories** for clarity and ease of use:

### 1. **Scarlet Hollow Save Editor**
📍 Repository: `Scarlet-Hollow-Save-Editor`
- Browser-based save file editor
- No installation required
- Modify traits, relationships, names
- Reset cheater flags

**Users:** Anyone with a `.save` file

**Launch:** Download `save-editor-enhanced.html` and open in browser

### 2. **Scarlet Hollow CheatBypass Tool**
📍 Repository: `Scarlet-Hollow-CheatBypass`
- Python command-line tool
- Patches game source code
- Allows unlimited traits without cheater flag
- Includes interactive installers for Windows/Linux/macOS

**Users:** Players who want to select 3+ traits before starting

**Launch:** Run `install_anticheat.bat` (Windows) or `./install_anticheat.sh` (Linux/macOS)

---

## Directory Structure

```
GitHub Organization (FridgeFreezerUnit)
│
├── Scarlet-Hollow-Save-Editor/
│   ├── save-editor-enhanced.html      ← Main editor tool
│   ├── README.md                      ← Full documentation
│   ├── LICENSE
│   ├── CONTRIBUTING.md
│   ├── CODE_OF_CONDUCT.md
│   ├── SECURITY.md
│   ├── PROJECT_STRUCTURE.md
│   ├── CHANGELOG.md
│   ├── .gitignore
│   ├── .gitattributes
│   ├── saves/                         ← Example saves
│   └── .github/
│       ├── ISSUE_TEMPLATE/
│       │   ├── bug_report.md
│       │   ├── feature_request.md
│       │   └── config.yml
│       └── pull_request_template.md
│
├── Scarlet-Hollow-CheatBypass/
│   ├── install_anticheat.bat          ← Windows installer
│   ├── install_anticheat.sh           ← Linux/macOS installer
│   ├── cheat_bypass.py                ← Main patching tool
│   ├── deploy_mod_enhanced.py         ← Repacking helper
│   ├── extract_scripts.py             ← Script extractor
│   ├── find_anti_cheat.py             ← Anti-cheat finder
│   ├── debug_archive.py               ← Debug utility
│   ├── README.md                      ← Full documentation
│   ├── QUICKSTART.md                  ← Quick reference
│   ├── LICENSE
│   ├── CONTRIBUTING.md
│   ├── SECURITY.md
│   ├── .gitignore
│   ├── .gitattributes
│   └── .github/
│       ├── ISSUE_TEMPLATE/
│       │   ├── bug_report.md
│       │   └── config.yml
│       └── pull_request_template.md
```

---

## When to Use Which Tool

### Use **Save Editor** for:
- ✅ Changing traits in an existing save
- ✅ Editing character relationships
- ✅ Changing your character's name
- ✅ Resetting cheater flags from old saves
- ✅ Quick GUI without command-line
- ✅ Cross-platform (works in any browser)

**Good for:** Modifying saves mid-game or for existing saves

### Use **CheatBypass** for:
- ✅ Starting a NEW game with 3+ traits
- ✅ Preventing cheater flag entirely
- ✅ Game source code patching
- ✅ Permanent trait count removal
- ✅ Advanced users comfortable with command-line

**Good for:** Setting up game before first play

### Use **BOTH** for Maximum Power:
1. **CheatBypass:** Patch game before starting new game → select unlimited traits
2. **Save Editor:** Modify save while playing → edit relationships and names

---

## File Locations

### Save Editor Repository Files
- **Main editor:** `save-editor-enhanced.html`
- **Full docs:** `README.md`
- **Contributions:** `CONTRIBUTING.md`
- **Issues:** `.github/ISSUE_TEMPLATE/`
- **Examples:** `saves/` (example save files)

### CheatBypass Repository Files  
- **Windows installer:** `install_anticheat.bat`
- **Linux/macOS installer:** `install_anticheat.sh`
- **Core tool:** `cheat_bypass.py`
- **Full docs:** `README.md`
- **Quick start:** `QUICKSTART.md`
- **Helper tools:** `*.py` files in repo

---

## Installation Instructions

### Save Editor
1. Go to [Scarlet-Hollow-Save-Editor](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor)
2. Download `save-editor-enhanced.html`
3. Double-click the file
4. Done!

### CheatBypass
1. Go to [Scarlet-Hollow-CheatBypass](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass)
2. **Windows:** Download and run `install_anticheat.bat`
3. **Linux/macOS:** Clone repo and run `./install_anticheat.sh`
4. Follow the interactive prompts

---

## Cross-Repository References

### From Save Editor README
- Links to [CheatBypass](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass) for game patching
- Explains relationship between the two tools
- Recommends CheatBypass for unlimited traits

### From CheatBypass README
- Links to [Save Editor](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor) for save modification
- Shows when to use each tool
- Recommends combining both tools

---

## Development Workflow

### For Save Editor Contributions
```bash
git clone https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor.git
cd Scarlet-Hollow-Save-Editor
# Edit save-editor-enhanced.html, README.md, etc.
git commit -m "Your changes"
git push
```

### For CheatBypass Contributions
```bash
git clone https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass.git
cd Scarlet-Hollow-CheatBypass
# Edit Python files, documentation, installers
git commit -m "Your changes"
git push
```

---

## Documentation Standards

Both repositories maintain:
- ✅ Comprehensive README.md with full documentation
- ✅ CONTRIBUTING.md for contributors
- ✅ LICENSE (MIT with disclaimer)
- ✅ SECURITY.md for vulnerability reporting
- ✅ .github/ISSUE_TEMPLATE/ for bug/feature reporting
- ✅ CODE_OF_CONDUCT.md (in Save Editor repo, links in CheatBypass)
- ✅ Cross-references between repositories

---

## Version Tracking

### Save Editor Versioning
```
v2.0.0 - Relationships editor, name editor
v1.0.0 - Initial release with traits editor
```

See `CHANGELOG.md` in Save Editor repo

### CheatBypass Versioning
```
v1.0.0 - Initial release with installer scripts
```

See `README.md` in CheatBypass repo

---

## FAQ About the Split

**Q: Why are they separate?**
A: Cleaner organization, easier maintenance, independent versioning, users only download what they need.

**Q: Can I use just one?**
A: Yes! Each works independently:
- Save Editor works alone for modifying existing saves
- CheatBypass works alone for patching game before playing

**Q: Do they work together?**
A: Yes! Better together:
1. CheatBypass patches the game
2. Save Editor modifies saves while playing

**Q: Which should I use first?**
A: Depends on your situation:
- **Existing save?** → Use Save Editor
- **Starting new game?** → Use CheatBypass first, then Save Editor while playing

**Q: What if I only want the save editor?**
A: Download `save-editor-enhanced.html` from Save Editor repo, that's it!

**Q: What if I only want the cheat bypass?**
A: Clone CheatBypass repo, follow the installer, you're good!

---

## Support & Contributions

### For Save Editor Issues
→ [Save Editor Issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues)

### For CheatBypass Issues
→ [CheatBypass Issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass/issues)

### For Questions
→ [Discussions](https://github.com/FridgeFreezerUnit/) (check both repos)

### To Contribute
→ See `CONTRIBUTING.md` in each repository

---

## Related Links

- **Scarlet Hollow:** [Black Tabby Games](https://www.scarlethollow.com)
- **Itch.io:** [Play the game](https://blacktabbygames.itch.io/scarlet-hollow)
- **Save Editor Repo:** [GitHub](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor)
- **CheatBypass Repo:** [GitHub](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass)

---

**Last Updated:** May 2026
