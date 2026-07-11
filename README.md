# 🌐 Safeena Khanam — Portfolio (CI/CD Deployed)

> Personal portfolio site, deployed to **GitHub Pages** through a **GitHub Actions** pipeline — zero hosting costs, fully automated.

![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222222?logo=github&logoColor=white)

**🔗 Live site:** https://skhnam.github.io

---

## 🎯 Problem Statement

Resumes get scanned, not studied. I wanted a portfolio that:

- Proves my DevOps skills *by how it's built*, not just what it says
- Costs $0 to host and maintain
- Ships automatically on every `git push` — no manual deploy steps, ever

So the portfolio itself is a small CI/CD project: push to `main` → pipeline validates the HTML → deploys to GitHub Pages.

## 🛠️ Tech Stack

- **Site:** Single-file HTML/CSS/vanilla JS (no framework, no build step — fast and dependency-free)
- **CI/CD:** GitHub Actions (`.github/workflows/deploy.yml`)
- **Hosting:** GitHub Pages (free, HTTPS included)

## ✨ Features

- 🚀 **Automated deployment** — push to `main` triggers validate → deploy
- ✅ **CI validation step** — HTML linting + section integrity checks before deploy
- 🖥️ **Terminal-themed dark UI** with typing animation and scroll reveals
- 📱 **Fully responsive** — works on mobile, tablet, desktop
- 🔒 **HTTPS by default** via GitHub Pages

## ⚙️ CI/CD Flow

```
git push origin main
   │
   ▼
GitHub Actions triggered
   │
   ├─ Job 1: validate  → lint HTML (tidy) + check all sections exist
   │
   └─ Job 2: deploy    → upload artifact → deploy to GitHub Pages
                         └─ live at skhnam.github.io ✅
```

## 🚀 How to Run Locally

```bash
git clone https://github.com/skhnam/skhnam.github.io.git
cd skhnam.github.io

# no build step needed — just open it
start index.html       # Windows
open index.html        # macOS

# or serve it properly
python3 -m http.server 8000   # → http://localhost:8000
```

## 📁 Folder Structure

```
.
├── index.html                  # the entire site (HTML + CSS + JS)
├── .github/
│   └── workflows/
│       └── deploy.yml          # CI/CD pipeline: validate → deploy
└── README.md
```

## 📚 Learnings / Challenges

- **GitHub Pages deployment models:** chose the Actions-based deploy (`actions/deploy-pages`) over the classic branch-based deploy so I could add a validation gate before anything goes live — the same pattern as production pipelines.
- **Keeping it single-file:** resisting a framework kept the site at ~0 dependencies, instant load, and nothing to break in CI.
- **Concurrency control:** added a `concurrency` group so rapid pushes cancel stale deploys instead of racing each other.

## 👩‍💻 About Me

Software Engineer (4 yrs) — cloud-native architecture, DevOps automation, and applied AI (RAG pipelines).
AWS · Terraform · Kubernetes · GitHub Actions · Python.

## 📫 Contact

- **LinkedIn:** [safeena-khanam](https://www.linkedin.com/in/safeena-khanam)
- **Email:** khanamsafeena5@gmail.com
- **Portfolio:** https://skhnam.github.io
