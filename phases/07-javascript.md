# 📜 Phase 7 — JavaScript & Secrets Analysis (Hidden endpoints & keys)

### কেন করবো?

Developers প্রায়ই JS files এ API keys, internal endpoints, AWS credentials, private URLs hardcode করে রাখে। JS analysis এ এগুলো বের করা যায়।

<details>

   <summary> SecretFinder — Python JS Secret Scanner </summary> <br>

   **কী কাজ করে:** JavaScript files এ regex based pattern matching করে API keys, tokens, passwords খোঁজে।

**GitHub:** https://github.com/m4ll0k/SecretFinder

```bash

# Installation
git clone https://github.com/m4ll0k/SecretFinder.git
cd SecretFinder
pip3 install -r requirements.txt

```
```bash

# একটা JS file scan করো
python3 SecretFinder.py -i https://target.com/app.js -o cli

# Local file scan করো
python3 SecretFinder.py -i /path/to/file.js -o cli

# HTML output
python3 SecretFinder.py -i https://target.com/app.js -o results.html

```

</details>

<details>

   <summary> jsluice — Modern JavaScript URL & Secret Extractor </summary> <br>

   **কী কাজ করে:** JavaScript files এর static analysis করে URLs, endpoints, API keys, secrets বের করে। SecretFinder এর আধুনিক replacement।

**GitHub:** https://github.com/BishopFox/jsluice

```bash

# Installation
go install github.com/BishopFox/jsluice/cmd/jsluice@latest

```

```bash

# একটা JS file এ URLs extract করো
jsluice urls target.js

# Secrets extract করো (API keys, tokens)
jsluice secrets target.js

# JSON output
jsluice urls target.js | jq .

# URL থেকে directly fetch করো
curl -s https://target.com/app.js | jsluice urls
curl -s https://target.com/app.js | jsluice secrets

# Bulk — সব JS files analyze করো
cat cleaned_urls.txt | grep "\.js$" | xargs -I@ curl -s @ | jsluice urls

```
</details> <br>


> [!TIP]
> **New here?** Click ▶ **SecretFinder** or ▶ **jsluice** to explore the detailed documentation.

<br>






<!--
## ⚠️ Important

A string that looks like a secret is **not automatically a valid secret**.

Always verify findings safely and within scope.

## ✅ Checklist

- [ ] Collect JavaScript URLs
- [ ] Analyze important JS files
- [ ] Note API paths
- [ ] Note interesting configuration
- [ ] Review possible sensitive values carefully

-->
➡️ **Next: [Phase 8 — Parameter Discovery](08-parameters.md)**
