# ✅ Phase 3 — HTTP Probing

> **Goal:** Find which discovered hosts actually have a reachable web service.

## 🧠 Why?

You may discover 500 subdomains, but only some may respond over HTTP/HTTPS.

So now we ask:

> “Which ones are alive?”

## 🛠️ Tools

### 1. httpx
**Use for:** HTTP/HTTPS probing, status codes, titles and useful metadata.

### 2. Gowitness
**Use for:** Taking screenshots of reachable web services.

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

➡️ **Next: [Phase 4 — Technology Fingerprinting](04-technology.md)**
