# 🔍 Phase 1 — Passive Recon & OSINT (Target এ কোনো request পাঠাবে না)

> **Goal:** Find information about the target without directly interacting with the application as much as possible.

## 🧠 What is Passive Recon?

Passive recon means collecting information from **publicly available sources**.

Think of it as:

> “What can I learn about this target before touching the target?”

## 🌐 Online Tools (No Install Needed) 

### 1. Censys - internet-wide scanner database
**Use for:** Internet-facing hosts, services and certificates.

### Link : https://search.censys.io/

### Usage

```bash

Site: search.censys.io
Search: "target.com" — IP ranges, ports, certificates বের হবে
Search: ip:1.2.3.4 — specific IP এর info

```

### 2. Shodan — Search engine for IoT & servers
**Use for:** Publicly indexed services, ports and banners.
### Link : https://www.shodan.io/
### Usage

```
Site: shodan.io
Search: hostname:"target.com" — সব subdomains + ports
Search: org:"Company Name" — company এর সব IP
Search: ssl:"target.com" — SSL certificate দিয়ে সার্চ

```

### 3. DNSDumpster
**Use for:** DNS information and possible subdomains.

### 4. WHOIS
**Use for:** Domain registration information.

### 5. ViewDNS
**Use for:** DNS and network-related lookups.

## 📌 Simple Workflow

```text
Target
  ↓
Censys / Shodan
  ↓
DNS information
  ↓
Possible subdomains
  ↓
Save what you find
```

## ✅ Checklist

- [ ] Censys checked
- [ ] Shodan checked
- [ ] DNS information collected
- [ ] WHOIS checked
- [ ] Interesting domains/subdomains noted

➡️ **Next: [Phase 2 — Subdomain Enumeration](02-subdomain-enumeration.md)**
