# 🚀 GitHub Deployment Guide

## ✅ ČO POTREBUJEŠ:

1. **GitHub účet** (zadarmo na github.com)
2. **Git** nainštalovaný (git-scm.com)
3. **Tento projekt** (už máš!)

---

## 📦 KROK 1: Priprav Súbory

### **Štruktúra projektu:**
```
crypto-analyzer-ultimate/
├── README.md                          ← Hlavný návod
├── LICENSE                            ← MIT license
├── .gitignore                         ← Čo NEnahrávať
├── docker-compose.yml                 ← Docker config
├── index.html                         ← Main aplikácia
└── docs/                              ← Dokumentácia
    ├── INSTALLATION.md
    ├── TELEGRAM-SETUP.md
    ├── ADX-GUIDE.md
    └── screenshots/
        ├── watchlist.png
        └── detail-view.png
```

### **Súbory ktoré SOM TI VYTVORIL:**
```
✅ README-GITHUB.md → premenuj na README.md
✅ LICENSE
✅ .gitignore
✅ index.html (crypto-analyzer-ultimate.html)
✅ docker-compose.yml (už máš)
```

---

## 🔧 KROK 2: Vytvor GitHub Repo

### **1. Cez Web Interface:**

1. Choď na https://github.com
2. Klikni **"+"** (hore vpravo) → **"New repository"**
3. Vyplň:
   ```
   Repository name: crypto-analyzer-ultimate
   Description: Advanced crypto trading analyzer with multi-TF analysis & S/R detection
   ☑️ Public (alebo Private ak chceš)
   ☐ Add README (my už máme)
   ☐ Add .gitignore (my už máme)
   ☐ Choose license (my už máme)
   ```
4. Klikni **"Create repository"**

---

## 💻 KROK 3: Upload Súborov

### **Option A: Git Command Line** (Recommended)

```bash
# 1. Prejdi do priečinka s projektom
cd /opt/stacks/crypto-analyzer
# alebo kde máš súbory

# 2. Inicializuj git
git init

# 3. Pridaj súbory
git add .

# 4. Commit
git commit -m "Initial commit - Crypto Analyzer Ultimate v4.0"

# 5. Pripoj GitHub repo (NAHRAĎ YOUR-USERNAME!)
git remote add origin https://github.com/YOUR-USERNAME/crypto-analyzer-ultimate.git

# 6. Push
git branch -M main
git push -u origin main
```

### **Option B: GitHub Web Upload**

1. Na GitHub repo stránke klikni **"uploading an existing file"**
2. Drag & drop všetky súbory
3. Commit message: "Initial commit"
4. Klikni **"Commit changes"**

---

## 📝 KROK 4: Upraviť README

1. Otvor `README.md` na GitHube
2. Klikni **✏️ Edit**
3. **NAHRAĎ**:
   ```markdown
   git clone https://github.com/YOUR-USERNAME/crypto-analyzer-ultimate.git
   ```
   
   **S tvojím username:**
   ```markdown
   git clone https://github.com/TvojUsername/crypto-analyzer-ultimate.git
   ```

4. Commit changes

---

## 🖼️ KROK 5: Pridať Screenshots (Voliteľné)

### **Kde získať screenshots:**

1. Otvor aplikáciu: http://localhost:8080
2. Urob screenshot:
   - **Watchlist**: Hlavná obrazovka
   - **Detail View**: Graf s S/R levelmi
   - **Telegram Alert**: Screenshot z Telegramu
   
3. Ulož do `/docs/screenshots/`

4. Upload na GitHub:
   ```bash
   git add docs/screenshots/
   git commit -m "Add screenshots"
   git push
   ```

---

## ⚙️ KROK 6: GitHub Pages (Voliteľné)

**Publikuj app ZADARMO na GitHub Pages!**

### **1. Aktivuj Pages:**

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from branch**
3. Branch: **main** / **root**
4. Save

### **2. Počkaj 1-2 minúty**

### **3. Otvor:**
```
https://YOUR-USERNAME.github.io/crypto-analyzer-ultimate/
```

**BOOM! Tvoja app je LIVE! 🚀**

---

## 🏷️ KROK 7: Releases (Voliteľné)

### **Vytvor prvý release:**

1. Repo → **Releases** → **Create a new release**
2. Tag: `v4.0.0`
3. Title: `v4.0.0 - ADX Edition`
4. Description:
   ```markdown
   ## 🎉 Features
   - ✅ Multi-coin watchlist
   - ✅ ADX indicator
   - ✅ S/R detection & visualization
   - ✅ Smart Telegram alerts
   - ✅ Backtesting engine
   ```
5. Attach: `crypto-analyzer-ultimate.zip` (optional)
6. **Publish release**

---

## 📊 KROK 8: Add Topics/Tags

1. Repo page → **⚙️ (cog)** vedľa About
2. Pridaj topics:
   ```
   cryptocurrency
   trading
   binance
   telegram-bot
   technical-analysis
   react
   chart
   day-trading
   backtesting
   ```
3. Save

---

## 🎯 HOTOVO! ✅

**Tvoj repo je LIVE!**

### **URLs:**
```
Repo: https://github.com/YOUR-USERNAME/crypto-analyzer-ultimate
Live App: https://YOUR-USERNAME.github.io/crypto-analyzer-ultimate/
```

### **Zdieľaj:**
```
Twitter: "Just released my crypto analyzer! 🚀 Check it out:"
Reddit: r/cryptocurrency, r/CryptoTechnology
Discord: Trading communities
```

---

## 🔄 Budúce Updates

### **Pri zmene kódu:**

```bash
# 1. Uprav súbory
nano index.html

# 2. Commit
git add .
git commit -m "Add new feature: XYZ"

# 3. Push
git push

# 4. Vytvor nový release (optional)
# Repo → Releases → Draft new release
# Tag: v4.1.0
```

---

## 💡 Pro Tips

### **1. README Badges:**
```markdown
![Version](https://img.shields.io/badge/version-4.0.0-blue)
![Stars](https://img.shields.io/github/stars/YOUR-USERNAME/crypto-analyzer-ultimate)
![Issues](https://img.shields.io/github/issues/YOUR-USERNAME/crypto-analyzer-ultimate)
```

### **2. Contribution Guide:**
Create `CONTRIBUTING.md`:
```markdown
# Contributing
1. Fork repo
2. Create branch: `git checkout -b feature/amazing`
3. Commit: `git commit -m 'Add amazing feature'`
4. Push: `git push origin feature/amazing`
5. Open Pull Request
```

### **3. Issue Templates:**
Settings → Features → Issues → Set up templates
- Bug report
- Feature request

### **4. GitHub Actions (CI/CD):**
Auto-deploy when you push!
`.github/workflows/deploy.yml`

---

## 📞 Pomoc

**Problémy?**
- Git tutorial: https://git-scm.com/docs/gittutorial
- GitHub Docs: https://docs.github.com
- Alebo sa opýtaj mňa! 😊

---

**Good luck s GitHub!** 🚀

Keď to nahráš, pošli mi link - rád sa pozriem! 👀
