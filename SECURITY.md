# Security Policy

<p align="center">
  <img src="https://img.shields.io/badge/Encryption-AES--256-green?style=for-the-badge" alt="AES-256">
  <img src="https://img.shields.io/badge/Signatures-Ed25519-blue?style=for-the-badge" alt="Ed25519">
  <img src="https://img.shields.io/badge/Storage-Local%20Only-purple?style=for-the-badge" alt="Local Only">
  <img src="https://img.shields.io/badge/Telemetry-None-red?style=for-the-badge" alt="No Telemetry">
</p>

---

## 🛡️ Our Commitment

Security is the foundation of **MyWorld**. As a password manager, we understand that you're trusting us with your most sensitive data. We take this responsibility extremely seriously.

This document outlines our security practices and provides instructions for responsible vulnerability disclosure.

---

## ✅ Supported Versions

| Version | Status | Security Updates |
|---------|--------|------------------|
| 2.x.x   | ✅ Current | Active support |
| 1.x.x   | ⚠️ Legacy | Critical fixes only |
| < 1.0   | ❌ EOL | No support |

> **Recommendation:** Always use the latest version to ensure you have the most recent security patches.

---

## 🔐 Security Architecture

### Encryption & Key Management

| Component | Technology | Details |
|-----------|------------|---------|
| **Data Encryption** | AES-256-GCM | Authenticated encryption for all stored data |
| **Key Derivation** | PBKDF2-SHA256 | 100,000+ iterations, unique salt per vault |
| **Update Signatures** | Ed25519 | Cryptographic verification of all updates |
| **Hash Verification** | SHA-256 | Integrity checking for downloaded files |

### Data Protection

```
┌─────────────────────────────────────────────────────────┐
│                    YOUR DEVICE                          │
│  ┌─────────────────────────────────────────────────┐   │
│  │              MYWORLD VAULT                       │   │
│  │  ┌─────────────┐    ┌─────────────────────┐    │   │
│  │  │ Master Key  │───▶│ AES-256 Encrypted   │    │   │
│  │  │  (PBKDF2)   │    │     Passwords       │    │   │
│  │  └─────────────┘    └─────────────────────┘    │   │
│  └─────────────────────────────────────────────────┘   │
│                         │                               │
│                    ❌ NO CLOUD                          │
│                    ❌ NO SYNC                           │
│                    ❌ NO TELEMETRY                      │
└─────────────────────────────────────────────────────────┘
```

### Security Features

| Feature | Description |
|---------|-------------|
| 🔒 **Zero-Knowledge** | Master password never stored or transmitted |
| 🧹 **Memory Protection** | Sensitive data cleared from RAM after use |
| ⏱️ **Auto-Lock** | Automatic vault locking after inactivity |
| 📋 **Clipboard Guard** | Auto-clear clipboard after copying passwords |
| 🔄 **Signed Updates** | Ed25519 signatures prevent tampered updates |
| 🌐 **Offline-First** | No internet required; no data leaves your device |

---

## 🚨 Reporting a Vulnerability

We appreciate the security research community's efforts in helping keep our users safe.

### ⚠️ Important

> **DO NOT** open a public GitHub issue for security vulnerabilities.
>
> Public disclosure before a fix is available puts users at risk.

### 📧 How to Report

**Email:** [moner.aldabai@gmail.com](mailto:moner.aldabai@gmail.com)

**Subject Line:** `[SECURITY] Brief description`

### 📝 What to Include

```markdown
## Vulnerability Report

**Type:** [e.g., Encryption flaw, Authentication bypass, Data exposure]

**Severity:** [Critical / High / Medium / Low]

**Affected Version(s):** [e.g., 2.0.0]

**Description:**
[Clear description of the vulnerability]

**Steps to Reproduce:**
1. Step one
2. Step two
3. ...

**Impact:**
[What an attacker could achieve]

**Proof of Concept:**
[Code, screenshots, or video if available]

**Suggested Fix:**
[Optional - your recommendations]
```

### ⏰ Response Timeline

| Stage | Timeframe |
|-------|-----------|
| **Acknowledgment** | Within 48 hours |
| **Initial Assessment** | Within 7 days |
| **Status Updates** | Every 7 days during investigation |
| **Resolution** | Based on severity (critical: ASAP) |
| **Disclosure** | Coordinated with researcher |

---

## 🤝 Safe Harbor

We consider security research conducted in accordance with this policy to be:

- ✅ **Authorized** and lawful
- ✅ **Helpful** to the security of our users
- ✅ **Conducted in good faith**

### We Will NOT Pursue Legal Action If You:

- Report vulnerabilities in good faith
- Avoid privacy violations and data destruction
- Do not exploit vulnerabilities beyond proof of concept
- Allow reasonable time for fixes before disclosure
- Do not use findings for personal gain or malicious purposes

---

## 👤 Security Best Practices

### For Users

| Practice | Why It Matters |
|----------|----------------|
| 🔑 **Strong Master Password** | Use 16+ characters, mix of types, unique to MyWorld |
| 🔄 **Keep Updated** | Updates include critical security patches |
| 💾 **Secure Backups** | Encrypt backup files, store in safe location |
| 🔒 **Lock When Away** | Use auto-lock or manually lock when leaving |
| ✅ **Verify Downloads** | Only download from official GitHub releases |
| 🚫 **Never Share** | Never share your master password with anyone |

### Password Strength Guidelines

```
❌ Weak:     password123
❌ Medium:   MyP@ssw0rd!
✅ Strong:   correct-horse-battery-staple-42!
✅ Best:     [Generated 20+ character random password]
```

---

## 📞 Contact

| Purpose | Contact |
|---------|---------|
| 🔒 **Security Reports** | [moner.aldabai@gmail.com](mailto:moner.aldabai@gmail.com) |
| 🐛 **Bug Reports** | [GitHub Issues](https://github.com/moneraldabai-ui/MyWorld-Password-Manager-Password-Manager/issues) |
| 💬 **General Questions** | [GitHub Discussions](https://github.com/moneraldabai-ui/MyWorld-Password-Manager-Password-Manager/discussions) |

---

<p align="center">
  <strong>Thank you for helping keep MyWorld users safe.</strong>
</p>

<p align="center">
  <a href="https://github.com/moneraldabai-ui/MyWorld-Password-Manager-Password-Manager">← Back to Repository</a>
</p>
