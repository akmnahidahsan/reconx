# 📄 Phase 0 — Prerequisites (First-Time Setup)

### কেন দরকার?

ReconX-এর অনেকগুলো reconnaissance tool Go-based, আর কিছু tool Python ও অন্যান্য common command-line dependencies ব্যবহার করে।  
তাই প্রথমবার কাজ শুরু করার আগে basic environment setup করে নেওয়া দরকার।

একবার এগুলো properly setup করা হলে পরবর্তী phase-গুলোর প্রয়োজনীয় tool সহজেই install ও use করা যাবে।

---

### 🔧 Install Go (Linux/Kali)

Go-based toolগুলো install এবং run করার জন্য Go প্রয়োজন।

```bash
# Update packages
sudo apt update && sudo apt upgrade -y

# Install Go
sudo apt install golang-go -y

# Verify installation
go version

# Add Go bin to PATH
export PATH=$PATH:$(go env GOPATH)/bin

# Reload shell
source ~/.bashrc

```
</br>

## 🔧 Install Common Dependencies

Recon workflow-এর বিভিন্ন tool install ও ব্যবহার করার জন্য কিছু common dependency আগে থেকেই থাকা ভালো।

```bash
# Python and pip (for Python-based tools)
sudo apt install python3 python3-pip pipx -y

# Git (for cloning repositories)
sudo apt install git -y

# curl and wget
sudo apt install curl wget -y

```
</br>

## 🔎 Quick Verification
সবকিছু ঠিকভাবে install হয়েছে কিনা check করতে:
```bash
go version
python3 --version
git --version
curl --version
wget --version

```

>**💡Note:** Kali Linux-এর recent versions-এ কিছু package আগে থেকেই installed থাকতে পারে। তাই কোনো dependency already installed থাকলে আবার install করার প্রয়োজন নেই।

## ✅ Phase 0 Checklist

- [ ] Linux/Kali ready
- [ ] Git installed
- [ ] Python installed
- [ ] Go installed
- [ ] curl installed
- [ ] wget installed
- [ ] Go PATH configured
- [ ] Recon workspace created
- [ ] Target scope confirmed

## 🎯 Phase 0 Complete

Your environment is ready.

➡️ **Next: [Phase 1 — Passive Recon](01-passive-recon.md)**
