# 🌐 Phase 2 — Subdomain Enumeration

> **Goal:** Find as many relevant subdomains as possible.

## কেন করবো?

Main domain এর বাইরে dev, staging, api, admin, mail — এরকম subdomains থাকতে পারে যেগুলো vulnerable। যত বেশি subdomain পাবে, তত বেশি attack surface।


<details>

<summary> Part A — Passive Subdomain Discovery (Subfinder) </summary>

### Subfinder — Industry Standard Passive Subdomain Finder

### কী কাজ করে: 
50+ passive sources (Shodan, Censys, VirusTotal, SecurityTrails ইত্যাদি) থেকে subdomains বের করে।
Target এ কোনো request যায় না।

**GitHub:** https://github.com/projectdiscovery/subfinder

### **Installation**

```

# Method 1: Go install
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest

# Verify
subfinder -version

```

## API Keys Setup (provider-config.yaml)

**File location:** ```~/.config/subfinder/provider-config.yaml```

```

# First run subfinder once to generate config file
subfinder -d example.com

# Then edit the config file
nano ~/.config/subfinder/provider-config.yaml

```

```
# ~/.config/subfinder/provider-config.yaml
# শুধু যেগুলোর key আছে সেগুলো fill করো, বাকিগুলো [] রাখো
bevigil: [YOUR_BEVIGIL_KEY]
builtwith: [YOUR_BUILTWITH_KEY]
censys: [API_ID:SECRET]
certspotter: [YOUR_CERTSPOTTER_KEY]
chaos: [YOUR_CHAOS_KEY]
fullhunt: [YOUR_FULLHUNT_KEY]
github: [YOUR_GITHUB_TOKEN]
intelx: [2.intelx.io:YOUR_INTELX_KEY]
redhuntlabs: [https://reconapi.redhuntlabs.com/community/v1/domains/subdomains:YOUR_KEY]
securitytrails: [YOUR_SECURITYTRAILS_KEY]
shodan: [YOUR_SHODAN_KEY]
virustotal: [YOUR_VIRUSTOTAL_KEY]
whoisxmlapi: [YOUR_WHOISXMLAPI_KEY]
zoomeyeapi: [YOUR_ZOOMEYE_KEY]
# NOTE: BinaryEdge shutdown হয়েছে (March 2025), BufferOver inactive

```

## Usage Commands

```

# Basic scan
subfinder -d target.com

# Save to file
subfinder -d target.com -o subdomains.txt

# All sources use করো (API keys থাকলে)
subfinder -d target.com -all -o subdomains.txt

# Multiple domains
subfinder -dL domains.txt -o subdomains.txt

# Silent mode (শুধু results, no extra output)
subfinder -d target.com -silent

# JSON output
subfinder -d target.com -oJ -o subdomains.json

# Available sources দেখো
subfinder -ls

```

## 🔑 Free API Keys Registration Guide

| Provider | Free Limit | Sign Up | API Key Location | Notes
|---|---|---|---|---|
| :--- | :--- | :--- | :--- | :--- |
| BeVigil | 25-50 credits/month | https://bevigil.com/ | Dashboard → API Keys | Email দিয়ে signup করো |
| BuiltWith | Limited | [builtwith.com/signup](https://builtwith.com/signup) | https://api.builtwith.com/ | Tempmail use করবে না |
| Censys | 250 queries/month | https://search.censys.io/ | Account → API | Format: ```API_ID:SECRET``` |


</details>













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
