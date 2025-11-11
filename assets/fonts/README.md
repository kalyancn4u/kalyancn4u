# 🔡 `assets/fonts/` — Web Font Files & Typography Assets

Welcome! 👋
This folder stores all **custom or self-hosted font files** used by your website.
Fonts are an important part of your brand identity — they define how your text looks and feels across browsers, devices, and languages.

> 💡 Think of this as your **typography vault** —
> where all the styles, weights, and formats of your site’s fonts live safely and consistently.

---

## 🧱 Purpose of This Folder

The `fonts/` directory helps you:

* ✅ Serve fonts locally (for speed, privacy, and offline access)
* ✅ Keep consistent typography across browsers and devices
* ✅ Reduce dependency on third-party CDNs
* ✅ Manage multiple font families and weights easily

---

## 📂 Recommended Folder Structure

```
assets/
└── fonts/
    ├── roboto/
    │   ├── roboto-regular.woff2
    │   ├── roboto-bold.woff2
    │   └── roboto-italic.woff2
    │
    ├── open-sans/
    │   ├── open-sans-regular.woff2
    │   └── open-sans-bold.woff2
    │
    ├── lato/
    │   ├── lato-regular.woff
    │   └── lato-bold.woff
    │
    ├── LICENSES.txt
    ├── .gitkeep
    └── README.md   ← this file
```

> 🧩 Each font family should have its **own subfolder**,
> containing all available weights and styles (regular, bold, italic, etc.).

---

## 🧠 Common Font Formats

| Format              | Description                     | Recommended Use               |
| ------------------- | ------------------------------- | ----------------------------- |
| **`.woff2`**        | Modern, compressed format       | ✅ Best for web (small & fast) |
| **`.woff`**         | Older compressed format         | For older browser support     |
| **`.ttf` / `.otf`** | TrueType / OpenType             | For design tools or fallbacks |
| **`.eot`**          | Legacy format for IE8 and below | Rarely needed today           |
| **`.svg`**          | Scalable vector fonts           | Deprecated, avoid if possible |

---

## 🎨 How to Use Web Fonts in CSS

### Option 1: Link from Local `assets/fonts/`

```css
@font-face {
  font-family: 'Roboto';
  src: url('../fonts/roboto/roboto-regular.woff2') format('woff2'),
       url('../fonts/roboto/roboto-regular.woff') format('woff');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
```

Then apply it globally:

```css
body {
  font-family: 'Roboto', Arial, sans-serif;
}
```

---

### Option 2: Organize Multiple Weights and Styles

```css
@font-face {
  font-family: 'Open Sans';
  src: url('../fonts/open-sans/open-sans-bold.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
}
@font-face {
  font-family: 'Open Sans';
  src: url('../fonts/open-sans/open-sans-italic.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
}
```

---

### Option 3: Use Variables (SCSS Example)

```scss
$primary-font: 'Roboto', sans-serif;

body {
  font-family: $primary-font;
  line-height: 1.6;
}
```

---

## ⚙️ Loading Best Practices

| Tip                                        | Why It Matters                           |
| ------------------------------------------ | ---------------------------------------- |
| Use `.woff2` first                         | Smaller, faster format                   |
| Use `font-display: swap;`                  | Avoid invisible text while loading       |
| Limit to 2–3 font families                 | Too many fonts slow down pages           |
| Subset your fonts (use only needed glyphs) | Reduce file size                         |
| Preload important fonts                    | Improves performance for above-fold text |

Example preload tag in HTML:

```html
<link rel="preload" href="assets/fonts/roboto/roboto-regular.woff2" as="font" type="font/woff2" crossorigin="anonymous">
```

---

## ⚖️ Good Practices for Organizing Fonts

| ✅ Do                                                    | ❌ Don’t                                 |
| ------------------------------------------------------- | --------------------------------------- |
| Use one folder per font family                          | Mix all fonts into one folder           |
| Include weights (regular, bold, italic)                 | Keep only one style                     |
| Document font sources in `LICENSES.txt`                 | Forget where you downloaded them        |
| Use modern `.woff2`                                     | Upload raw `.ttf` files unoptimized     |
| Name files consistently (`fontname-weight-style.woff2`) | Use random names (`font1.woff`)         |
| Test in multiple browsers                               | Assume fonts render the same everywhere |

---

## 📘 Example `LICENSES.txt`

```
Roboto © Google Fonts — Apache License, Version 2.0
Open Sans © Google Fonts — Apache License, Version 2.0
Lato © Łukasz Dziedzic — SIL Open Font License 1.1
```

🧠 Always keep track of font licenses and sources — this is **very important** for open-source compliance and professional documentation.

---

## 🧾 Example Placeholder Setup (for Initialization)

If you’re setting this up freshly:

```bash
mkdir -p assets/fonts/{roboto,open-sans,lato}
touch assets/fonts/.gitkeep
echo "Roboto (placeholder font folder)" > assets/fonts/roboto/README.txt
```

Then, download web-optimized fonts (e.g., from [Google Fonts](https://fonts.google.com/))
and place them in the respective subfolders.

---

## 🧭 Relationship with Other Folders

| Folder          | Role                                                      |
| --------------- | --------------------------------------------------------- |
| `assets/fonts/` | Stores web fonts and type assets                          |
| `assets/css/`   | Defines how fonts are used in stylesheets                 |
| `assets/icons/` | Stores symbolic or pictogram-style icons (not text fonts) |

> 💡 **Fonts ≠ Icons:** Icon fonts (like Font Awesome) belong in `assets/vendor/` or `assets/icons/`, not here.

---

## ✅ Summary

| Concept            | Description                                          |
| ------------------ | ---------------------------------------------------- |
| **Folder Purpose** | Store and serve self-hosted web fonts                |
| **File Types**     | `.woff2`, `.woff`, `.ttf`, `.otf`                    |
| **Structure**      | One folder per font family                           |
| **Usage**          | Imported via `@font-face` in CSS                     |
| **Best Practice**  | Use modern `.woff2` format with `font-display: swap` |
| **Default Files**  | `.gitkeep`, `LICENSES.txt`, `README.md`              |

---

### ✨ Bottom Line

> The `assets/fonts/` folder is your site’s **voice** 🔡 —
> it gives your text style, tone, and readability.
> Keep your fonts organized, licensed, and optimized —
> and your website will look sharp, load fast, and stay future-proof. 🚀

---
