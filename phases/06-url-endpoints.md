# 🔗 Phase 6 — URL & Endpoint Discovery

> **Goal:** Build a larger list of known URLs and endpoints.

## 🧠 Why?

Historical URLs and crawled URLs can reveal functionality that is not obvious from the homepage.

## 🛠️ Tools

### 1. Katana
**Use for:** Web crawling and endpoint discovery.

### 2. GAU
**Use for:** Collecting URLs from public/historical sources.

### 3. Waybackurls
**Use for:** Finding archived URLs.

### 4. Hakrawler
**Use for:** Simple link and endpoint crawling.

## 📌 Simple Workflow

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
