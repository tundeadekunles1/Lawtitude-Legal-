# Lawtitude Legal — Website

> Legal & Project Support for SMEs | Nigeria · US · UK · Canada

---

## 🗂️ Repo Structure

```
lawtitude-legal/
├── index.html                        ← Main site entry point
├── Lawtitude-Legal_files/
│   ├── index-Dac3WYdf.css            ← Styles
│   ├── index-vHQ8ZZr7.js             ← JS bundle
│   └── _flock.js                     ← Analytics
└── .github/
    └── workflows/
        └── deploy.yml                ← CI/CD pipeline
```

---

## 🚀 Deployment Pipeline

**Push to `main`** → GitHub Actions triggers → FTP deploy to **cPanel on GCP**

### GitHub Secrets Required

Go to **Settings → Secrets and variables → Actions** and add:

| Secret | Value |
|---|---|
| `FTP_HOST` | GCP VM external IP (e.g. `34.x.x.x`) |
| `FTP_USERNAME` | cPanel FTP account username |
| `FTP_PASSWORD` | cPanel FTP account password |
| `FTP_PORT` | `21` (FTP) or `22` (SFTP) |
| `REMOTE_DIR` | `/public_html/` |

---

## 🛠️ Local Setup

```bash
git clone https://github.com/YOUR_USERNAME/lawtitude-legal.git
cd lawtitude-legal

# Open in browser
open index.html
```

## 📦 Deploy

```bash
git add .
git commit -m "your message"
git push origin main
# ↑ This triggers auto-deploy to cPanel
```

---

© 2026 Lawtitude Legal. All rights reserved.
