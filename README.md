# 🦉 OLogX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OLogX** — Security Log Analyzer / SIEM-lite

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OLogX is a security log analyzer (SIEM-lite) that streams auth, syslog, Apache/Nginx, journalctl text, JSON-lines, and key=value logs. It detects brute-force, spray, privilege changes, web probes, and more; matches IOCs; builds timelines and stats; and exports TXT, CSV, or JSON with optional baseline/diff.

---

## ✨ Features

- Streaming ingest of auth.log/syslog/secure, Apache/Nginx access+error, journalctl text, JSON-lines, key=value (plain or .gz)
- Parsers for sshd, sudo, su, cron, PAM, user/group changes, combined access, and web error formats
- Detections: brute-force bursts, password spray, success-after-failure, root SSH, sudo failures, scanner UAs, sensitive path probes, 4xx/5xx spikes
- IOC matcher for IP/CIDR/domain/hash lists; merged multi-file timeline with host/user/IP/service and `--since` filters
- Stats with top talkers/URIs/status/users, offline geo class, and ASCII hourly histogram
- Baseline digests + spike diff; TXT/CSV/JSON export; CLI and interactive menu

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLogX -f /var/log/auth.log --ssh --since 24h
./OLogX -d ./logs --web --ioc iocs.txt --json -o findings.json
./OLogX -f access.log --stats --timeline --fail-on high
./OLogX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
