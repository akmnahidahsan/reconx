# 📂 Phase 5 — Content Discovery

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

## 🛠️ Tools

### 1. ffuf
**Use for:** Authorized web content discovery and fuzzing.

### 2. Feroxbuster
**Use for:** Fast content and recursive path discovery.

### 3. Dirsearch
**Use for:** Directory and file discovery.

## 📌 Simple Workflow

```text
Live Website
   ↓
Wordlist
   ↓
Content Discovery
   ↓
Interesting Paths
   ↓
Verify Manually
```

## 💡 Tip

Do not blindly trust every result. Check status codes, response size and the actual page.

## ✅ Checklist

- [ ] Choose an appropriate wordlist
- [ ] Run content discovery
- [ ] Remove false positives
- [ ] Manually review interesting paths
- [ ] Save useful findings

➡️ **Next: [Phase 6 — URL & Endpoint Discovery](06-url-endpoints.md)**
