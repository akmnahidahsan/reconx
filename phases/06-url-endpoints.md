# 🔗 Phase 6 — URL & Endpoint Discovery (সব URLs collect করো)

### কেন করবো?

Target এর সব known URLs (Wayback Machine, crawling, Google Cache) collect করলে hidden endpoints, deprecated APIs, old admin paths পাওয়া যায়। এগুলো থেকে vulnerability পাওয়ার chance বেশি।

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

➡️ **Next: [Phase 7 — JavaScript Analysis](07-javascript.md)**
