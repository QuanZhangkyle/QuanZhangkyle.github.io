# Quan Zhang — personal website

A [Quarto](https://quarto.org) website. Layout: sidebar profile (about · *trestles*).
Palette: **Teal Scholar** (`#FFFFFF` / `#1A1A1A` / `#0F766E` / `#64748B`).

## Edit & preview locally

```bash
quarto preview      # live-reload preview in your browser
quarto render       # build the static site into _site/
```

Open the folder in **Positron** and use the live preview, or run the commands
above in a terminal.

## Structure

| File | Purpose |
|------|---------|
| `_quarto.yml` | Site config — navbar, links, theme, metadata |
| `index.qmd` | Home page (profile card + bio) |
| `research.qmd` | Research themes, working papers, grants |
| `publications.qmd` | Publication list |
| `teaching.qmd` | Courses & mentoring |
| `cv.qmd` | Embedded + downloadable CV |
| `theme.scss` | Teal Scholar colors & typography |
| `assets/` | Profile photo, favicon, `cv.pdf` |

## Things to fill in (search the repo for `TODO`)

- [ ] Exact title & department in `index.qmd`
- [ ] Real bio (1–3 sentences)
- [ ] Education entries
- [ ] Google Scholar / GitHub / LinkedIn URLs (`_quarto.yml` + `index.qmd`)
- [ ] Real publications (`publications.qmd`)
- [ ] Research themes & working papers (`research.qmd`)
- [ ] Replace `assets/profile.svg` with a real photo (`assets/profile.jpg`, then update `image:` in `index.qmd`)
- [ ] Add `assets/cv.pdf`

## Deploy (GitHub Pages)

A GitHub Actions workflow (`.github/workflows/publish.yml`) renders and deploys
on every push to `main`. After pushing the repo:

1. GitHub → repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
2. Push to `main`; the site builds and goes live at `https://<user>.github.io/<repo>/`.
3. For a custom domain (e.g. `quanzhang.org`): add it under **Settings → Pages →
   Custom domain**, then set DNS at your registrar (A/ALIAS records to GitHub
   Pages + a `CNAME` for `www`). Also set `site-url` in `_quarto.yml`.
