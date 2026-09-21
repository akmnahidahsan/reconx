# ✅ Phase 3 — Active Probing & Verification (কোনগুলো live আছে?)
    
### কেন করবো?
    
Hundreds বা thousands of subdomains পাওয়ার পর verify করতে হবে কোনগুলো actually HTTP/HTTPS serve করছে। Dead domains এ সময় নষ্ট না করে শুধু live ones এ focus করো।

<details>

   <summary> httpx — Fast Multi-purpose HTTP Toolkit (Industry Standard) </summary> <br>

   **কী কাজ করে:** Subdomain list নিয়ে প্রতিটায় HTTP request পাঠায়, কোনগুলো live তা verify করে। Status code, title, technology stack, screenshot সব দেয়।

**GitHub:** https://github.com/projectdiscovery/httpx

```bash

# Installation
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest

# Verify
httpx -version

```

```bash

# Basic — live hosts filter করো
cat subdomains.txt | httpx

# Title, status code, tech detect সহ (সবচেয়ে ভালো command)
cat subdomains.txt | httpx -title -status-code -tech-detect

# Multiple ports check করো
cat subdomains.txt | httpx -title -status-code -tech-detect -p 80,443,8080,8443,8888

# Subfinder → httpx directly
subfinder -d target.com -silent | httpx -title -status-code -tech-detect -o live_hosts.txt

# Full recon pipeline (Subfinder → dnsx → httpx)
subfinder -d target.com -silent | dnsx -silent | httpx -title -status-code -tech-detect -o live_hosts.txt

# Screenshot নাও (gowitness needed)
httpx -l subdomains.txt -screenshot

# JSON output
httpx -l subdomains.txt -json -o results.json

# Specific status code filter করো
httpx -l subdomains.txt -mc 200,301,302,403

```
   
</details>

<details>

   <summary> Visualization — gowitness (Screenshots of live hosts) </summary> <br>

   **কী কাজ করে:** প্রতিটি live host এর screenshot নেয়। একটা HTML report তৈরি করে সব screenshot দিয়ে। Manually review করতে সুবিধা হয়।

**GitHub:** https://github.com/sensepost/gowitness

```bash

# Installation
go install github.com/sensepost/gowitness@latest

# File থেকে screenshot নাও
gowitness scan file -f live_hosts.txt

# Report দেখো
gowitness report serve
# Browser এ যাও: http://localhost:7171

```

</details> <br>


> [!TIP]
> **New here?** Click ▶ **httpx** or ▶ **Visualization** to explore the detailed documentation.

<br>

<!--
## 📌 Simple Workflow

```text
Subdomains
   ↓
HTTPX
   ↓
Live web hosts
   ↓
Gowitness (optional)
   ↓
Visual review
```



## 📄 Useful Output

Keep information such as:

- URL
- Status code
- Page title
- Technology hints

## ✅ Checklist

- [ ] Probe discovered hosts
- [ ] Separate live from dead hosts
- [ ] Record status codes
- [ ] Record page titles
- [ ] Screenshot interesting hosts if needed

-->

➡️ **Next: [Phase 4 — Technology Fingerprinting](04-technology.md)**
