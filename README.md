# 🦉 Ouser

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1-cyan?style=flat-square"/>
</p>

> **Ouser** — OSINT Username Scanner

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


Ouser is an offline, read-only local user, group and account-policy auditor that parses /etc/passwd, /etc/shadow, /etc/group and login.defs to assess identity hygiene. It flags UID 0 duplicates, empty or weak password hashes, stale and never-expiring accounts, orphaned files and risky sudo/group membership. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Parsers for /etc/passwd, /etc/shadow, /etc/group, /etc/gshadow and login.defs
- Duplicate UID 0 / privileged-account detection and system-vs-human account classification
- Password-hygiene checks: empty/locked/weak hashes, aging, expiry and never-expiring accounts
- Group and sudo membership review for over-privileged users
- Shell/home-directory and orphaned-file hygiene checks
- CWE+ATT&CK mapping, offline --root trees, score/grade and TXT/MD/JSON/CSV/SARIF export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./Ouser --scan -f sarif -o users.sarif
./Ouser --passwd /etc/passwd --shadow /etc/shadow
./Ouser -r /mnt/image --fail-on high --json
./Ouser --demo
./Ouser --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
