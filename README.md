# 🎮 Scarlett Hollow Enhanced Save Editor

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Maintained](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor)
![Type: Browser Tool](https://img.shields.io/badge/Type-Browser%20Tool-blue)

A **powerful, offline-first browser-based save editor** for the indie game **Scarlett Hollow** by Black Tabby Games. Modify your saves to customize traits, relationships, and game flags without leaving your browser.

> ⚠️ **This is an unofficial fan-made tool.** It is not affiliated with, endorsed by, or sponsored by Black Tabby Games.

**[➡️ Launch the Editor](https://FridgeFreezerUnit.github.io/Scarlet-Hollow-Save-Editor/)** | **[📖 Full Documentation](./README.md)**

---

## ✨ Features

### Core Functionality
- **✅ Trait Editor** — Toggle the 7 character traits freely (Mystical, Sincere, Pragmatic, Romantic, Rational, Emotional, Sensible)
- **✅ Relationship Editor** — View and edit relationship dimensions for all 9 characters (agreeable, adversarial, open, closed, bold, passive, reliable, unreliable, insightful, dull)
- **✅ Anti-Cheat Management** — Reset cheater flags to clean up saves marked by the game's anti-cheat system
- **✅ Smart Flag Reset** — Automatically clean up related story flags when you disable traits
- **✅ Player Name Editor** — Change your character's name across the entire save file

### Technical Features
- **🔒 100% Offline** — No external dependencies, CDNs, or internet connection required
- **📤 Drag-and-Drop** — Simply drag your `.save` file onto the editor
- **💾 Safe Downloads** — Generates modified saves as `-modified.save` files (keeps originals safe)
- **🔍 Advanced Debugging** — Console output shows exactly which game variables were found and modified
- **⚡ Fast & Responsive** — Runs entirely in your browser with no server upload

### Related Tools
- **🛡️ [CheatBypass Tool](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass)** — Standalone Python utility to patch the game's anti-cheat code before playing (see separate repository)

---

## 📖 Table of Contents

- [Quick Start](#-quick-start)
- [Detailed Usage](#-detailed-usage)
- [Installation & Setup](#-installation--setup)
- [Troubleshooting](#-troubleshooting)
- [About CheatBypass](#-about-cheatbypass-tool)
- [Technical Details](#-technical-details)
- [Support & Contact](#-support--contact)
- [Credits](#-credits)
- [License & Disclaimer](#-license--disclaimer)

---

## 🚀 Quick Start

### Step 1: Open the Editor
Download `save-editor-enhanced.html` and **double-click** to open in your browser.

*(No installation or server required!)*

### Step 2: Load Your Save
**Drag and drop** your `.save` file from your save folder onto the editor.

The file will load immediately — no upload to servers!

### Step 3: Make Changes
- **Traits Tab**: Toggle traits on/off, see related flags that will auto-reset
- **Relationships Tab**: View/edit character relationship dimensions, check special flags
- **Advanced Tab**: Change player name, reset cheater flags, view debug info

### Step 4: Download Modified Save
Click **"Download Modified Save"** to get your edited save as `original-modified.save`

Load this new file in the game and play!

---

## 📚 Detailed Usage

### Traits Tab

Shows all traits found in your save file. For each trait:
- **Toggle On/Off** — Enable or disable the trait
- **Original Badge** — Shows what the trait was originally set to
- **Related Flags** — Lists other game variables that depend on this trait
- **Auto-Cleanup** — When you disable a trait, related flags are automatically reset

**Why can't I create new traits?**
RenPy saves only store variables that have been initialized. If a trait was never selected in-game, it won't exist in the save data, and the editor can't create it from scratch. You can only modify traits that already exist in your save.

### Relationships Tab

**Two Modes:**

#### Read-Only Mode
- View all 9 characters with their 10 relationship dimensions
- Each dimension is scored 0-100
- Hover over dimension names for wiki tooltips explaining what they mean
- See special relationship flags (romance, trust, affection)

**Characters:**
- Stella ⭐, Tabitha 🌿, Oscar 📖, Kaneeka 🔬, Reese 🎨, Wayne 🔧, Duke 🐾, Avery ⚖️, Sybil 🌙

**Dimensions (5 Axes, 10 Total):**
1. **Agreeable ↔ Adversarial** — How much character likes you
2. **Open ↔ Closed** — How honest they are with you
3. **Bold ↔ Passive** — How assertive they act
4. **Reliable ↔ Unreliable** — How much you can depend on them
5. **Insightful ↔ Dull** — How perceptive they are

#### Edit Mode
- Toggle edit button to switch to editable mode
- Change any dimension value (0-100)
- Values are clamped automatically
- Click to apply changes

**Relationship Flags:**
Some characters have special boolean flags for romance, trust, or affection status. These are displayed below the dimensions if they exist in your save.

### Advanced Tab

#### Player Name Editor
Change your character's name across the entire save file. This updates both `store.player_name` and `store.save_name` simultaneously.

#### Cheater Flag Management
The game marks saves as "cheater" if you:
- Select more than 2 traits in Chapter 1
- This check happens at **runtime in the game engine**, not when loading the save

**What This Does:**
- Resets the `persistent.cheater` flag in your save
- Cleans up old saves that were marked
- Does NOT prevent future flags from being set (use CheatBypass tool for that)

**To prevent cheater flags entirely**, use the [CheatBypass Tool](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass) to patch the game itself.

#### Debug Info
- Save filename
- File size
- Number of traits found
- Pickle variable positions (for troubleshooting)

---

## 🛠️ Installation & Setup

### Quick Start (No Installation!)
1. Download `save-editor-enhanced.html`
2. Double-click the file
3. It opens in your default browser
4. Done! ✅

### If You Get a Browser Security Warning

You may see: `"Unsafe attempt to load URL file:///..."`

This is normal browser security. The editor works fine, but if you want to remove the warning, set up a local web server:

#### Option A: Python (Easiest)
1. Open Command Prompt/Terminal in the folder with the HTML file
2. **Python 3:** `python -m http.server 8000`
3. **Python 2:** `python -m SimpleHTTPServer 8000`
4. Open `http://localhost:8000` in your browser
5. Click the HTML file

#### Option B: VS Code Live Server
1. Install the "Live Server" extension in VS Code
2. Right-click the HTML file → "Open with Live Server"
3. Browser opens automatically at `http://localhost:5500`

#### Option C: Node.js
1. Install `http-server`: `npm install -g http-server`
2. In the folder: `http-server`
3. Open `http://localhost:8080`

**Note:** The editor works 100% offline either way. The warning is just browser security being cautious about `file://` URLs.

### Browser Compatibility

| Browser | Status |
|---------|--------|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| IE 11 | ❌ Not supported |

### Save File Locations

Where to find your Scarlet Hollow saves:

**Windows:**
```
C:\Users\[Your Username]\AppData\Roaming\RenPy\ScarletHollow\
```

**macOS:**
```
~/Library/RenPy/ScarletHollow/
```

**Linux:**
```
~/.renpy/ScarletHollow/
```

Save files are named like: `1-1-LT1.save`, `persistent`, `auto-1-LT1.save`, etc.

---

## 🐛 Troubleshooting

### "I get a browser security warning"
See [Installation & Setup](#-installation--setup) above. The tool works fine, but you can set up a local server to remove the warning.

### "The file won't load"
- Make sure it's a real `.save` file from Scarlet Hollow (not renamed)
- Try a different save file to test
- Check browser console (F12) for error messages

### "I don't see all 7 traits"
This is normal! RenPy saves only store variables that have been initialized in-game. If you never selected a trait in Chapter 1, it won't exist in the save. You can only edit traits that were already chosen.

### "Changes aren't showing up in the game"
- Make sure you're loading the `-modified.save` file, not the original
- The game loads saves at startup — restart the game completely
- Try a different save file to test

### "My save file is broken"
- Restore your original save file from backup
- Check that you're using the correct `-modified.save` file
- Try loading a different save to test if it's a game issue

### "I want to select more than 2 traits without cheater flag"
The save editor can't help with this — the game checks trait count at runtime, not in the save file. You need the [CheatBypass Tool](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass) to patch the game itself.

---

## 🛡️ About CheatBypass Tool

The CheatBypass Tool is a **separate project** for patching the game's source code to allow unlimited traits.

### Why Two Tools?

**Save Editor** (`save-editor-enhanced.html`):
- ✅ Fixes/modifies existing saves
- ✅ Changes trait selections, relationships, names
- ✅ Resets cheater flags in old saves
- ❌ Can't prevent in-game trait count checks

**CheatBypass Tool** (separate repository):
- ✅ Patches the game's source code before playing
- ✅ Allows selecting unlimited traits without cheater flag
- ✅ Prevents future trait count checks
- ❌ Requires Python and command-line use

### When Do I Need CheatBypass?

**Use CheatBypass if:**
- ✅ You want to select more than 2 traits
- ✅ You want to avoid the cheater flag entirely
- ✅ You're starting a new game

**Use Save Editor if:**
- ✅ You're fixing an existing save
- ✅ You want to edit relationships
- ✅ You want to change your character name
- ✅ You want a GUI without command-line

### Get CheatBypass

👉 **[Scarlet Hollow CheatBypass Tool](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-CheatBypass)**

Or see [CHEATBYPASS_SETUP.md](./CHEATBYPASS_SETUP.md) for integration guide.

---

## 🔧 Technical Details

### How It Works

1. **Read** — JavaScript's FileReader reads your `.save` file (which is a ZIP)
2. **Extract** — JSZip library extracts the `log` file (Python pickle data)
3. **Parse** — Binary parsing finds game variables using Python pickle opcodes
4. **Modify** — Changes are made to specific byte positions
5. **Rebuild** — ZIP is rebuilt with modified save data
6. **Download** — Browser downloads the new file

### What Gets Modified

The editor modifies these pickle variables in the `log` file:

- `store.selected_traits` (list of trait names)
- `store.player_name` (your character's name)
- `store.save_name` (display name in game)
- `persistent.cheater` (cheater flag)
- `persistent.relationships` (character dimensions as 10-value dicts)
- Related flags (romance_*_count, *_distrust, etc.)

### Supported Save Versions

| Game Version | Supported |
|-------------|-----------|
| Chapter 1 | ✅ Yes |
| Chapter 2 | ✅ Yes |
| Chapter 3 | ✅ Yes |
| Chapter 4 | ✅ Yes |
| Chapter 5 | ✅ Yes |
| Chapter 6+ | ✅ Likely (untested) |

*Note: Very old Chapter 1 saves may not have all variables. New game updates may add new variables we don't recognize yet.*

### Safety Features

- ✅ Original file never modified
- ✅ All changes preserved in console log
- ✅ Easy backup/restore via original file
- ✅ No external network calls
- ✅ No data collection
- ✅ No automatic updates

---

## 💬 Support & Contact

### Getting Help

**First, check:**
- [Troubleshooting](#-troubleshooting) section above
- [GitHub Issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues) — search for your problem

**Still stuck?**
- [GitHub Discussions](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/discussions) — ask questions
- [GitHub Issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues) — report bugs

### Report a Bug

1. Check [existing issues](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues)
2. Create new issue with:
   - What you were trying to do
   - What happened instead
   - Error messages from browser console (F12)
   - Your game version / chapter

### Feature Requests

Have an idea? [Open a discussion](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/discussions) or [GitHub issue](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues)

### Security Issues

**Do NOT open public issues for security problems.**

Email maintainers privately. See [SECURITY.md](./SECURITY.md).

---

## 🎨 About Scarlett Hollow

Scarlett Hollow is an indie psychological mystery game by **Black Tabby Games** with:
- Deep character relationships
- Branching story with multiple endings
- Puzzle-solving and exploration
- Beautiful art and atmospheric sound

**Support the creators:**
- 🎮 [Itch.io](https://blacktabbygames.itch.io/scarlet-hollow)
- 🐦 [Twitter](https://twitter.com/BlackTabbyGames)
- 🌐 [Official Site](https://www.scarlethollow.com)

---

## 🙏 Credits

### Development
- **Tool Author**: FridgeFreezerUnit
- **JSZip Library**: David Duponchel ([jszip.js.org](https://stuk.github.io/jszip/))

### Game Data
- Character information from Scarlett Hollow wiki
- Game mechanics from official wiki
- Relationship data verified against in-game values

### Community
- Thanks to everyone testing and providing feedback!
- Special thanks to Black Tabby Games for creating Scarlett Hollow

---

## 📄 License & Disclaimer

### License

This project is licensed under the **MIT License**. See [LICENSE](./LICENSE) file for details.

**TL;DR**: You can use, modify, and distribute this tool freely, as long as you include the original license and copyright notice.

### Disclaimer

**⚠️ IMPORTANT:**

This tool is **unofficial and fan-made**. It is:
- ❌ NOT affiliated with, endorsed by, or sponsored by Black Tabby Games
- ❌ NOT a Black Tabby Games official product
- ❌ Created independently by the community

**Your Responsibility:**
- ✅ Back up your save files before using this tool
- ✅ Keep your backups safe
- ✅ Test on a throwaway save first
- ✅ Understand that modifying saves is at your own risk
- ✅ Support Black Tabby Games by purchasing the game

**No Warranty:**
This tool is provided "as-is" without any warranty. Use at your own risk. The authors are not responsible for:
- Lost saves
- Corrupted files
- Game bugs or crashes
- Any other damage or loss

**Intellectual Property:**
- Scarlett Hollow © Black Tabby Games
- This tool is not associated with Black Tabby Games
- Do not claim this tool as your own work
- Do not violate the game's terms of service

---

## 📋 Contributing

Want to help improve this tool?

See [CONTRIBUTING.md](./CONTRIBUTING.md) for:
- How to report bugs
- How to suggest features
- How to contribute code
- Code style guidelines
- Testing checklist

**Everyone welcome!** Whether it's bug reports, feature ideas, or code contributions.

---

## 📦 Version History

### v2.0.0 (Current)
- ✨ Relationships editor with 10 dimensions
- ✨ Player name editor
- 🎨 UI improvements
- 🐛 Various bug fixes

### v1.0.0
- ✨ Initial release
- ✨ Traits editor
- ✨ Offline operation

See [CHANGELOG.md](./CHANGELOG.md) for full history.

---

## Footer

**For the latest updates and downloads**, visit the [GitHub Repository](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor).

**Questions?** Open an [issue](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/issues) or start a [discussion](https://github.com/FridgeFreezerUnit/Scarlet-Hollow-Save-Editor/discussions)!

---

**Last Updated:** May 2026  
**Status:** Actively Maintained ✅  
**License:** MIT
