

## 🛰️ ReconX

### Simple • Sequential • Beginner-Friendly Web Recon Guide

ReconX is a clean, step-by-step reconnaissance guide for **authorized security testing**.

> **Start from Phase 0 and move forward. One phase at a time.**

---

## 🗺️ Recon Roadmap

| Phase | Topic | What are we trying to find? |
|---|---|---|
| ⚙️ **Phase 0** | Setup | Prepare the environment |
| 🔍 **Phase 1** | Passive Recon & OSINT | Public information about the target |
| 🌐 **Phase 2** | Subdomain Enumeration | Subdomains |
| ✅ **Phase 3** | HTTP Probing | Live web hosts |
| 🧩 **Phase 4** | Technology Fingerprinting | Technologies being used |
| 📂 **Phase 5** | Content Discovery | Directories and files |
| 🔗 **Phase 6** | URL & Endpoint Discovery | URLs and endpoints |
| 📜 **Phase 7** | JavaScript Analysis | Useful information inside JS |
| 🎯 **Phase 8** | Parameter Discovery | Parameters and inputs |
| 🛡️ **Phase 9** | Vulnerability Scanning | Security issues to review |
| 📚 **Resources** | Wordlists & Resources | Helpful resources |

---

## 🔄 The Whole Process

```text
                    TARGET
                       │
                       ▼
              ⚙️ PHASE 0 — SETUP
                       │
                       ▼
          🔍 PHASE 1 — PASSIVE RECON
                       │
                       ▼
       🌐 PHASE 2 — SUBDOMAIN ENUMERATION
                       │
                       ▼
            ✅ PHASE 3 — HTTP PROBING
                       │
                       ▼
       🧩 PHASE 4 — TECHNOLOGY FINGERPRINT
                       │
                       ▼
        📂 PHASE 5 — CONTENT DISCOVERY
                       │
                       ▼
       🔗 PHASE 6 — URL & ENDPOINTS
                       │
                       ▼
          📜 PHASE 7 — JAVASCRIPT
                       │
                       ▼
          🎯 PHASE 8 — PARAMETERS
                       │
                       ▼
       🛡️ PHASE 9 — SECURITY REVIEW
                       │
                       ▼
                    REPORT



                    📚 Phases
⚙️ Phase 0 — Setup

Prepare your basic environment before starting recon.

→ Open Phase 0

🔍 Phase 1 — Passive Recon & OSINT

Collect publicly available information about the target.

Tools covered:

Censys
Shodan
DNSDumpster
WHOIS
ViewDNS

→ Open Phase 1

🌐 Phase 2 — Subdomain Enumeration

Find subdomains and validate the discovered names.

Tools covered:

Subfinder
Amass
dnsx
PureDNS

→ Open Phase 2

✅ Phase 3 — HTTP Probing

Find which discovered hosts have reachable web services.

Tools covered:

httpx
Gowitness

→ Open Phase 3

🧩 Phase 4 — Technology Fingerprinting

Understand what technologies the web application is using.

Tools covered:

Wappalyzer
WhatWeb
BuiltWith

→ Open Phase 4

📂 Phase 5 — Content & Directory Discovery

Discover publicly reachable directories, files and paths.

Tools covered:

ffuf
Feroxbuster
Dirsearch

→ Open Phase 5

🔗 Phase 6 — URL & Endpoint Discovery

Build a larger list of known URLs and application endpoints.

Tools covered:

Katana
GAU
Waybackurls
Hakrawler

→ Open Phase 6

📜 Phase 7 — JavaScript Analysis

Review JavaScript files for useful application information.

Tools covered:

SecretFinder
JSluice

→ Open Phase 7

🎯 Phase 8 — Parameter Discovery

Find parameters used by web applications.

Tools covered:

Arjun
ParamSpider

→ Open Phase 8

🛡️ Phase 9 — Vulnerability Scanning

Use your recon results to guide authorized security testing.

Tools covered:

Nuclei
Nmap
SQLMap / Ghauri
Dalfox

→ Open Phase 9

📚 Resources

Useful wordlists and supporting resources.

→ Open Resources

🧠 How to Use ReconX

Don't try to learn every tool at once.

For each phase:

1. Read the goal
       ↓
2. Understand why the phase exists
       ↓
3. Learn the tools
       ↓
4. Run them only in an authorized scope
       ↓
5. Understand the output
       ↓
6. Move to the next phase

The important thing is not memorizing commands.

Understand what you are looking for and why.

⚠️ Legal & Ethical Use

ReconX is intended for authorized security testing and educational use.

Only test:

Systems you own
CTF/lab environments
Bug-bounty targets that are explicitly in scope
Systems where you have permission

Always verify the target's scope and rules before running tools.

⭐ ReconX Philosophy

Discover → Verify → Understand → Review → Report

Keep recon simple, organized and repeatable.

📜 License

MIT License
"""
