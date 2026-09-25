# 🔗 Phase 6 — URL & Endpoint Discovery (সব URLs collect করো)

### কেন করবো?

Target এর সব known URLs (Wayback Machine, crawling, Google Cache) collect করলে hidden endpoints, deprecated APIs, old admin paths পাওয়া যায়। এগুলো থেকে vulnerability পাওয়ার chance বেশি।













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
