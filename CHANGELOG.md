# Changelog

All notable changes to **MyWorld Password Manager** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### Planned
- Browser extension for auto-fill
- Biometric unlock (Windows Hello)
- Password sharing (encrypted)
- Mobile companion app

---

## [2.0.0] - 2026-03-26

### Added

#### Security
- **AES-256-GCM encryption** for all stored data
- **PBKDF2-SHA256** key derivation with 100,000+ iterations
- **Ed25519 signed updates** for secure auto-update verification
- **Auto-lock** after configurable inactivity timeout
- **Memory protection** - sensitive data cleared from RAM
- **Clipboard auto-clear** after copying passwords

#### Password Management
- **Password generator** with customizable rules (8-128 characters)
- **Strength meter** with visual indicators (Weak → Excellent)
- **Duplicate detection** to find reused passwords
- **Breach check** against known password leaks
- **Password history** tracking

#### Organization
- **Categories** - Social, Banking, Work, Email, and custom categories
- **Tags** - Flexible labeling system
- **Favorites** - Quick access to frequently used entries
- **Smart search** - Instant filtering across all fields
- **Secure notes** - Encrypted text attached to entries

#### User Interface
- **Modern dark theme** with clean design
- **Keyboard shortcuts** for all common actions
- **Zoom controls** for accessibility
- **Responsive layout** adapts to window size

#### Data Management
- **Encrypted backup** - Export vault with full encryption
- **Import support** - Migrate from other password managers
- **Offline-first** - No internet connection required
- **Portable mode** - Run from USB drive (optional)

#### Auto-Update System
- **Secure updates** with Ed25519 signature verification
- **SHA-256 integrity** checking for downloaded files
- **Configurable** update preferences (automatic/manual)
- **Rollback support** if update fails

### Security Notes
- Zero-knowledge architecture - master password never stored
- No cloud storage - all data remains on local device
- No telemetry - no tracking, analytics, or data collection
- No account required - fully offline operation

---

## [1.x.x] - Legacy

> **Note:** Version 1.x was a private beta release. Users on 1.x should upgrade to 2.0.0 for the latest security features.

### 1.0.0 - Initial Development
- Basic password storage
- Simple encryption
- Local file storage

---

## Version History

| Version | Date | Type |
|---------|------|------|
| **2.0.0** | 2026-03-26 | Major Release |
| 1.x.x | Private | Legacy Beta |

---

## Upgrade Guide

### From 1.x to 2.0.0

1. **Backup your vault** before upgrading
2. Download the [latest installer](https://github.com/moneraldabai-ui/MyWorld/releases/latest)
3. Run the installer - it will handle the migration
4. Verify your data after upgrade

> **Important:** Version 2.0 uses enhanced encryption. The upgrade process will re-encrypt your vault automatically.

---

## Links

- **Download:** [Latest Release](https://github.com/moneraldabai-ui/MyWorld/releases/latest)
- **Issues:** [Report a Bug](https://github.com/moneraldabai-ui/MyWorld/issues)
- **Security:** [Report Vulnerability](mailto:moner.aldabai@gmail.com)

---

<p align="center">
  <a href="https://github.com/moneraldabai-ui/MyWorld">
    <img src="https://img.shields.io/badge/MyWorld-Changelog-5865F2?style=for-the-badge" alt="Changelog">
  </a>
</p>
