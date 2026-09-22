# 🧩 Phase 4 — Technology Fingerprinting (Target কোন tech use করছে?)

### কেন করবো?

Target কোন framework, CMS, server, JS library use করছে জানলে সেই specific technology এর vulnerabilities খোঁজা যায়। WordPress? → WordPress-specific bugs খোঁজো।

<details>

   <summary> Wappalyzer — Browser Extension (Easiest) </summary> <br>

   **কী কাজ করে:** Browser extension হিসেবে install করলে যেকোনো website visit করলে সাথে সাথে tech stack দেখায়।

**Install:** Chrome/Firefox এ "Wappalyzer" extension install করো

**Link:** https://www.wappalyzer.com/


</details> 

<details>

   <summary> WhatWeb — Command Line Tech Fingerprinter </summary> <br>

   **কী কাজ করে:** Website এর server headers, HTML, cookies analyze করে technology বের করে।

**GitHub:** https://github.com/urbanadventurer/whatweb

```bash

# Installation
sudo apt install whatweb

# Basic scan
whatweb https://target.com

# Verbose output
whatweb -v https://target.com

# Multiple targets
whatweb -i live_hosts.txt --log-brief=results.txt

# Aggression level (1-4, বেশি = বেশি request)
whatweb -a 3 https://target.com

```
</details>

<details>

   <summary> BuiltWith — Business Tech Stack Identifier </summary> <br> 

   **কী কাজ করে:** Website এর technology stack history সহ দেখায়। আগে কী use করতো এখন কী করছে।

**Link:** https://builtwith.com/

   
</details> <br>

> [!TIP]
> **New here?** Click ▶ **Wappalyzer** , ▶ **WhatWeb**, ▶ **BuiltWith** to explore the detailed documentation.

<br>







<!--

## ⚠️ Important

Technology detection is **not proof of a vulnerability**.

It is information that helps you decide what to investigate next.

## ✅ Checklist

- [ ] Identify web server
- [ ] Identify framework/CMS
- [ ] Note interesting technologies
- [ ] Record versions when reliably exposed

-->

➡️ **Next: [Phase 5 — Content Discovery](05-content-discovery.md)**
