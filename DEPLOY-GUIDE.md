# 🚀 Deploy Guide — Portfolio Live on GitHub in ~10 Minutes

Everything below already uses your username: **skhnam**.

---

## Part 1 — Portfolio Website (GitHub Pages)

### Step 1: Fix/create the repo

You already created `Safeena-khanam.github.io` — rename it:

1. Open https://github.com/skhnam/Safeena-khanam.github.io
2. **Settings** → *General* → **Repository name** → change to exactly: `skhnam.github.io` → **Rename**

(The repo name must exactly match `<username>.github.io` for GitHub to host it at the root URL.)

### Step 2: Push the site

Open PowerShell **inside the `portfolio-site` folder**:

```powershell
cd "$HOME\Documents\portfolio-skhnam-ready\portfolio-site"

git init
git add .
git commit -m "feat: initial portfolio with CI/CD deploy pipeline"
git branch -M main
git remote add origin https://github.com/skhnam/skhnam.github.io.git
git push -u origin main
```

On push, a browser window pops up → sign in to GitHub → **Authorize**.

### Step 3: Enable Pages via Actions

1. In the repo → **Settings** → **Pages**
2. Under *Build and deployment* → Source: select **GitHub Actions**
3. Go to the **Actions** tab — "Build & Deploy Portfolio" runs: Validate ✅ → Deploy ✅
4. Your site is live at:

   **https://skhnam.github.io**

Every future `git push` to `main` redeploys automatically.

---

## Part 2 — Profile README (your GitHub homepage)

1. https://github.com/new → Repository name: exactly `skhnam` → Public → check **"Add a README file"** → Create
2. GitHub shows a banner about the "special repository" — that's correct!
3. Click the ✏️ pencil on README.md → replace contents with my `profile-readme/README.md` → **Commit changes**
4. Visit **github.com/skhnam** — your profile intro is live 🎉

---

## Part 3 — Finishing Touches

1. **Update LinkedIn & resume** with the live URL: `skhnam.github.io`
2. **Pin your best repos** on your profile
3. **Record a 1-minute Loom/OBS demo**: push a change → show the Actions pipeline → show the live site update. Embed in README.
4. **Next repos to build** (make the placeholder project links real, one at a time):
   - `rag-conversational-ai` — publish your ASEE-NE research code
   - `terraform-aws-pipeline` — IaC deployment showcase
   - `observability-stack` — Grafana + CloudWatch monitoring demo

---

## Troubleshooting

- **Workflow fails on "Setup Pages"** → Settings → Pages → Source must be *GitHub Actions*.
- **404 after deploy** → repo name must be exactly `skhnam.github.io`; `index.html` must be at repo root.
- **Site looks unstyled** → hard-refresh (Ctrl+Shift+R); Pages CDN caches a few minutes.
- **`git` not recognized** → reopen PowerShell after installing Git, or reinstall from git-scm.com.
