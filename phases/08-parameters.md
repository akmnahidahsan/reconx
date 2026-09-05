# 🎯 Phase 8 — Parameter Discovery

> **Goal:** Find parameters used by web applications.

## 🧠 What is a Parameter?

Example:

```text
https://example.com/search?q=hello
                         └── q
```

Here, `q` is a parameter.

Applications can also use parameters in:

- POST requests
- JSON bodies
- Forms
- APIs

## 🛠️ Tools

### 1. Arjun
**Use for:** Discovering potentially undocumented HTTP parameters.

### 2. ParamSpider
**Use for:** Finding parameterized URLs from public/historical sources.

## 📌 Simple Workflow

```text
Known URLs
   ↓
Find parameterized URLs
   ↓
Discover additional parameters
   ↓
Organize the results
   ↓
Review in authorized testing
```

## 💡 Tip

Parameter discovery is about **finding inputs**. It does not mean those inputs are vulnerable.

## ✅ Checklist

- [ ] Collect parameterized URLs
- [ ] Run parameter discovery where appropriate
- [ ] Remove duplicates
- [ ] Organize GET/POST/API parameters
- [ ] Save interesting inputs

➡️ **Next: [Phase 9 — Vulnerability Scanning](09-vulnerability-scanning.md)**
