# Ravi Ranjan — Personal Academic Website

Built with [Quarto](https://quarto.org/) and hosted on [GitHub Pages](https://pages.github.com/).

## Quick start

### Prerequisites
- [Quarto](https://quarto.org/docs/get-started/) installed
- [Git](https://git-scm.com/) installed
- A [GitHub](https://github.com/) account
- RStudio (recommended) or any text editor

### One-time setup: install the Font Awesome extension

The Bluesky icon in the navbar needs the Font Awesome extension (Quarto's
built-in icon set is too old to include it). From the project folder, run
this once in the Terminal:

```bash
quarto add quarto-ext/fontawesome
```

This creates an `_extensions/` folder. Commit that folder to Git along with
everything else.

### Local preview

```bash
quarto preview
```

This opens a live-reloading preview in your browser.

### Before you publish — things to update

1. **`_quarto.yml`** — Replace placeholder URLs and email:
   - `site-url` → your actual GitHub Pages URL
   - `mailto:` → your email address
   - GitHub link → your GitHub profile URL

2. **`_quarto.yml`** — Update your Bluesky handle in the navbar (the
   `bsky.app/profile/...` link).

3. **`img/profile.jpg`** — Add your profile photo (recommended ~400×400px).

4. **`files/ravi_ranjan_cv.pdf`** — Place your CV PDF here.

5. **`files/ranjan-klausmeier-2022.pdf`** — Place your paper PDF here
   (or remove the PDF link from `publications.qmd`).

6. Review all `.qmd` files and update any content that has changed since migration.

### Deploy to GitHub Pages

```bash
# Option 1: One-command publish
quarto publish gh-pages

# Option 2: Manual — render, then push
quarto render
git add -A
git commit -m "Update site"
git push
```

For Option 2, set GitHub Pages to deploy from the `docs/` folder in your
repo settings (Settings → Pages → Source → Deploy from branch → /docs).

## File structure

```
.
├── _quarto.yml          # Site configuration
├── custom.scss          # Theme: fonts, colors, layout
├── _extensions/         # Font Awesome (created by `quarto add`)
├── index.qmd            # Home / About page
├── research.qmd         # Research overview & projects
├── publications.qmd     # Publication list
├── teaching.qmd         # Teaching history
├── cv.qmd               # CV download page
├── img/                 # Profile photo
│   └── profile.jpg
├── files/               # Downloadable files (CV PDF, paper PDFs)
│   └── ravi_ranjan_cv.pdf
└── README.md            # This file
```
