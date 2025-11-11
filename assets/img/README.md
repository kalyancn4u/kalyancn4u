# 🖼️ `assets/img/` — Image Assets & Graphics

Welcome! 👋
This folder contains all the **images and graphics** used in your website or web app —
everything from logos and hero banners to background textures and product photos.

> 💡 Think of this as your website’s **gallery or scrapbook** —
> where all still visuals live neatly organized for fast access and clean presentation.

---

## 🧱 Purpose of This Folder

The `img/` directory stores all **non-animated**, **static**, or **background images**.
Keeping them separate from `icons/` or `media/` helps you:

* 🧩 manage image assets easily
* 🖥️ optimize for performance (resize, compress, lazy-load)
* 🗂️ keep your code organized and predictable
* 🌐 reuse images consistently across pages

---

## 📂 Recommended Folder Structure

```
assets/
└── img/
    ├── logos/
    │   ├── site-logo.png
    │   └── favicon.png
    │
    ├── backgrounds/
    │   ├── hero-bg.webp
    │   └── texture.png
    │
    ├── banners/
    │   ├── homepage-banner.jpg
    │   └── sale-banner.jpg
    │
    ├── products/
    │   ├── product-1.webp
    │   └── product-2.webp
    │
    ├── team/
    │   ├── member1.jpg
    │   └── member2.jpg
    │
    ├── illustrations/
    │   ├── data-visual.svg
    │   └── workflow.svg
    │
    ├── thumbnails/
    │   └── preview.jpg
    │
    ├── .gitkeep
    └── README.md   ← this file
```

> 🧩 You can rename or remove subfolders as needed — the key idea is **categorizing by purpose**.

---

## 🧩 Common Image Categories

| Folder           | Purpose                     | Typical Formats |
| ---------------- | --------------------------- | --------------- |
| `logos/`         | Brand and site identity     | `.png`, `.svg`  |
| `backgrounds/`   | Hero or section backgrounds | `.jpg`, `.webp` |
| `banners/`       | Promotional or page headers | `.jpg`, `.webp` |
| `products/`      | Catalog / portfolio images  | `.jpg`, `.webp` |
| `team/`          | Profile or staff photos     | `.jpg`, `.png`  |
| `illustrations/` | Custom visuals, diagrams    | `.svg`, `.png`  |
| `thumbnails/`    | Small preview images        | `.jpg`, `.webp` |

---

## 🧠 Recommended Image Formats

| Format      | Use Case                           | Notes                                          |
| ----------- | ---------------------------------- | ---------------------------------------------- |
| **`.webp`** | Default for web                    | Modern, small file size, supports transparency |
| **`.jpg`**  | Photos / backgrounds               | Great compression; use 80–90% quality          |
| **`.png`**  | Icons / graphics with transparency | Larger but lossless                            |
| **`.svg`**  | Logos, vector illustrations        | Infinite resolution, small size                |
| **`.gif`**  | Simple non-video animations        | Use only if necessary (prefer `.webp`)         |

---

## 🧩 Example Usage in HTML

### ✅ Static Image

```html
<img src="assets/img/logos/site-logo.png" alt="Website Logo" width="120" height="120">
```

### 🖼️ Background Image (CSS)

```css
.hero-section {
  background: url('../img/backgrounds/hero-bg.webp') no-repeat center center / cover;
}
```

### 📱 Responsive Image

```html
<picture>
  <source srcset="assets/img/banners/homepage-banner.webp" type="image/webp">
  <img src="assets/img/banners/homepage-banner.jpg" alt="Homepage Banner">
</picture>
```

---

## ⚙️ Optimization Tips (for Beginners)

| Tip                                          | Why It Helps                      |
| -------------------------------------------- | --------------------------------- |
| Use `.webp` whenever possible                | Smaller, faster loading           |
| Resize images to actual display size         | Avoid wasting bandwidth           |
| Compress using tools like TinyPNG or Squoosh | Improves page speed               |
| Use `alt` attributes                         | Accessibility & SEO               |
| Lazy-load below-fold images                  | Faster first paint                |
| Keep filenames lowercase, hyphenated         | Better consistency and URL safety |

---

## 🧾 Example Placeholder Setup

If you’re just initializing this directory:

```bash
mkdir -p assets/img/{logos,backgrounds,banners,products,team,illustrations,thumbnails}
touch assets/img/.gitkeep
```

Then add small placeholder images or empty `.gitkeep` files in each folder:

```
assets/img/logos/.gitkeep
assets/img/backgrounds/.gitkeep
...
```

This ensures GitHub tracks your folder structure even before real images exist.

---

## ⚖️ Good Practices

| ✅ Do                                              | ❌ Don’t                                      |
| ------------------------------------------------- | -------------------------------------------- |
| Store web-optimized versions only                 | Commit raw camera photos                     |
| Use descriptive names (`hero-bg.webp`)            | Use vague names (`image1.png`)               |
| Group by purpose                                  | Keep all images flat in one folder           |
| Add a short `README` if the folder is specialized | Leave others guessing                        |
| Keep backups of originals outside `/assets`       | Mix editable PSD/AI files in production repo |

---

## 🔐 Licensing & Attribution

If you’re using images from stock sources (Unsplash, Pexels, Freepik, etc.):

* Always **verify the license terms** (many are free but may need attribution).
* Credit the author in your main `LICENSES.txt` or `credits.md`.
* Avoid copyrighted material unless explicitly allowed.

Example:

```
Image: Team Photo by John Doe via Unsplash (Free to use)
```

---

## 🧭 Relationship with Other Folders

| Folder          | Role                                       |
| --------------- | ------------------------------------------ |
| `assets/img/`   | Static images (logos, backgrounds, etc.)   |
| `assets/media/` | Playable media (videos, audio, animations) |
| `assets/icons/` | Small vector or favicon graphics           |

> 🧩 Keep `img/` for still visuals, `media/` for motion, and `icons/` for symbolic images.

---

## ✅ Summary

| Concept                 | Description                                                                                 |
| ----------------------- | ------------------------------------------------------------------------------------------- |
| **Folder Purpose**      | Stores all static image assets                                                              |
| **Default Subfolders**  | `logos/`, `backgrounds/`, `banners/`, `products/`, `team/`, `illustrations/`, `thumbnails/` |
| **Default Placeholder** | `.gitkeep`                                                                                  |
| **Recommended Formats** | `.webp`, `.jpg`, `.png`, `.svg`                                                             |
| **Usage**               | `<img>` tag or CSS backgrounds                                                              |
| **Optimized For**       | Speed, clarity, and consistency                                                             |

---

### ✨ Bottom Line

> The `assets/img/` folder is your website’s **visual identity library** 🖼️ —
> every photo, logo, and background that gives your site its unique look lives here.
> Keep it optimized, organized, and clearly named — your design (and page speed) will thank you. 🚀

---
