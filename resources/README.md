# 📚  Essential Wordlists & Resources
<br>


## SecLists — The Ultimate Wordlist Collection
**কী আছে:** Usernames, passwords, URLs, directories, subdomains, fuzzing payloads — সব ধরনের wordlist এক জায়গায়।

**GitHub:** https://github.com/danielmiessler/SecLists

```bash

# Installation
sudo apt install seclists

# OR manually
git clone https://github.com/danielmiessler/SecLists.git /usr/share/seclists

```

**Useful paths:**

```bash
/usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt  → Directory brute force
/usr/share/seclists/Discovery/Web-Content/raft-medium-words.txt          → Better directory list
/usr/share/seclists/Discovery/DNS/subdomains-top1million-20000.txt       → Subdomain brute force
/usr/share/seclists/Fuzzing/                                             → XSS, SQLi payloads
```


### 📦 PayloadBox — Vulnerability Specific Payloads

**Link:** https://github.com/payloadbox

### Additional Resources

- Web Recon Guide: https://dhiyaneshgeek.github.io/bug/bounty/2020/02/06/recon-with-me/
- Recon Methodology: https://github.com/pr0xh4ck/web-recon



