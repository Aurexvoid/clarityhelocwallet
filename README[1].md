# Clarity Heloc — Cloudflare Pages Deployment

## ⚠️ CRITICAL: Repo Structure

Your GitHub repo MUST look like this:

```
clarity-heloc/           ← repo root
  ├── index.html         ← MUST be at root, not in a folder
  ├── _redirects         ← MUST be at root
  └── README.md          ← this file
```

**WRONG structure (causes 404):**
```
clarity-heloc/
  └── some-folder/       ← ❌ WRONG — do not put files inside a folder
        ├── index.html
        └── _redirects
```

## 🚀 Deploy Steps

### 1. Push to GitHub
- Upload `index.html` and `_redirects` directly to the repo root
- Do NOT upload a folder containing them

### 2. Connect to Cloudflare Pages
- Go to dash.cloudflare.com → Pages → Create project → Connect to Git
- Select this repo

### 3. Build Settings (EXACT)
| Setting | Value |
|---------|-------|
| Framework preset | `None` |
| Build command | *(leave empty)* |
| Build output directory | `/` |

### 4. Deploy
Click Save and Deploy. Your site goes live.
