# 3D Italian Artisan

Diorama & Articulated Action Figures — models with description, instructions, preview image and PDF with zoom.

🌐 Live site: *(after connecting Netlify, paste your URL here)*
🌐 Languages: English / Italiano / Deutsch / 日本語 — selector top right.

## Project structure

```
index.html          -> the whole site (edit models here)
assets/images/      -> PREVIEW IMAGES ONLY (.jpg / .png / .webp)
assets/pdfs/         -> PDF FILES ONLY (.pdf)
netlify.toml        -> Netlify config (static site, no build)
```

## How to add a new model

**1. Add the files**

- Preview image → `assets/images/` — e.g. `my-castle.jpg`
- PDF → `assets/pdfs/` — e.g. `my-castle.pdf`

Use file names with no spaces: `my-castle.jpg`, not `My Castle FINAL v2!!.jpg`

**2. Edit `index.html`**

Find `const MODELLI_INIZIALI = [` and add a new line at the TOP of the list:

```js
{ nome: "Diorama — My Castle", categoria: "Diorama",
  descrizione: "Short description...",
  istruzioni: "1. Download the PDF.\n2. Print...\n3. Assemble...",
  immagine: "assets/images/my-castle.jpg",
  pdf: "assets/pdfs/my-castle.pdf" },
```

Category must be exactly `"Diorama"` or `"Articulated Action Figures"`.

**3. Commit & push to GitHub**

Netlify will redeploy automatically in ~30 seconds. Same URL, no manual upload.

## Author Area

Top right on the site. Default code: `1234`
Change it in `index.html`: `const CODICE_AUTORE = "1234"`

> ⚠️ The Author Area is only for quick preview/testing. Files uploaded there are saved only in that browser. For the public site, always use the steps above.

## First setup: GitHub + Netlify (do it once)

### A) Put this project on GitHub

**Option 1 — from the GitHub website (no terminal):**
1. Go to https://github.com/new
2. Repository name: `3d-italian-artisan` — Public — **do NOT** check “Add a README”
3. Create repository
4. Click **“uploading an existing file”**
5. Drag ALL files from this folder (`index.html`, `netlify.toml`, `.gitignore`, `README.md`, `assets/`…)
6. Commit changes

**Option 2 — from terminal (if you have git):**
```bash
cd 3d-italian-artisan-github
git init
git add .
git commit -m "First version - 3D Italian Artisan"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/3d-italian-artisan.git
git push -u origin main
```

### B) Connect Netlify to GitHub (do it once)

1. Go to https://app.netlify.com → **Add new site → Import an existing project**
2. Choose **GitHub** → authorize → select repo `3d-italian-artisan`
3. Settings:
   - **Branch:** `main`
   - **Build command:** *(leave empty)*
   - **Publish directory:** `.` (a single dot)
4. Click **Deploy site**
5. Netlify gives you a URL like `https://3d-italian-artisan.netlify.app`
   You can rename it in **Site settings → Site details → Change site name**.

### C) Every future update

1. Edit / add files locally (or upload them directly on GitHub: repo → Add file → Upload files)
2. Commit / push
3. Done — Netlify redeploys automatically. Check it in Netlify → **Deploys**.

## License
© 2026 3D Italian Artisan — Max
