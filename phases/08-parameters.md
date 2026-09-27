# ⚡ Phase 8 — Parameter Discovery (Injection points খোঁজো)


###  What is a Parameter?

Example:

```text
https://example.com/search?q=hello
                         └── q
```

Here, `q` is a parameter.

--- 

### কেন করবো?

XSS, SQLi, SSRF, IDOR এই সব vulnerabilities parameters এর মাধ্যমে exploit হয়। Hidden বা undocumented parameters বের করতে পারলে নতুন attack vectors পাওয়া যায়।

<details>

  <summary> Arjun — HTTP Parameter Discovery Tool </summary> <br>

  **কী কাজ করে:** Endpoints এ GET, POST, JSON, XML সব methods এ hidden parameters খোঁজে। 25,000+ parameter wordlist built-in আছে।

**GitHub:** https://github.com/s0md3v/Arjun

```bash

# Installation
pipx install arjun

# OR via pip
pip3 install arjun

# OR via apt
sudo apt install arjun

```

```bash

# GET parameters খোঁজো
arjun -u https://target.com/search

# POST parameters খোঁজো
arjun -u https://target.com/login -m POST

# JSON body parameters
arjun -u https://target.com/api -m JSON

# Custom wordlist
arjun -u https://target.com -w /path/to/wordlist.txt

# Multiple URLs
arjun -i urls.txt

# Output save করো
arjun -u https://target.com -o results.json

# Burp Suite export
arjun -u https://target.com -oB

# Rate limit avoid করতে delay দাও
arjun -u https://target.com --stable

```
</details>


<details>

  <summary> ParamSpider — Wayback Machine Parameter Finder </summary> <br>

  **কী কাজ করে:** Wayback Machine থেকে parameters সহ URLs collect করে। Historical data থেকে parameter names বের করে।

**GitHub:** https://github.com/devanshbatham/ParamSpider

```bash


# Installation
git clone https://github.com/devanshbatham/ParamSpider
cd ParamSpider
pip3 install -r requirements.txt

```

```bash

# Basic usage
python3 paramspider.py -d target.com

# Subdomains include
python3 paramspider.py -d target.com --subs

# Output file
python3 paramspider.py -d target.com -o params.txt

```
</details> <br> 


> [!TIP]
> **New here?** Click ▶ **Arjun** , ▶ **ParamSpider** to explore the detailed documentation.

<br>



<!--

## 💡 Tip

Parameter discovery is about **finding inputs**. It does not mean those inputs are vulnerable.

## ✅ Checklist

- [ ] Collect parameterized URLs
- [ ] Run parameter discovery where appropriate
- [ ] Remove duplicates
- [ ] Organize GET/POST/API parameters
- [ ] Save interesting inputs

-->
➡️ **Next: [Phase 9 — Vulnerability Scanning](09-vulnerability-scanning.md)**
