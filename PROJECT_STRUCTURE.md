# Project Structure

## File Organization

```
Scarlet-Hollow-Save-Editor/
├── save-editor-enhanced.html       # Main tool - open in browser
├── README.md                        # Main documentation
├── CHANGELOG.md                     # Version history
├── CONTRIBUTING.md                 # How to contribute
├── LICENSE                          # MIT license
├── SECURITY.md                      # Security policy
│
├── CheatBypass/                     # Game anti-cheat patcher
│   ├── cheat_bypass.py              # Main tool
│   ├── deploy_mod_enhanced.py       # Archive repacker helper
│   ├── extract_scripts.py           # Script extractor
│   ├── find_anti_cheat.py           # Anti-cheat code finder
│   ├── debug_archive.py             # Archive debugger
│   ├── README.md                    # CheatBypass documentation
│   └── QUICKSTART.md                # Quick setup guide
│
├── .github/                         # GitHub configuration
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md            # Bug report template
│   │   ├── feature_request.md       # Feature request template
│   │   └── config.yml               # Issue template config
│   └── pull_request_template.md     # PR template
│
├── saves/                           # Save files (example/testing)
│   └── [.save files]
│
├── site/                            # Website/wiki reference
│   └── [offline wiki pages]
│
└── .gitignore                       # Git ignore patterns
```

## Key Files

### For Users

| File | Purpose |
|------|---------|
| `save-editor-enhanced.html` | The actual save editor tool - just open in a browser! |
| `README.md` | Complete documentation, features, troubleshooting |
| `CheatBypass/README.md` | Guide for disabling the game's anti-cheat |
| `CHANGELOG.md` | What's new in each version |

### For Developers

| File | Purpose |
|------|---------|
| `CONTRIBUTING.md` | How to contribute code/documentation |
| `SECURITY.md` | Security policy and vulnerability reporting |
| `.github/ISSUE_TEMPLATE/` | GitHub issue templates |
| `.gitignore` | Files to exclude from git |

## File Sizes & Dependencies

### Single HTML File
The main `save-editor-enhanced.html` is a **self-contained** file:
- **~1700 lines** of code
- **~800KB** when opened (minified JSZip library embedded)
- **~50KB** when gzipped for transfer
- **No external dependencies** needed
- **Fully offline compatible** after download

### JSZip Library
- Embedded minified JavaScript
- Handles ZIP file reading/writing
- No CDN required, no network calls

### CheatBypass Tool
- **Python 3.6+** required
- Standalone utilities for game patching
- No external Python dependencies

## Code Organization

### Main Editor (`save-editor-enhanced.html`)

```html
<head>
  <!-- CSS Styles (~700 lines) -->
  <!-- Game data constants -->
  <!-- Trait definitions -->
  <!-- Relationship dimensions -->
  <!-- Flag mappings -->
</head>

<body>
  <!-- HTML Structure (~150 lines) -->
  <!-- Drop zone -->
  <!-- Tabs for different features -->
  <!-- Status display -->
  
  <script>
    <!-- JSZip Library (minified, ~50KB) -->
    
    <!-- Game Constants -->
    const TRAITS = [...]
    const REL_DIMS = [...]
    const REL_PAIRS = [...]
    
    <!-- Pickle Parsing Functions -->
    function findBoolPositions() {}
    function parseRelationshipDict() {}
    function readStoreVar() {}
    
    <!-- String Handling Functions -->
    function findStoreString() {}
    function encodePickleString() {}
    function replaceStoreString() {}
    function replaceRelationshipDict() {}
    
    <!-- UI Rendering -->
    function renderTraits() {}
    function renderRelationships() {}
    function updateUI() {}
    
    <!-- User Interactions -->
    function loadSave(file) {}
    function downloadSave() {}
    function applyNameEdit() {}
    
    <!-- Event Listeners -->
    document.addEventListener('change', ...)
    dropZone.addEventListener('drop', ...)
  </script>
</body>
```

### CheatBypass Tools

```
cheat_bypass.py          Main entry point
├── find_game_path()     Locate Scarlet Hollow
├── extract_archive()    Unzip .rpa file
├── find_and_patch_files()  Search & modify code
└── repack_archive()     Rebuild modified archive

deploy_mod_enhanced.py   Helper for repacking
extract_scripts.py       Extract all scripts
find_anti_cheat.py       Diagnostic tool
debug_archive.py         Debug utility
```

## Development Workflow

### Making a Change

1. **Edit files** (HTML, Python, or docs)
2. **Test locally**:
   - Open `save-editor-enhanced.html` in browser (F12 for console)
   - Or run Python tools: `python CheatBypass/cheat_bypass.py`
3. **Create pull request** with description

### Testing Save Compatibility

1. **Get a test save** from Scarlet Hollow
2. **Load in editor** - watch console (F12) for debug output
3. **Make changes** - traits, relationships, etc.
4. **Download modified** save
5. **Load in game** - verify it works
6. **Test edge cases**:
   - Very old saves (Chapter 1)
   - Recent saves (latest chapter)
   - Different trait selections

## Building for Release

When publishing a new version:

1. **Update version** in README.md and CHANGELOG.md
2. **Test thoroughly** with multiple saves
3. **Tag release**: `git tag v2.0.0`
4. **Create GitHub release** with changelog
5. **Verify** live site updates

## Documentation

### Keep These Updated
- `README.md` — Feature changes, new sections
- `CHANGELOG.md` — Version history
- `CONTRIBUTING.md` — If contribution process changes
- `CheatBypass/README.md` — Game patching info

### Don't Forget
- Example code in docs
- Troubleshooting section
- Configuration examples
- Save location references

## Performance Considerations

### Current Optimizations
- ✅ Minified JSZip library
- ✅ No external network requests
- ✅ Efficient pickle parsing
- ✅ Direct byte manipulation
- ✅ Cached DOM queries

### Potential Improvements
- [ ] Lazy loading for large saves
- [ ] Worker threads for parsing
- [ ] Indexed binary search
- [ ] Compression caching

## Security Checklist

- ✅ No external dependencies
- ✅ No server communication
- ✅ No data collection
- ✅ No automatic updates
- ✅ Open source for review
- ⚠️ Pickle parsing (trustworthy format only)
- ⚠️ Browser security assumptions

## Maintenance Notes

### Regular Tasks
- Monitor GitHub issues weekly
- Update for major game patches
- Keep dependencies fresh (mainly Python)
- Test with new browser versions

### Long-term
- Consider game version changes
- Plan for breaking Ren'Py updates
- Archive old versions
- Maintain compatibility matrix

---

**Last Updated:** 2024  
For questions about structure, see CONTRIBUTING.md
