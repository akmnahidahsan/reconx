# 🔗 Phase 6 — URL & Endpoint Discovery (সব URLs collect করো)

### কেন করবো?

Target এর সব known URLs (Wayback Machine, crawling, Google Cache) collect করলে hidden endpoints, deprecated APIs, old admin paths পাওয়া যায়। এগুলো থেকে vulnerability পাওয়ার chance বেশি।

<br>
<details>

 <summary> Katana — Next-Gen Web Crawler (Modern Standard) </summary> <br>

 **কী কাজ করে:** Modern web apps crawl করতে পারে। JavaScript parse করে, headless browser support আছে। SPAs এর জন্যও কাজ করে।

**GitHub:** https://github.com/projectdiscovery/katana

```bash

# Installation
go install github.com/projectdiscovery/katana/cmd/katana@latest

```

```bash

# Basic crawl
katana -u https://target.com

# JavaScript parsing সহ (JS apps এর জন্য)
katana -u https://target.com -jc

# Headless mode (dynamic sites)
katana -u https://target.com -headless

# Depth set করো
katana -u https://target.com -d 5

# Output save করো
katana -u https://target.com -jc -o crawled_urls.txt

# Multiple targets
cat live_hosts.txt | katana -jc -o all_urls.txt

# Scope limit করো
katana -u https://target.com -jc -fs rdn

```

</details>

<details>

 <summary> gau — Get All URLs (Historical + Public Sources) </summary> <br>

 **কী কাজ করে:** AlienVault OTX, Wayback Machine, Common Crawl এবং URLScan থেকে historically crawled URLs collect করে। Target এ কোনো request যায় না।

**GitHub:** https://github.com/lc/gau

```bash

# Installation
go install github.com/lc/gau/v2/cmd/gau@latest

```

```bash

# Basic usage
gau target.com

# File এ save করো
gau target.com > gau_urls.txt

# Extensions filter করো
gau target.com --o js,php,aspx

# Multiple threads
gau target.com --threads 10

# Subdomain include করো
gau --subs target.com

```
</details>

<details>

 <summary> waybackurls — Wayback Machine URL Fetcher </summary> <br>

 **কী কাজ করে:** Wayback Machine এ archive হওয়া সব URLs বের করে। পুরনো endpoints, deprecated APIs খুঁজে পাওয়া যায়।

**GitHub:** https://github.com/tomnomnom/waybackurls

```bash

# Installation
go install github.com/tomnomnom/waybackurls@latest

```

```bash

# Basic usage
echo "target.com" | waybackurls

# File এ save করো
echo "target.com" | waybackurls > wayback_urls.txt

# Sort করো এবং unique রাখো
echo "target.com" | waybackurls | sort -u > unique_urls.txt

```
</details>

<details>

 <summary> hakrawler — Simple & Fast Web Crawler </summary> <br>

 **কী কাজ করে:** Simple Go-based crawler যা links, forms, JavaScript files quickly extract করে।

**GitHub:** https://github.com/hakluke/hakrawler

```bash

# Installation
go install github.com/hakluke/hakrawler@latest

```

```bash

# Basic crawl
echo https://target.com | hakrawler

# Depth set করো
echo https://target.com | hakrawler -d 3

# Subdomains include
echo https://target.com | hakrawler -subs

# Plain output
echo https://target.com | hakrawler -plain

```
</details>

<details>

 <summary> 💡 Combined URL Collection Workflow </summary> <br> 

 ```bash

# সব sources থেকে URLs collect করো
echo "target.com" | waybackurls > all_urls.txt
gau target.com >> all_urls.txt
katana -u https://target.com -jc >> all_urls.txt

# Cleanup করো — duplicates বাদ, images/css বাদ
cat all_urls.txt | sort -u | grep -ivE "\.(jpg|jpeg|gif|png|css|woff|woff2|svg|pdf|ico|ttf|eot)$" > cleaned_urls.txt

# কতটা পেলে?
wc -l cleaned_urls.txt
```
</details> <br>

> [!TIP]
> **New here?** Click ▶ **Katana**, ▶ **gau**, ▶ **waybackurls**, ▶ **hakrawler**, ▶ **Combined URL Collection Workflow** to explore the detailed documentation.

<br>
<br>






<!--

```text
Historical Sources
       +
    Crawling
       ↓
   URL Collection
       ↓
 Remove duplicates
       ↓
 Interesting endpoints
```

## 📄 Look for

```text
/api/
/login
/upload
/graphql
/admin
```

These are examples of **paths to investigate**, not proof that something is vulnerable.

## ✅ Checklist

- [ ] Collect historical URLs
- [ ] Crawl the application
- [ ] Combine results
- [ ] Remove duplicates
- [ ] Review interesting endpoints

-->
➡️ **Next: [Phase 7 — JavaScript Analysis](07-javascript.md)**
