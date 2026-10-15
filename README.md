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

Security log analyzer & SIEM-lite (SSH, sudo, web, IOC, timeline)

---

## ✨ Features

- Streaming ingest of auth.log, syslog, secure, Apache/Nginx access + error logs, journalctl text exports, JSON-lines and key=value logs — plain or gzip (.gz), line by line, never fully loaded
- Parsers — sshd (failed / accepted / invalid user / preauth disconnects), sudo, su, cron, PAM, useradd, groupadd/usermod, combined / common access format, Apache & Nginx error log, JSON lines, key=value
- Detections — brute-force bursts (threshold/window), password spray across users, success-after-failure, new user / sudo group changes, root SSH login, sudo failures, scanner User-Agents, sensitive path probes (.env, wp-login, admin, .git ...), 4xx/5xx spikes, proxy / CONNECT abuse, off-hours activity, clock skew / out-of-order timestamps
- IOC matcher — IP / CIDR / domain / hash lists
- Merged multi-file timeline with host/user/IP/service filters and --since relative or absolute time
- Stats — top talkers, top URIs, status codes, users, offline geo class (private/public/bogon), ASCII hourly histogram
- Baseline daily digests + spike diff
- Export TXT / CSV / JSON with save-location chooser, clipboard copy of critical findings
- Full CLI mode (--file, --dir, --ssh, --web, --ioc, --since, --json, -o, --fail-on) + interactive menu

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLogX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
