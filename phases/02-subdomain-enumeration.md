# 🌐 Phase 2 — Subdomain Enumeration

> **Goal:** Find as many relevant subdomains as possible.

## 🧠 What is a Subdomain?

Example:

```text
example.com
api.example.com
admin.example.com
dev.example.com
```

`api`, `admin`, and `dev` are subdomains.

## 🛠️ Tools

### 1. Subfinder
**Use for:** Passive subdomain discovery.

### 2. Amass
**Use for:** Broader attack-surface and subdomain mapping.

### 3. dnsx
**Use for:** DNS resolution and validation.

### 4. PureDNS
**Use for:** Large-scale DNS resolution and validation.

## 📌 Simple Workflow

```text
Subfinder
   ↓
Amass (optional)
   ↓
Combine results
   ↓
dnsx / PureDNS
   ↓
Valid DNS names
```

## 💡 Remember

Finding a subdomain does **not** mean it is a live website.

That is why we verify the results in the next phase.

## ✅ Checklist

- [ ] Run Subfinder
- [ ] Add Amass results if needed
- [ ] Remove duplicates
- [ ] Resolve discovered names
- [ ] Save valid results

➡️ **Next: [Phase 3 — HTTP Probing](03-http-probing.md)**
