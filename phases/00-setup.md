# ⚙️ Phase 0 — Setup

> **Goal:** Get your basic environment ready before starting reconnaissance.

## 🧠 Why Start Here?

Before doing recon, make sure your system has the basic tools required.

## 💻 Recommended Environment

- Linux / Kali Linux
- Git
- Python 3
- Go
- curl
- wget

## 🔧 Step 1 — Update Your System

```bash
sudo apt update
```

## 🔧 Step 2 — Install Basic Tools

```bash
sudo apt install git curl wget python3 golang-go -y
```

## 🔎 Step 3 — Check Everything

```bash
git --version
python3 --version
go version
curl --version
wget --version
```

If the commands return version information, your basic environment is ready.

## 🛠️ Step 4 — Prepare Go Tools

Many modern reconnaissance tools are distributed through Go.

```bash
export PATH="$PATH:$(go env GOPATH)/bin"
```

## 📁 Step 5 — Create a Workspace

```bash
mkdir -p ~/recon
cd ~/recon
```

Example:

```text
recon/
├── targets/
├── results/
└── notes/
```

## ⚠️ Step 6 — Confirm Your Scope

Before running any recon tool:

- [ ] I own the target
- [ ] OR I have explicit permission
- [ ] OR the target is an authorized CTF/lab
- [ ] OR the target is explicitly in a bug-bounty scope
- [ ] I understand the allowed testing methods

**Never skip this step.**

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
