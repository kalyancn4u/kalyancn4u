# 🧵 `assets/scss/` — Sass / SCSS Source Files

Welcome! 👋
This folder contains your **Sass (SCSS)** source files — the *modular, developer-friendly* version of your CSS styles.

> 💡 **SCSS = “Sassy CSS”**
> It extends normal CSS with features like **variables**, **nesting**, **mixins**, and **partials** that make writing and maintaining styles much easier.

---

## 🧱 Purpose of This Folder

The `scss/` folder stores **uncompiled source files** that will later be converted into final `.css` files (usually in the `assets/css/` directory).

Keeping SCSS separate from CSS helps you:

* 🧩 organize styles into smaller, reusable modules
* ⚙️ change global variables (like colors or fonts) easily
* 🎨 maintain consistent design patterns across the site
* 🚀 compile & minify automatically during builds

---

## 📂 Recommended Folder Structure

```
assets/
└── scss/
    ├── _variables.scss     # Global variables (colors, fonts, spacing)
    ├── _mixins.scss        # Reusable mixins (functions for styles)
    ├── _base.scss          # Base resets (html, body, headings)
    ├── _layout.scss        # Page structure (containers, grids)
    ├── _components.scss    # Buttons, cards, modals, etc.
    ├── _utilities.scss     # Helper classes (margins, padding, etc.)
    ├── main.scss           # Imports all partials into one master file
    └── README.md           # This file
```

> 🧩 Files starting with an **underscore** (`_`) are called **partials** —
> they are not compiled individually, but imported into `main.scss`.

---

## ⚙️ Example: Import Structure

`main.scss`

```scss
// Import all partials (order matters)
@import 'variables';
@import 'mixins';
@import 'base';
@import 'layout';
@import 'components';
@import 'utilities';
```

When you compile `main.scss`, it becomes a single optimized CSS file:

```
assets/css/main.css
```

---

## 🧶 Basic Example Files

### `_variables.scss`

```scss
// Color palette
$primary-color: #007acc;
$secondary-color: #005b99;

// Fonts
$font-family: 'Roboto', sans-serif;
```

### `_mixins.scss`

```scss
// A reusable function for responsive design
@mixin respond($breakpoint) {
  @if $breakpoint == small {
    @media (max-width: 600px) { @content; }
  }
  @else if $breakpoint == medium {
    @media (max-width: 900px) { @content; }
  }
}
```

### `_base.scss`

```scss
// Basic resets
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: $font-family;
  background-color: #fff;
  color: #333;
}
```

---

## 🧰 How to Compile SCSS → CSS

You can use **any compiler** (Sass CLI, VS Code extension, or build tool).

### 🔹 Using the Sass CLI (beginner-friendly)

Run this command in your project root:

```bash
sass assets/scss/main.scss assets/css/main.css
```

This compiles SCSS into CSS.

### 🔹 Watch Mode (auto-update on save)

```bash
sass --watch assets/scss/main.scss:assets/css/main.css
```

💡 Each time you edit and save an `.scss` file, Sass will recompile it automatically.

---

## 🧭 Folder Relationships

| Folder         | Role                            | Output        |
| -------------- | ------------------------------- | ------------- |
| `assets/scss/` | Developer-friendly source files | Input (.scss) |
| `assets/css/`  | Compiled production files       | Output (.css) |

---

## 🧩 Naming Conventions (Beginner Tips)

| File Type   | Naming Example     | Purpose                  |
| ----------- | ------------------ | ------------------------ |
| Variables   | `_variables.scss`  | Store reusable values    |
| Mixins      | `_mixins.scss`     | Define reusable patterns |
| Base        | `_base.scss`       | Set global defaults      |
| Layout      | `_layout.scss`     | Define structure, grids  |
| Components  | `_components.scss` | Buttons, cards, etc.     |
| Utilities   | `_utilities.scss`  | Helper classes           |
| Master File | `main.scss`        | Imports everything       |

---

## 🎨 Example Compilation Flow

```
1️⃣ You write/edit → assets/scss/_variables.scss
2️⃣ You import it into → assets/scss/main.scss
3️⃣ You compile main.scss → assets/css/main.css
4️⃣ You link it in your HTML → <link rel="stylesheet" href="assets/css/main.css">
```

---

## 💡 Tips for Beginners

| Tip                              | Why It Helps                             |
| -------------------------------- | ---------------------------------------- |
| Keep variables in one place      | Easy color/font updates                  |
| Use partials and imports         | Organized and modular styles             |
| Don’t edit compiled CSS directly | Always change SCSS files                 |
| Use watch mode                   | Saves time; auto-compiles changes        |
| Minify CSS for production        | Reduces file size and improves load time |
| Include comments                 | Helps teammates understand structure     |

---

## ⚖️ Good Practices

| ✅ Do                                  | ❌ Don’t                               |
| ------------------------------------- | ------------------------------------- |
| Use `_filename.scss` for partials     | Compile every small file individually |
| Use logical naming (`_buttons.scss`)  | Dump all code in one big file         |
| Keep SCSS DRY (Don’t Repeat Yourself) | Copy/paste similar code               |
| Store mixins/functions separately     | Mix logic and design in one file      |

---

## 📘 Example: Minimal Starter Set (for quick setup)

If you just need a simple base to start with, use:

```
assets/scss/
├── _variables.scss
├── _base.scss
└── main.scss
```

`main.scss`

```scss
@import 'variables';
@import 'base';
```

---

## 🧾 Example `.gitkeep` and Defaults

If you’re setting up this directory fresh:

```bash
mkdir -p assets/scss
touch assets/scss/{_variables.scss,_mixins.scss,_base.scss,_layout.scss,_components.scss,_utilities.scss,main.scss,.gitkeep}
```

Then add a brief comment in each file:

```scss
// Placeholder for SCSS partial: customize as needed.
```

---

## ✅ Summary

| Concept             | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| **Folder Purpose**  | Store modular SCSS source files                              |
| **Output Location** | Compiled CSS → `assets/css/`                                 |
| **Key Advantage**   | Clean, reusable, and maintainable styles                     |
| **Default Files**   | `_variables.scss`, `_mixins.scss`, `_base.scss`, `main.scss` |
| **How to Compile**  | `sass assets/scss/main.scss assets/css/main.css`             |

---

### ✨ Bottom Line

> The `assets/scss/` folder is your **design workshop** 🎨 —
> where you build, tweak, and polish styles before they’re ready for production.
> It keeps your website’s visual code clean, modular, and easy to evolve.

---
