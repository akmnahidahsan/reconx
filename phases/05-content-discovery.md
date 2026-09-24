# 📂 Phase 5 — Content & Directory Discovery ( Hidden files খোঁজো )

<!--

> **Goal:** Find publicly reachable directories, files and application paths.

## 🧠 Why?

A website may contain more than what appears in the main navigation.

Example:

```text
/
├── login
├── admin
├── api
├── uploads
└── assets
```
-->
### কেন করবো?

Developers অনেক সময় admin panels, backup files (.bak, .old), config files, API endpoints publicly accessible রেখে দেয়। Wordlist দিয়ে brute force করে এগুলো বের করো।

<details>

   <summary> ffuf — Fast Web Fuzzer (Industry Standard) </summary> <br>

   **কী কাজ করে:** Wordlist দিয়ে directory, file, parameter, header সব কিছু fuzz করতে পারে। Go তে লেখা তাই অনেক fast।

**GitHub:** https://github.com/ffuf/ffuf

```bash

# Installation
go install github.com/ffuf/ffuf/v2@latest

# OR
sudo apt install ffuf

```

```bash

# Basic directory brute force
ffuf -u https://target.com/FUZZ -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt

# Extensions সহ
ffuf -u https://target.com/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-medium-words.txt -e .php,.html,.txt,.bak,.js

# Status code filter করো (404 বাদ)
ffuf -u https://target.com/FUZZ -w wordlist.txt -fc 404

# Size filter করো
ffuf -u https://target.com/FUZZ -w wordlist.txt -fs 1234

# POST request fuzz করো
ffuf -u https://target.com/login -w wordlist.txt -X POST -d "username=FUZZ&password=test"

# Subdomain fuzz করো
ffuf -u https://FUZZ.target.com -w subdomains.txt -H "Host: FUZZ.target.com"

# Output save করো
ffuf -u https://target.com/FUZZ -w wordlist.txt -o results.json -of json

# Burp Suite এর মাধ্যমে route করো
ffuf -u https://target.com/FUZZ -w wordlist.txt -x http://127.0.0.1:8080

```
</details>

<details>

   <summary> Feroxbuster — Fast Recursive Directory Buster (Rust) </summary> <br>
   
   **কী কাজ করে:** Rust এ লেখা তাই ffuf এর চেয়েও faster। Recursive directory scan automatically করে। Bug bounty তে খুব popular।

**GitHub:** https://github.com/epi052/feroxbuster

```bash

# Installation
sudo apt install feroxbuster

# OR via cargo (Rust package manager)
cargo install feroxbuster

```

```bash

# Basic scan
feroxbuster -u https://target.com

# Custom wordlist সহ
feroxbuster -u https://target.com -w /usr/share/seclists/Discovery/Web-Content/raft-medium-words.txt

# Extensions সহ
feroxbuster -u https://target.com -x php,html,txt,bak,js -w wordlist.txt

# Thread count set করো
feroxbuster -u https://target.com -t 50 -w wordlist.txt

# Status codes filter করো
feroxbuster -u https://target.com -s 200,301,302 -w wordlist.txt

# Burp Suite proxy route করো
feroxbuster -u https://target.com --proxy http://127.0.0.1:8080 --insecure

# Output save করো
feroxbuster -u https://target.com -o results.txt

# File থেকে multiple targets
cat live_hosts.txt | feroxbuster --stdin

```
</details>

<details>

   <summary> dirsearch — Python Directory Scanner </summary> <br>

   **কী কাজ করে:** Python based directory scanner। Use করা সহজ, built-in wordlist আছে। Beginners এর জন্য ভালো।

**GitHub:** https://github.com/maurosoria/dirsearch

```bash

# Installation
pip3 install dirsearch

# OR
sudo apt install dirsearch

```

```bash

# Basic scan
dirsearch -u https://target.com

# Custom wordlist
dirsearch -u https://target.com -w /path/to/wordlist.txt

# Extensions set করো
dirsearch -u https://target.com -e php,html,txt,bak

# Multiple targets
dirsearch -l live_hosts.txt

# Output save করো
dirsearch -u https://target.com -o results.txt
```
</details> <br>

> [!TIP]
> **New here?** Click ▶ **ffuf** , ▶ **Feroxbuster**, ▶ **dirsearch** to explore the detailed documentation.

<br>


<!--
## 💡 Tip

Do not blindly trust every result. Check status codes, response size and the actual page.

## ✅ Checklist

- [ ] Choose an appropriate wordlist
- [ ] Run content discovery
- [ ] Remove false positives
- [ ] Manually review interesting paths
- [ ] Save useful findings
-->

➡️ **Next: [Phase 6 — URL & Endpoint Discovery](06-url-endpoints.md)**
