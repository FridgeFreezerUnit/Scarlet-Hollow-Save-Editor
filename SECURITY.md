# Security Policy

## Overview

The Scarlett Hollow Enhanced Save Editor takes security seriously. This document explains how to report security issues responsibly.

## Supported Versions

| Version | Supported          |
|---------|-------------------|
| 2.0.x   | ✅ Yes            |
| 1.0.x   | ⚠️ Legacy only     |
| < 1.0   | ❌ Not supported   |

## Reporting a Vulnerability

### If You Find a Security Issue

**Do NOT open a public GitHub issue.** Security vulnerabilities should be reported privately.

### How to Report

1. **Contact the maintainers privately** with:
   - Description of the vulnerability
   - Steps to reproduce (if applicable)
   - Potential impact
   - Any proof-of-concept code (if safe to share)

2. **Do NOT**:
   - Publicly disclose the vulnerability before we can fix it
   - Share exploit code publicly
   - Discuss it on Discord or social media

3. **We will**:
   - Acknowledge receipt within 48 hours
   - Work on a fix as priority
   - Coordinate disclosure timeline with you
   - Credit you (if you wish) in the fix announcement

## Security Considerations

### This Tool is Safe Because:

✅ **No server communication** — Everything runs in your browser  
✅ **No external dependencies** — JSZip is embedded, not loaded from CDN  
✅ **Open source** — All code is visible for security review  
✅ **No data collection** — We don't track or store anything  
✅ **No automatic updates** — You control what version you use  

### Limitations:

⚠️ **Ren'Py saves are unencrypted** — This tool reads plaintext pickle format (same as Scarlet Hollow itself)  
⚠️ **Browser security** — Depends on your browser's security implementation  
⚠️ **User responsibility** — You must use this responsibly and keep backups  

### Trust Model

- **Trust Requirement**: You must trust Black Tabby Games with save file content
- **What We Do**: Provide a tool to modify unencrypted save data you already have
- **We Don't**: Upload files to servers, collect data, or access anything else

## Best Practices for Users

### Protect Your Saves

1. **Always backup** before using this tool
2. **Keep backups** in a separate folder
3. **Test modified saves** on a throwaway game save first
4. **Never share** save files with untrusted sources

### Browser Security

1. **Use an updated browser** (Chrome, Firefox, Safari, Edge)
2. **Enable security features** (JavaScript enabled is required)
3. **Only open HTML from trusted sources**
4. **Don't give browser excessive permissions** (save editor only needs file access)

### File Security

1. **Keep save files private** — Don't share with strangers
2. **Be careful with modified saves** — Only distribute to people you trust
3. **Understand pickle format** — It can execute arbitrary code (but we don't)

## Dependency Security

### Current Dependencies

- **JSZip 3.10.1** — Minified, embedded in HTML (no external requests)
- **Modern browser APIs** — FileReader, Uint8Array, etc. (built-in, always current)

### No External CDNs

✅ No external scripts loaded  
✅ No CSS frameworks loaded  
✅ No third-party libraries fetched  
✅ Zero network dependencies (after initial page load)

## Known Limitations

1. **Very old saves** — Pre-Chapter 2 saves may not be fully compatible
2. **Game updates** — New game versions may add variables we don't recognize
3. **Trait limitations** — Can't create traits that don't exist in save yet
4. **Save validation** — We don't validate game logic, only byte format

## Responsible Disclosure

### Timeline

- **Day 1**: You report vulnerability
- **Day 2-3**: We investigate and acknowledge
- **Day 3-14**: We develop and test a fix
- **Day 14**: Fix is released
- **Day 15**: Public disclosure of issue (with credit to you)

If you need a longer timeline, let us know.

## Scope

### In Scope (Report These)

- Code vulnerabilities in the editor or CheatBypass tool
- Browser security bypasses
- Data leaks or privacy issues
- Unintended file access
- Pickle injection vulnerabilities

### Out of Scope (Don't Report These)

- Game balance issues
- Scarlet Hollow game vulnerabilities (report to Black Tabby Games)
- Platform issues (Steam, itch.io violations)
- Missing features or UI improvements
- Third-party dependency issues

## Contact

For security issues, contact the maintainers at:

> [See README.md for current contact information]

---

## Additional Resources

### Related Security Topics

- [OWASP Web Security](https://owasp.org/)
- [Python Pickle Security](https://docs.python.org/3/library/pickle.html#what-can-pickle-do)
- [Ren'Py Save Format](https://renpy.org/)

### Acknowledgments

Thanks to everyone who has responsibly reported issues and helped us improve security!

---

**Last Updated:** 2024  
**Status:** Active and Maintained
