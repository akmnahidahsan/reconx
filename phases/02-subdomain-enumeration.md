# 🌐 Phase 2 — Subdomain Enumeration

> **Goal:** Find as many relevant subdomains as possible.

## কেন করবো?

Main domain এর বাইরে dev, staging, api, admin, mail — এরকম subdomains থাকতে পারে যেগুলো vulnerable। যত বেশি subdomain পাবে, তত বেশি attack surface।

Part A — Passive Subdomain Discovery (Subfinder)

### Subfinder — Industry Standard Passive Subdomain Finder

**কী কাজ করে:** 50+ passive sources (Shodan, Censys, VirusTotal, SecurityTrails ইত্যাদি) থেকে subdomains বের করে।
Target এ কোনো request যায় না।

**GitHub:** https://github.com/projectdiscovery/subfinder

### **Installation**

```

# Method 1: Go install
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest

# Verify
subfinder -version

```


## 🛠️ Tools

### 1. Subfinder
**Use for:** Passive subdomain discovery.

### 2. Amass
**Use for:** Broader attack-surface and subdomain mapping.

### 3. dnsx
**Use for:** DNS resolution and validation.

### 4. PureDNS
**Use for:** Large-scale DNS resolution and validation.

## 📌 Simple Workflow

```text
Subfinder
   ↓
Amass (optional)
   ↓
Combine results
   ↓
dnsx / PureDNS
   ↓
Valid DNS names
```

## 💡 Remember

Finding a subdomain does **not** mean it is a live website.

That is why we verify the results in the next phase.

## ✅ Checklist

- [ ] Run Subfinder
- [ ] Add Amass results if needed
- [ ] Remove duplicates
- [ ] Resolve discovered names
- [ ] Save valid results

➡️ **Next: [Phase 3 — HTTP Probing](03-http-probing.md)**
