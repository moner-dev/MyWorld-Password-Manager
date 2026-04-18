# Build & Installation Guide

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows" alt="Windows">
  <img src="https://img.shields.io/badge/Architecture-x64-blue?style=for-the-badge" alt="x64">
  <img src="https://img.shields.io/badge/Installer-Inno%20Setup-5865F2?style=for-the-badge" alt="Inno Setup">
  <img src="https://img.shields.io/badge/Signed-Ed25519-green?style=for-the-badge" alt="Signed">
</p>

---

## Overview

This repository contains **release builds only** for MyWorld Password Manager. The source code is maintained privately to ensure security integrity.

> All releases are cryptographically signed with Ed25519 signatures and verified via SHA-256 hashes.

---

## Quick Start

### Download & Install

1. Download the latest installer from [GitHub Releases](https://github.com/moner-dev/MyWorld-Password-Manager/releases/latest)
2. Run `MyWorld_Setup_x.x.x.exe`
3. Follow the installation wizard
4. Launch MyWorld from your desktop or Start menu

---

## System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | Windows 10 (64-bit) | Windows 11 (64-bit) |
| **RAM** | 4 GB | 8 GB |
| **Storage** | 100 MB | 200 MB |
| **Display** | 1280 x 720 | 1920 x 1080 |
| **Internet** | Not required | Not required |

### Runtime Dependencies

| Dependency | Version | Included |
|------------|---------|----------|
| WebView2 Runtime | Latest | Auto-installed |
| Visual C++ Redistributable | 2019+ | Bundled |

> **Note:** The installer handles all dependencies automatically.

---

## Installation Options

### Standard Installation (Recommended)

```
1. Download: MyWorld_Setup_2.0.0.exe
2. Run installer as Administrator (optional, for all users)
3. Choose installation directory
4. Select Start Menu shortcuts
5. Complete installation
```

### Silent Installation

For enterprise deployment or scripting:

```batch
MyWorld_Setup_2.0.0.exe /SILENT /NORESTART
```

| Flag | Description |
|------|-------------|
| `/SILENT` | Minimal UI, shows progress only |
| `/VERYSILENT` | No UI at all |
| `/NORESTART` | Suppress restart prompts |
| `/DIR="path"` | Custom install directory |
| `/LOG="file"` | Write installation log |

---

## Verify Your Download

### SHA-256 Checksum

Always verify the installer integrity before running:

**Windows PowerShell:**
```powershell
(Get-FileHash -Algorithm SHA256 .\MyWorld_Setup_2.0.0.exe).Hash
```

**Expected Hash (v2.0.0):**
```
bc57b11c907ef3a9096e2a1c2db25e94857b96b56ee5c9e907147b3239c818d0
```

### Signature Verification

MyWorld uses Ed25519 digital signatures for update verification. The application automatically verifies signatures during the update process.

| Component | Algorithm |
|-----------|-----------|
| File Integrity | SHA-256 |
| Signature | Ed25519 |
| Key Derivation | PBKDF2-SHA256 |

---

## Uninstallation

### Via Windows Settings

1. Open **Settings** > **Apps** > **Installed Apps**
2. Find **MyWorld**
3. Click **Uninstall**

### Via Control Panel

1. Open **Control Panel** > **Programs** > **Uninstall a program**
2. Select **MyWorld**
3. Click **Uninstall**

### Data Handling

| Data Type | Location | Removed on Uninstall |
|-----------|----------|----------------------|
| Application Files | `C:\Program Files\MyWorld` | Yes |
| User Vault | `%APPDATA%\MyWorld` | No (preserved) |
| Settings | `%APPDATA%\MyWorld\config` | No (preserved) |

> **Important:** Your encrypted vault and settings are preserved during uninstallation. Delete `%APPDATA%\MyWorld` manually if you want to remove all data.

---

## Auto-Update System

MyWorld includes a secure auto-update mechanism:

```
┌─────────────────────────────────────────────────────────┐
│                    UPDATE PROCESS                        │
├─────────────────────────────────────────────────────────┤
│  1. Check manifest.json for new version                 │
│  2. Download installer to temp directory                │
│  3. Verify SHA-256 hash matches manifest                │
│  4. Verify Ed25519 signature                            │
│  5. Prompt user for installation                        │
│  6. Apply update and restart                            │
└─────────────────────────────────────────────────────────┘
```

### Update Preferences

| Setting | Options |
|---------|---------|
| Check Frequency | Startup, Daily, Weekly, Manual |
| Download | Automatic, Ask First |
| Install | Automatic, Ask First |

---

## Troubleshooting

### Common Issues

| Issue | Solution |
|-------|----------|
| **Installer won't start** | Right-click > Run as Administrator |
| **Missing DLL errors** | Install Visual C++ Redistributable 2019 |
| **WebView2 issues** | Installer should auto-install; manually install from Microsoft |
| **Antivirus blocks** | Add exception for MyWorld; false positive (unsigned personal project) |

### Log Files

| Log | Location |
|-----|----------|
| Installation | `%TEMP%\MyWorld_Setup.log` (if `/LOG` used) |
| Application | `%APPDATA%\MyWorld\logs\` |

---

## Building from Source

The source code for MyWorld is **not publicly available**. This repository contains release artifacts only.

### For Authorized Contributors

If you have access to the private source repository:

1. Refer to the internal `CONTRIBUTING.md`
2. Follow the development environment setup guide
3. Use the provided build scripts

### Technology Stack

| Component | Technology |
|-----------|------------|
| **Backend** | Python 3.11+ |
| **Framework** | PyWebView 5.1 + Flask 3.0 |
| **Frontend** | HTML5, CSS3, JavaScript |
| **Encryption** | cryptography (AES-256-GCM) |
| **Packaging** | PyInstaller |
| **Installer** | Inno Setup 6 |

---

## Release Artifacts

Each release includes:

| File | Description |
|------|-------------|
| `MyWorld_Setup_x.x.x.exe` | Windows installer |
| `manifest.json` | Version manifest with signatures |
| `CHANGELOG.md` | Version history |

---

## Contact

| Purpose | Contact |
|---------|---------|
| Bug Reports | [GitHub Issues](https://github.com/moner-dev/MyWorld-Password-Manager/issues) |
| Feature Requests | [GitHub Issues](https://github.com/moner-dev/MyWorld-Password-Manager/issues) |
| Security Issues | [moner.intelligence@gmail.com](mailto:moner.intelligence@gmail.com) |
| General Questions | [GitHub Discussions](https://github.com/moner-dev/MyWorld-Password-Manager/discussions) |

---

<p align="center">
  <a href="https://github.com/moner-dev/MyWorld-Password-Manager/releases/latest">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-5865F2?style=for-the-badge" alt="Download">
  </a>
</p>

<p align="center">
  <a href="https://github.com/moner-dev/MyWorld-Password-Manager">Back to Repository</a>
</p>
