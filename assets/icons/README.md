# 🧩 `assets/icons/` — Icons, Favicons & Symbol Assets

Welcome! 👋
This folder contains all the **icon graphics** used across your website — from favicons in the browser tab 🧭 to UI icons like 🔍 search, 🛒 cart, or 📧 email.

> 💡 Think of this as your **symbol library** —
> small, lightweight visuals that make your design more intuitive and interactive.

---

## 🧱 Purpose of This Folder

The `icons/` directory is meant for:

* ✅ **UI and system icons** (SVGs, PNGs, ICOs)
* ✅ **Favicons** and app icons
* ✅ **Sprite sheets** or **symbol packs**
* ✅ **Vector-based illustrations** used repeatedly

Keeping them separate from `img/` and `media/` ensures:

* clarity between decorative images vs. functional icons,
* faster file access and smaller sizes, and
* consistent icon usage across the entire project.

---

## 📂 Recommended Folder Structure

```
assets/
└── icons/
    ├── favicon.ico
    ├── site-icon-192.png
    ├── apple-touch-icon.png
    ├── social/
    │   ├── facebook.svg
    │   ├── twitter.svg
    │   └── linkedin.svg
    │
    ├── ui/
    │   ├── search.svg
    │   ├── close.svg
    │   ├── menu.svg
    │   ├── user.svg
    │   └── cart.svg
    │
    ├── sets/
    │   └── icons.svg   # Combined SVG sprite file
    │
    ├── manifest.json   # (Optional) for PWA or favicon configuration
    ├── .gitkeep
    └── README.md       ← this file
```

> 🧩 Organizing icons by **purpose** (`ui/`, `social/`, `sets/`) helps maintain clarity when your project scales.

---

## 🧩 Common Icon Types

| Type                    | Examples                                      | Description                           |
| ----------------------- | --------------------------------------------- | ------------------------------------- |
| **Favicon**             | `favicon.ico`                                 | The small browser tab icon            |
| **App Icons**           | `apple-touch-icon.png`, `site-icon-192.png`   | Used for mobile shortcuts or PWA      |
| **UI Icons**            | `search.svg`, `close.svg`, `user.svg`         | Interface actions or status symbols   |
| **Social Icons**        | `facebook.svg`, `twitter.svg`, `linkedin.svg` | Links to social media                 |
| **Icon Sets / Sprites** | `icons.svg`                                   | Combined SVG file with multiple icons |

---

## 🧠 Recommended Formats

| Format                 | Purpose                    | Advantages                                              |
| ---------------------- | -------------------------- | ------------------------------------------------------- |
| **`.svg`**             | Preferred for UI icons     | Scales infinitely, tiny file size, customizable via CSS |
| **`.png`**             | Fallback or older browsers | Raster, but widely supported                            |
| **`.ico`**             | Browser favicon            | Required by older browsers                              |
| **`.json` (manifest)** | PWA metadata               | Defines icon usage on devices                           |

---

## 🧩 Example: Adding a Favicon

In your HTML `<head>` section:

```html
<link rel="icon" type="image/x-icon" href="assets/icons/favicon.ico">
<link rel="apple-touch-icon" href="assets/icons/apple-touch-icon.png">
<link rel="manifest" href="assets/icons/manifest.json">
```

---

## 🧭 Example: Using SVG Icons

### 1️⃣ Inline SVG

```html
<svg width="24" height="24">
  <use href="assets/icons/sets/icons.svg#search"></use>
</svg>
```

### 2️⃣ Direct Image Tag

```html
<img src="assets/icons/ui/user.svg" alt="User Icon" width="24" height="24">
```

### 3️⃣ As Background in CSS

```css
button.search {
  background: url('../icons/ui/search.svg') no-repeat center;
  width: 32px;
  height: 32px;
}
```

---

## ⚙️ Optimization Tips

