# Personal CV

A clean, single-column CV page (plain HTML + CSS, no build step), styled after
[jojoldu.github.io](https://jojoldu.github.io/): left-aligned text header, nested
bullet lists, monochrome text on white with blue links.

## Preview locally

Just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Edit your content

| What | Where |
|------|-------|
| Name, tagline, all sections | `index.html` (look for `TODO` comments) |
| Social / contact links | replace the `USERNAME` placeholders in the header of `index.html` |
| Sections | About Me · Experience · Strengths · Skills · Open Source · Education · External Activities |
| Colors / fonts / spacing | `css/style.css` (CSS variables at the top of the file) |

The page is print-friendly — `Cmd/Ctrl + P` → "Save as PDF" produces a clean
document (nav and social icons are hidden in print).

## Deploy to GitHub Pages

**Option A — personal site at `https://<username>.github.io`** (recommended for a CV):

```bash
git init
git add .
git commit -m "Add CV page"
git branch -M main
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

The site goes live at `https://<username>.github.io` within a minute or two.
(The repo **must** be named exactly `<username>.github.io`.)

**Option B — project site at `https://<username>.github.io/cv`:**

Push to any repo (e.g. `cv`), then in GitHub:
**Settings → Pages → Build and deployment → Source: Deploy from a branch →
`main` / `root` → Save.**

> `.nojekyll` is included so GitHub Pages serves these files as-is without
> running Jekyll.
