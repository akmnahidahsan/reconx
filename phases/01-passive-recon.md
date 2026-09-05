# 🔍 Phase 1 — Passive Recon

> **Goal:** Find information about the target without directly interacting with the application as much as possible.

## 🧠 What is Passive Recon?

Passive recon means collecting information from **publicly available sources**.

Think of it as:

> “What can I learn about this target before touching the target?”

## 🛠️ Tools

### 1. Censys
**Use for:** Internet-facing hosts, services and certificates.

### 2. Shodan
**Use for:** Publicly indexed services, ports and banners.

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
