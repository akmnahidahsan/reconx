# ðŸ›°ï¸ ReconX

### Simple â€¢ Sequential â€¢ Beginner-Friendly Web Recon Guide

ReconX is a clean, step-by-step reconnaissance guide for **authorized security testing**.

> **Start from Phase 0 and move forward. One phase at a time.**

---

## ðŸ—ºï¸ Recon Roadmap

| Phase | Topic | What are we trying to find? |
|---|---|---|
| âš™ï¸ **Phase 0** | Setup | Prepare the environment |
| ðŸ” **Phase 1** | Passive Recon & OSINT | Public information about the target |
| ðŸŒ **Phase 2** | Subdomain Enumeration | Subdomains |
| âœ… **Phase 3** | HTTP Probing | Live web hosts |
| ðŸ§© **Phase 4** | Technology Fingerprinting | Technologies being used |
| ðŸ“‚ **Phase 5** | Content Discovery | Directories and files |
| ðŸ”— **Phase 6** | URL & Endpoint Discovery | URLs and endpoints |
| ðŸ“œ **Phase 7** | JavaScript Analysis | Useful information inside JS |
| ðŸŽ¯ **Phase 8** | Parameter Discovery | Parameters and inputs |
| ðŸ›¡ï¸ **Phase 9** | Vulnerability Scanning | Security issues to review |
| ðŸ“š **Resources** | Wordlists & Resources | Helpful resources |

---

## ðŸ”„ The Whole Process

```text
                    TARGET
                       â”‚
                       â–¼
              âš™ï¸ PHASE 0 â€” SETUP
                       â”‚
                       â–¼
          ðŸ” PHASE 1 â€” PASSIVE RECON
                       â”‚
                       â–¼
       ðŸŒ PHASE 2 â€” SUBDOMAIN ENUMERATION
                       â”‚
                       â–¼
            âœ… PHASE 3 â€” HTTP PROBING
                       â”‚
                       â–¼
       ðŸ§© PHASE 4 â€” TECHNOLOGY FINGERPRINT
                       â”‚
                       â–¼
        ðŸ“‚ PHASE 5 â€” CONTENT DISCOVERY
                       â”‚
                       â–¼
       ðŸ”— PHASE 6 â€” URL & ENDPOINTS
                       â”‚
                       â–¼
          ðŸ“œ PHASE 7 â€” JAVASCRIPT
                       â”‚
                       â–¼
          ðŸŽ¯ PHASE 8 â€” PARAMETERS
                       â”‚
                       â–¼
       ðŸ›¡ï¸ PHASE 9 â€” SECURITY REVIEW
                       â”‚
                       â–¼
                    REPORT
```

---

# ðŸ“š Phases

## âš™ï¸ Phase 0 â€” Setup

Prepare your basic environment before starting recon.

**[â†’ Open Phase 0](phases/00-setup.md)**

---

## ðŸ” Phase 1 â€” Passive Recon & OSINT

Collect publicly available information about the target.

**Tools covered:**
- Censys
- Shodan
- DNSDumpster
- WHOIS
- ViewDNS

**[â†’ Open Phase 1](phases/01-passive-recon.md)**

---

## ðŸŒ Phase 2 â€” Subdomain Enumeration

Find subdomains and validate the discovered names.

**Tools covered:**
- Subfinder
- Amass
- dnsx
- PureDNS

**[â†’ Open Phase 2](phases/02-subdomain-enumeration.md)**

---

## âœ… Phase 3 â€” HTTP Probing

Find which discovered hosts have reachable web services.

**Tools covered:**
- httpx
- Gowitness

**[â†’ Open Phase 3](phases/03-http-probing.md)**

---

## ðŸ§© Phase 4 â€” Technology Fingerprinting

Understand what technologies the web application is using.

**Tools covered:**
- Wappalyzer
- WhatWeb
- BuiltWith

**[â†’ Open Phase 4](phases/04-technology.md)**

---

## ðŸ“‚ Phase 5 â€” Content & Directory Discovery

Discover publicly reachable directories, files and paths.

**Tools covered:**
- ffuf
- Feroxbuster
- Dirsearch

**[â†’ Open Phase 5](phases/05-content-discovery.md)**

---

## ðŸ”— Phase 6 â€” URL & Endpoint Discovery

Build a larger list of known URLs and application endpoints.

**Tools covered:**
- Katana
- GAU
- Waybackurls
- Hakrawler

**[â†’ Open Phase 6](phases/06-url-endpoints.md)**

---

## ðŸ“œ Phase 7 â€” JavaScript Analysis

Review JavaScript files for useful application information.

**Tools covered:**
- SecretFinder
- JSluice

**[â†’ Open Phase 7](phases/07-javascript.md)**

---

## ðŸŽ¯ Phase 8 â€” Parameter Discovery

Find parameters used by web applications.

**Tools covered:**
- Arjun
- ParamSpider

**[â†’ Open Phase 8](phases/08-parameters.md)**

---

## ðŸ›¡ï¸ Phase 9 â€” Vulnerability Scanning

Use your recon results to guide authorized security testing.

**Tools covered:**
- Nuclei
- Nmap
- SQLMap / Ghauri
- Dalfox

**[â†’ Open Phase 9](phases/09-vulnerability-scanning.md)**

---

# ðŸ“š Resources

Useful wordlists and supporting resources.

**[â†’ Open Resources](resources/README.md)**

---

# ðŸ§  How to Use ReconX

Don't try to learn every tool at once.

For each phase:

```text
1. Read the goal
       â†“
2. Understand why the phase exists
       â†“
3. Learn the tools
       â†“
4. Run them only in an authorized scope
       â†“
5. Understand the output
       â†“
6. Move to the next phase
```

The important thing is not memorizing commands.

**Understand what you are looking for and why.**

---

# âš ï¸ Legal & Ethical Use

ReconX is intended for **authorized security testing and educational use**.

Only test:

- Systems you own
- CTF/lab environments
- Bug-bounty targets that are explicitly in scope
- Systems where you have permission

Always verify the target's scope and rules before running tools.

---

# â­ ReconX Philosophy

> **Discover â†’ Verify â†’ Understand â†’ Review â†’ Report**

Keep recon simple, organized and repeatable.

---

## ðŸ“œ License

MIT License