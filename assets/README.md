# `assets/` — README

Welcome! 👋
This `README.md` lives inside the `assets/` folder of your website repository.
Its purpose is simple: explain **what each folder is for**, why it exists, and how a beginner can use or maintain it — written clearly and carefully so anyone can follow.

---

## Why this folder matters (plain language)

The `assets/` directory holds all the **static files** your website needs to display correctly: styles (CSS), scripts (JS), images, icons, fonts, and small data files.
Keeping these files organized makes your project easier to understand, faster to build, and simpler to maintain.

---

## Recommended folder structure (what you should see here)

```
assets/
├── css/        # Compiled stylesheets (production .css files)
├── scss/       # Optional: source SCSS/SASS files (if you use a preprocessor)
├── scripts/    # JavaScript files (app logic, modules)
├── img/        # Raster images (png, jpg, webp) and graphics
├── icons/      # SVGs, favicons, icon sprites
├── fonts/      # Web fonts (.woff / .woff2 / .ttf)
├── data/       # Small JSON / CSV / YAML files used by the frontend
├── media/      # Video/audio files (.mp4, .webm, .mp3)
├── vendor/     # Third-party libraries (optional)
└── themes/     # Optional alternate themes (light/dark) or CSS skins
```

> Note: Not all projects need *every* folder. Keep what you use.

---

## What goes in each directory (with simple rationale)

* **`css/`**
  Contains the final, compiled styles your pages load (e.g., `main.css`, `theme.min.css`). Browsers read these files directly.

* **`scss/`** *(optional)*
  Put SASS/SCSS source files here if you write modular styles. These are compiled into `css/` during your build step. Keeping source and compiled files separate avoids confusion.

* **`scripts/`**
  Your JavaScript code — app logic, small modules, or bundles. Example: `app.js`, `utils.js`. Use `vendor/` for third-party libs.

* **`img/`**
  All images used on the site (logos, photos, backgrounds). Prefer optimized formats: WebP for photos, SVG for logos/illustrations where possible.

* **`icons/`**
  SVGs, icon sprites, and favicons. SVG is preferred for crisp, scalable icons.

* **`fonts/`**
  Self-hosted font files (e.g., `.woff2`) so fonts load fast and are consistent.

* **`data/`**
  Small frontend data (e.g., `config.json`, `countries.csv`). Useful for static sites that render data client-side.

* **`media/`**
  Large media like background videos or audio clips. Keep file sizes reasonable — consider streaming or CDN for big assets.

* **`vendor/`**
  Copies of third-party libraries you need to keep with the repo (e.g., `chartjs/`, `bootstrap/`) — helpful when you want exact versions stored.

* **`themes/`** *(optional)*
  Alternate CSS files or resource variants for site themes (light/dark or branded skins).

---

## Keeping empty directories in GitHub

Git ignores empty directories. To ensure folders appear in the repo, a small placeholder file is commonly added:

* Add a `.gitkeep` file inside each empty folder:

  ```
  assets/css/.gitkeep
  assets/scripts/.gitkeep
  ...
  ```

  `.gitkeep` is a convention (not a Git rule) — it simply keeps the directory tracked.

---

## Quick commands (create structure locally)

Run these in a terminal inside your project root (works on macOS, Linux, Git Bash on Windows):

```bash
mkdir -p assets/{css,scss,scripts,img,icons,fonts,data,media,vendor,themes}
# Add .gitkeep to each directory so the folders appear on GitHub
for d in assets/*; do
  [ -d "$d" ] && touch "$d/.gitkeep"
done
```

---

## How to add files from the GitHub web UI (if you don't use git CLI)

1. In the repo, click **Add file → Create new file**.
2. In the filename box type a path like `assets/css/main.css`.
   GitHub will create the `assets/` and `css/` folders and the `main.css` file in one step.
3. Commit the new file.

---

## Naming & optimization tips (practical basics)

* Use **meaningful names**: `header-logo.svg`, `hero-bg.webp`, `main.min.css`.
* Image formats:

  * Photos: use **WebP** or optimized **JPEG**.
  * Logos/illustrations: use **SVG** when possible.
* Serve fonts in `.woff2` for best compression & browser support.
* Minify production CSS/JS (e.g., `main.min.css`, `bundle.min.js`).
* Use cache-busting (e.g., filename with version hash: `main.20250801.css`) when updating files in production.

---

## Performance & build notes (novice-friendly)

* Keep asset sizes small. Large images/videos slow page loads.
* Consider using a build tool (Webpack, Vite, Parcel, or your static site generator) to:

  * compile SCSS → CSS
  * bundle and minify JS
  * optimize images
* In production, consider hosting large assets (videos, big images) on a CDN for speed.

---

## Security & licensing reminders

* Don’t commit private keys or secrets in `assets/` — it’s public in most repos.
* For third-party `vendor/` files, keep licenses and version notes (e.g., `vendor/bootstrap/README.md`) so you know allowed usage.

---

## Example minimal `assets/` README section to include in your project docs

> Use this as a short blurb in your project overview:
>
> `assets/` — static frontend files (CSS, JS, images, fonts). Update files here and reference them with relative paths (`/assets/css/main.css`) in templates.

---
