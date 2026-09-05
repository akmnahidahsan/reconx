# 📜 Phase 7 — JavaScript Analysis

> **Goal:** Learn what the application's JavaScript files reveal.

## 🧠 Why?

JavaScript can contain useful information such as:

- API paths
- Endpoint names
- Configuration values
- Client-side routes
- References to third-party services

## 🛠️ Tools

### 1. SecretFinder
**Use for:** Searching JavaScript for patterns that may indicate sensitive values.

### 2. JSluice
**Use for:** Extracting interesting URLs, endpoints and strings from JavaScript.

## 📌 Simple Workflow

```text
Collected URLs
   ↓
Find .js files
   ↓
Analyze JavaScript
   ↓
Extract interesting strings
   ↓
Review manually
```

## ⚠️ Important

A string that looks like a secret is **not automatically a valid secret**.

Always verify findings safely and within scope.

## ✅ Checklist

- [ ] Collect JavaScript URLs
- [ ] Analyze important JS files
- [ ] Note API paths
- [ ] Note interesting configuration
- [ ] Review possible sensitive values carefully

➡️ **Next: [Phase 8 — Parameter Discovery](08-parameters.md)**