| Tip                                                                    | Why It Helps                              |
| ---------------------------------------------------------------------- | ----------------------------------------- |
| 🧩 Use **SVG** whenever possible                                       | Small, scalable, and accessible           |
| 🧾 Minify SVGs using [SVGOMG](https://jakearchibald.github.io/svgomg/) | Reduces size dramatically                 |
| ⚙️ Use consistent sizes (e.g., 24px grid)                              | Keeps icons aligned and crisp             |
| 🎨 Match stroke width and corner radius                                | Ensures visual consistency                |
| 🔍 Use descriptive filenames                                           | e.g., `close.svg`, not `icon5.svg`        |
| 🧭 Keep a simple `icons.svg` sprite                                    | Combines many icons into one HTTP request |

---

## 📦 Example SVG Sprite Setup

`assets/icons/sets/icons.svg`

```xml
<svg xmlns="http://www.w3.org/2000/svg" style="display: none;">
  <symbol id="search" viewBox="0 0 24 24">
    <path d="M10 18a8 8 0 1 1 4.9-14.32l4.83 4.83a1 1 0 0 1-1.42 1.42l-4.83-4.83A8 8 0 0 1 10 18z"/>
  </symbol>
  <symbol id="close" viewBox="0 0 24 24">
    <path d="M18 6L6 18M6 6l12 12"/>
  </symbol>
</svg>
```

Then in HTML:

```html
<svg class="icon"><use href="assets/icons/sets/icons.svg#close"></use></svg>
```

---

## ⚖️ Best Practices

| ✅ Do                                   | ❌ Don’t                                      |
| -------------------------------------- | -------------------------------------------- |
| Keep all icons in vector (SVG) format  | Use large raster icons for small UI elements |
| Use clear, semantic filenames          | Use vague names like `icon1.svg`             |
| Optimize icons before committing       | Push raw Illustrator exports                 |
| Separate UI, social, and favicon icons | Dump everything into one folder              |
| Track empty dirs with `.gitkeep`       | Lose folder structure on GitHub              |
| Document new icons in this README      | Leave teammates guessing                     |

---

## 🧾 Example Placeholder Setup

If starting from scratch:

```bash
mkdir -p assets/icons/{ui,social,sets}
touch assets/icons/{favicon.ico,manifest.json,.gitkeep}
```

Then inside each folder, you can add placeholder files:

```
assets/icons/ui/.gitkeep
assets/icons/social/.gitkeep
assets/icons/sets/.gitkeep
```

---

## 🔐 Licensing & Attribution

If you’re using third-party icon sets:

* Always review their **license terms** (MIT, CC, Free for commercial use, etc.).
* Keep their `LICENSE.txt` or note in this README.
* Example free sources:

  * [Font Awesome](https://fontawesome.com/icons)
  * [Feather Icons](https://feathericons.com/)
  * [Heroicons](https://heroicons.com/)
  * [Iconify](https://icon-sets.iconify.design/)

Example:

```
Feather Icons © Cole Bemis — MIT License
```

---

## 🧭 Relationship with Other Folders

| Folder          | Role                           |
| --------------- | ------------------------------ |
| `assets/icons/` | Symbols, favicons, UI icons    |
| `assets/img/`   | Static imagery and backgrounds |
| `assets/media/` | Videos, audio, motion graphics |

> 🧠 Icons are functional elements, not decorative — use `img/` for visuals and `media/` for motion.

---

## ✅ Summary

| Concept                | Description                       |
| ---------------------- | --------------------------------- |
| **Folder Purpose**     | Stores icons and favicons         |
| **File Types**         | `.svg`, `.png`, `.ico`, `.json`   |
| **Subfolders**         | `ui/`, `social/`, `sets/`         |
| **Default File**       | `favicon.ico`, `.gitkeep`         |
| **Recommended Format** | `.svg`                            |
| **Used In**            | `<img>`, `<svg>`, CSS backgrounds |

---

### ✨ Bottom Line

> The `assets/icons/` folder is your site’s **symbol dictionary** 🧩 —
> it keeps every small yet powerful visual cue in one well-organized place.
> Maintain consistency, use clean SVGs, and your UI will feel cohesive and polished. ⚡

---
