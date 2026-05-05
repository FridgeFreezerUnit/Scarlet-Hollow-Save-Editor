# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2024

### Added
- ✨ **Relationships Tab** — View and edit character relationship dimensions
  - 9 characters (Stella, Tabitha, Oscar, Kaneeka, Reese, Wayne, Duke, Avery, Sybil)
  - 10 dimensions per character (agreeable, adversarial, open, closed, bold, passive, reliable, unreliable, insightful, dull)
  - Wiki tooltips for each dimension explaining meaning
  - Toggle between read-only and edit mode
  - Romance/trust badges for special character flags
- ✨ **Player Name Editor** — Change character name in save
  - Updates both `store.player_name` and `store.save_name` 
  - Save-wide changes applied on download
- ✨ **Advanced Tab** — Detailed game variable inspection
  - Player name editor
  - Cheater flag management
  - Variable count and file size info
- ✨ **CheatBypass Tool** — Standalone Python utility to patch game anti-cheat
  - Automatically finds Scarlet Hollow installation
  - Extracts and patches trait count checks
  - Creates backups before modifying
  - Comprehensive documentation
- 📖 **Comprehensive Documentation**
  - Expanded README with table of contents
  - Detailed feature explanations
  - Troubleshooting guide
  - Save location reference
  - CheatBypass setup instructions
- 🎨 **UI Improvements**
  - Better organized stats bar
  - Improved layout for relationship cards
  - Enhanced color coding and visual hierarchy
  - More intuitive tab navigation

### Changed
- 📝 Rewrote documentation for clarity and completeness
- 🎨 Improved visual feedback for edit modes
- 🔄 Refactored pickle parsing for better accuracy

### Fixed
- 🐛 Fixed trait flag reset logic for multiple related flags
- 🐛 Improved error handling for malformed save files
- 🐛 Fixed browser security warnings documentation

### Known Issues
- Missing traits can't be created from scratch (must exist in save already)
- Some very old saves may not be fully compatible
- Game updates may require code updates for new variables

---

## [1.0.0] - 2024

### Added
- 🎉 Initial release
- ✨ **Traits Tab** — Edit character traits
  - Toggle 7 traits on/off
  - Original trait detection
  - Related flag cleanup on disable
  - Anti-cheat bypass option
- 📤 **Drag-and-drop** file loading
- 📂 **Save Format Details**
  - Ren'Py ZIP archive handling
  - Pickle binary parsing
  - Safe byte-level modification
- 🔒 **100% Offline** operation
- 📱 **Cross-browser** compatibility
- 📖 Basic documentation

---

## Future Roadmap

### Planned for v2.1
- [ ] Direct trait count manipulation (if game allows)
- [ ] Flag value editing (not just on/off)
- [ ] Save comparison tool (compare before/after)
- [ ] Batch processing (modify multiple saves)

### Under Consideration
- [ ] Story flag editor
- [ ] Inventory editor
- [ ] Save file validator
- [ ] Game state analyzer
- [ ] Dark mode theme

### Not Planned
- Game piracy tools or methods
- Multiplayer/online features
- Game reversal engineering beyond save editing

---

## Security Policy

### Reporting Security Issues

If you find a security vulnerability, please **do not** open a public GitHub issue.

Instead:
1. Email security concerns to maintainers (see README for contact info)
2. Describe the vulnerability clearly
3. Allow time for a fix before public disclosure

We take security seriously and will:
- Acknowledge receipt quickly
- Work on a fix promptly
- Credit you if you wish
- Coordinate responsible disclosure

---

## Archive

### Previous Development Notes
- Project hobby-coded in spare time
- Reverse-engineered Scarlet Hollow save format from game files
- Tested on saves from multiple playthrough patterns
- Validated against official wiki data

---

**Last Updated:** 2024  
**Maintainer:** Community Contributors  
**License:** MIT
