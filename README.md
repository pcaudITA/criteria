# PCaudit — End-of-Life Classification Guide

A single-page, self-contained reference guide describing how PCaudit audits, classifies (grades A–D) and quantifies the condition of recovered devices, and how each grade affects Fair Market Value (FMV).

**Features**

- **Trilingual** — Italian 🇮🇹 · English 🇬🇧 · Spanish 🇪🇸, switchable in-page (top-right `IT / EN / ES`). The choice is remembered between visits.
- **Light / dark mode** — moon/sun toggle. Defaults to your system preference and is remembered between visits.
- **No build step, no dependencies** — one `index.html`. Fonts load from Google Fonts; the logo is embedded. Works offline except for the web fonts.

## View it locally

Just open `index.html` in any browser — double-click it, or:

```bash
# optional: serve over http (nicer for some browsers)
python3 -m http.server 8000
# then open http://localhost:8000
```

## Publish to GitHub + GitHub Pages

From inside this folder:

```bash
git init
git add .
git commit -m "PCaudit EoL classification guide — trilingual, light/dark"
git branch -M main
# create an empty repo on github.com first (no README), then:
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

Then enable Pages:

1. On GitHub, open the repo → **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. After ~1 minute your guide is live at:
   `https://<your-username>.github.io/<your-repo>/`

> The included `.nojekyll` file tells GitHub Pages to serve the files as-is (no Jekyll processing), which avoids any surprises with the static HTML.

## Editing content

All text lives in `index.html`. Each translatable element carries a `data-i18n="tNN"` attribute; the three translations are held in the `const T = { it: {...}, en: {...}, es: {...} }` dictionary near the bottom of the file. To change wording, edit the matching key in all three languages so they stay in sync.

## Structure

```
.
├── index.html      # the entire guide (HTML + CSS + JS + embedded logo)
├── .nojekyll       # serve static files as-is on GitHub Pages
├── .gitignore
└── README.md
```

---
Reference document · Rev. 3 · 2026
