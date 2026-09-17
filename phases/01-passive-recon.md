## 🔎 Phase 1 — Passive Recon & OSINT (Target এ কোনো request পাঠাবে না)

### কেন করবো?

Target এ সরাসরি কোনো traffic না পাঠিয়ে publicly available তথ্য দিয়ে target সম্পর্কে ধারণা নেওয়া।  
IP ranges, ASN, registration info, DNS records এবং অন্যান্য public information এখান থেকে বের করা যায়।

---

### 🌐 Online Tools (No Install Needed)

<details>
<summary>▶ Censys — Internet-wide scanner database</summary>

### কী কাজে করে?

Internet-এর publicly accessible device/server-এর information খুঁজে দেখা যায়।  
Port, certificate, service এবং অন্যান্য information পাওয়া যেতে পারে।

**Link:** https://search.censys.io/

**Usage:**

```

Site: search.censys.io

Search: "target.com" — IP ranges, ports, certificates বের হবে
Search: ip:1.2.3.4 — specific IP-এর info

```
</details>

<details> <summary>▶ Shodan — Search engine for IoT & servers</summary>

### কী কাজে করে?

Internet এ exposed services, ports এবং banners search করা যায়।
Target-এর server কোন software run করছে সেটাও দেখা যেতে পারে।

**Link:** https://www.shodan.io/

**Usage:**

```

Site: shodan.io

Search: hostname:"target.com" — সব subdomains + ports
Search: org:"Company Name" — company-এর সব IP
Search: ssl:"target.com" — SSL certificate দিয়ে search

```
</details>

<details> <summary>▶ DNSDumpster — DNS records mapper</summary>
  
### কী কাজে করে?

Domain-এর DNS records (A, MX, TXT, NS) এবং subdomains visualize করা যায়।
প্রয়োজনে information export-ও করা যায়।

**Link:** https://dnsdumpster.com/

**Usage:**

```

Site এ গিয়ে domain দাও → DNS map এবং list পাবে

```
</details>

<details> <summary>▶ Whois — Domain ownership & registration info</summary>
  
### কী কাজে করে?

Domain কে register করেছে, কখন register করা হয়েছে, registrar কে এবং কোন nameserver ব্যবহার করা হচ্ছে—এই ধরনের registration information পাওয়া যায়।

**Link:** https://www.whois.com/

**Command (Terminal):**

```

whois target.com

```
</details>

<details> <summary>▶ ViewDNS — Multiple DNS lookups in one place</summary>
  
### কী কাজে করে?

Reverse IP lookup, DNS propagation check, IP history এবং আরও অনেক ধরনের DNS-related information এক জায়গা থেকে দেখা যায়।

**Link:** https://viewdns.info/

**Useful queries:**
```

Reverse IP → একটি IP-এর সাথে কোন কোন domain আছে

IP History → Domain-এর আগের IP গুলো (origin IP বের করতে কাজে আসে)

```
</details>

<br>

## 📌 Simple Workflow

```
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
