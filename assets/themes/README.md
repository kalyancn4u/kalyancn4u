# 🎨 `assets/themes/` — Website Theme Files

Welcome! 👋
This folder contains **theme-related files** — different visual styles, color palettes, and layout variations that define how your website looks and feels.

> 🧠 Think of a **theme** as your site’s “outfit.”
> It changes the **appearance** (colors, fonts, spacing, backgrounds) but not the **content** or **structure**.

---

## 🧱 Purpose

The `themes/` directory helps you:

* ✅ keep visual styles organized (light, dark, corporate, festive, etc.)
* ✅ switch between themes easily
* ✅ maintain a consistent design system
* ✅ avoid cluttering your main `css/` folder with multiple alternate stylesheets

Each theme here is an independent **CSS (or SCSS)** file that overrides your base `main.css`.

---

## 📂 Recommended Structure

```
assets/
└── themes/
    ├── light.css
    ├── dark.css
    ├── ocean.css
    ├── forest.css
    └── README.md   ← this file
```

You may also have:

```
assets/themes/scss/
```

if you maintain preprocessed theme files separately (e.g., `light.scss`, `dark.scss`).

---

## 🎨 Example Default Themes

| Theme File       | Description                                            | Example Look              |
| ---------------- | ------------------------------------------------------ | ------------------------- |
| **`light.css`**  | Default bright layout; white backgrounds and dark text | Clean, professional       |
| **`dark.css`**   | Dark background with light text for night mode         | Eye-friendly in low light |
| **`ocean.css`**  | Blue-tinted cool color palette                         | Calm, modern              |
| **`forest.css`** | Green and earthy palette                               | Nature-inspired theme     |

---

## 🧩 How to Apply a Theme in HTML

You can load a specific theme manually in your HTML:

```html
<!-- Base stylesheet -->
<link rel="stylesheet" href="assets/css/main.css">

<!-- Add the theme of your choice -->
<link rel="stylesheet" href="assets/themes/dark.css">
```

🪄 Tip: The **last stylesheet loaded** takes precedence —
so it overrides any matching styles from `main.css`.

---

## ⚙️ Switching Themes Dynamically (Beginner Example)

Here’s a simple JavaScript example to let users toggle between themes:

```html
<link id="theme-link" rel="stylesheet" href="assets/themes/light.css">

<button onclick="toggleTheme()">Switch Theme</button>

<script>
function toggleTheme() {
  const link = document.getElementById('theme-link');
  link.href = link.href.includes('light.css')
    ? 'assets/themes/dark.css'
    : 'assets/themes/light.css';
}
</script>
```

🧠 This simple toggle switches between `light.css` and `dark.css` dynamically!

---

## 🎨 Suggested Naming Conventions

| Type                   | Example                       | Description                     |
| ---------------------- | ----------------------------- | ------------------------------- |
| **Default Theme**      | `light.css`                   | Main or fallback theme          |
| **Dark Mode**          | `dark.css`                    | Accessible dark palette         |
| **Seasonal / Event**   | `summer.css`, `christmas.css` | Temporary themed design         |
| **Corporate / Brand**  | `brandname.css`               | Used for white-label sites      |
| **Minimal / Contrast** | `contrast.css`, `minimal.css` | Accessibility or style variants |

---

## 🧾 Example File Content

`light.css`

```css
/* Light Theme - Default */
body {
  background-color: #ffffff;
  color: #000000;
}
```

`dark.css`

```css
/* Dark Theme */
body {
  background-color: #121212;
  color: #f1f1f1;
}
```

---

## 💡 Tips for Beginners

| Tip                                                   | Why It Helps                  |
| ----------------------------------------------------- | ----------------------------- |
| Start with one theme (e.g., `light.css`)              | Easier to maintain            |
| Use consistent variable names (CSS vars or SCSS vars) | Makes switching themes easier |
| Use CSS variables (`:root { --primary-color: ... }`)  | Simplifies theme swapping     |
| Test in multiple browsers                             | Ensures consistent look       |
| Keep file names lowercase                             | Better for web compatibility  |

---

## 🌈 Example Advanced Setup (CSS Variables)

If your themes share common structure but differ in colors,
use **CSS custom properties**:

`main.css`

```css
:root {
  --bg-color: #fff;
  --text-color: #000;
}

body {
  background: var(--bg-color);
  color: var(--text-color);
}
```

`dark.css`

```css
:root {
  --bg-color: #121212;
  --text-color: #e0e0e0;
}
```

This way, you only change **variables**, not the whole layout — much cleaner!

---

## 📦 When to Add a New Theme

Add a new theme file when:

* You need a **new visual identity** (e.g., for branding)
* You’re adding **user theme preferences**
* You’re building a **multi-tenant (white-label)** site
* You want **temporary seasonal styling** (holiday sales, events, etc.)

---

## ⚖️ Best Practices

| Do ✅                               | Don’t ❌                          |
| ---------------------------------- | -------------------------------- |
| Keep each theme self-contained     | Mix unrelated styles in one file |
| Use variables or consistent naming | Copy full CSS for each theme     |
| Minify before production           | Use large unoptimized files      |
| Document differences               | Leave collaborators guessing     |
| Use `.gitkeep` if folder is empty  | Let Git ignore your directory    |

---

## 📘 In Summary

| Concept                   | Meaning                                     |
| ------------------------- | ------------------------------------------- |
| **Folder purpose**        | Stores alternate theme stylesheets          |
| **Files inside**          | `.css` (and optionally `.scss`) theme files |
| **Used for**              | Visual variation without changing structure |
| **Applied by**            | Linking the theme CSS in HTML or JS         |
| **Default files**         | `light.css`, `dark.css`                     |
| **Optional placeholders** | `.gitkeep` (for Git tracking)               |

---

### ✨ Bottom Line

> The `assets/themes/` folder is your website’s **wardrobe** 👕 —
> each file is a different **outfit** for your site.
> Swap them in seconds, test styles easily, and keep your design flexible and future-proof.

---
