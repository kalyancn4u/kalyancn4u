# ⚙️ `assets/scripts/` — JavaScript Files & Site Logic

Welcome! 👋
This folder contains all the **JavaScript files** that bring your website to life — from simple menu toggles to complex animations, data visualizations, and API interactions.

> 🧠 Think of JavaScript as your site’s **brain** 🧩 —
> while HTML builds the structure and CSS defines the look,
> **scripts control the behavior** (interactions, logic, and movement).

---

## 🧱 Purpose of This Folder

The `scripts/` directory holds all **custom JavaScript code** written for your project —
code that you or your team maintain directly.

It helps you:

* ✨ add interactivity and user experience improvements
* ⚙️ manage page events, form validation, and navigation
* 🔗 connect APIs and dynamic data
* 🧩 keep logic separate from presentation (clean architecture)

---

## 📂 Recommended Folder Structure

```
assets/
└── scripts/
    ├── app.js              # Main entry script for the website
    ├── utils.js            # Reusable helper functions
    ├── ui/                 # Scripts for user interface components
    │   ├── menu.js
    │   ├── modal.js
    │   └── carousel.js
    ├── vendor/             # Third-party plugins (if needed locally)
    │   └── .gitkeep
    ├── data/               # Optional JS-based data (static or dynamic)
    │   └── countries.js
    └── README.md           # This file
```

> 💡 Keep your **custom code** here, and use `assets/vendor/` for **external libraries** (like jQuery, Chart.js, etc.).

---

## 🧩 Key Files Explained (Simple Terms)

| File                 | Description                                                                                                     |
| -------------------- | --------------------------------------------------------------------------------------------------------------- |
| **`app.js`**         | The main file that initializes your website’s JavaScript. Often runs on page load and controls global behavior. |
| **`utils.js`**       | Small, reusable helper functions (e.g., format dates, random numbers, toggle classes).                          |
| **`ui/menu.js`**     | Manages navigation menus (e.g., mobile menu open/close).                                                        |
| **`ui/modal.js`**    | Handles modals, popups, or dialog boxes.                                                                        |
| **`ui/carousel.js`** | Controls sliders, carousels, or rotating banners.                                                               |
| **`data/`**          | Optional — if you keep small, local data sets (e.g., lists or configs).                                         |
| **`vendor/`**        | Optional — for third-party scripts not installed via CDN.                                                       |

---

## 💻 Example: `app.js`

```js
// app.js — Main script controlling global site behavior

// Wait until page content is fully loaded
document.addEventListener("DOMContentLoaded", () => {
  console.log("✅ Website JavaScript is loaded!");

  // Example: Toggle mobile menu
  const menuBtn = document.querySelector("#menu-btn");
  const navMenu = document.querySelector("#nav-menu");

  if (menuBtn && navMenu) {
    menuBtn.addEventListener("click", () => {
      navMenu.classList.toggle("open");
    });
  }
});
```

---

## 🧩 Example: `utils.js`

```js
// utils.js — Common helper functions

export function toggleClass(element, className) {
  element.classList.toggle(className);
}

export function formatDate(date) {
  return new Date(date).toLocaleDateString();
}
```

---

## ⚙️ How to Link JavaScript in HTML

Place this near the end of your `<body>` tag:

```html
<script src="assets/scripts/utils.js"></script>
<script src="assets/scripts/app.js"></script>
```

If you’re using modules (ES6+), use `type="module"`:

```html
<script type="module" src="assets/scripts/app.js"></script>
```

---

## 🧭 Folder Relationships

| Folder            | Role                                  |
| ----------------- | ------------------------------------- |
| `assets/scripts/` | Your **custom** site logic            |
| `assets/vendor/`  | **Third-party** scripts and libraries |
| `assets/data/`    | Static or JSON-based data for scripts |

---

## 🪶 Good Practices for Beginners

| Do ✅                                         | Don’t ❌                                |
| -------------------------------------------- | -------------------------------------- |
| Organize scripts by feature (`ui/`, `data/`) | Dump everything into one file          |
| Comment your code                            | Write cryptic logic                    |
| Keep reusable helpers in `utils.js`          | Repeat code everywhere                 |
| Load scripts just before `</body>`           | Block page rendering by loading early  |
| Use `DOMContentLoaded` event                 | Run scripts before page is ready       |
| Use modules (`import/export`)                | Mix everything in global scope         |
| Minify before deployment                     | Push unoptimized scripts to production |

---

## 🧰 Example: Project Initialization Order

```
1️⃣ utils.js — helper functions
2️⃣ ui/menu.js, ui/modal.js — feature scripts
3️⃣ app.js — initializes everything together
```

`app.js`

```js
import { toggleClass } from "./utils.js";

document.addEventListener("DOMContentLoaded", () => {
  const nav = document.querySelector(".nav");
  document.querySelector(".nav-toggle").addEventListener("click", () => {
    toggleClass(nav, "open");
  });
});
```

---

## ⚡ Using Modern Tools (Optional)

You can use a **build process** (like Webpack, Vite, or Parcel) to:

* bundle multiple scripts into one file (for performance),
* transpile ES6+ features (for older browsers),
* and minify automatically for production.

Example build output:

```
assets/scripts/
├── app.js          (your editable code)
└── app.min.js      (optimized version for deployment)
```

---

## 🧾 Defaults and Placeholders

If starting fresh, create:

```bash
mkdir -p assets/scripts/ui assets/scripts/vendor assets/scripts/data
touch assets/scripts/{app.js,utils.js}
touch assets/scripts/ui/{menu.js,modal.js,carousel.js}
touch assets/scripts/vendor/.gitkeep
```

Then, add a starter line inside each file:

```js
// Placeholder for [filename].js — to be implemented
```

---

## 💡 Tips for Collaboration

| Scenario             | Recommendation                                                          |
| -------------------- | ----------------------------------------------------------------------- |
| New teammate joins   | They should start by reading this `README.md`                           |
| Adding a new feature | Create a new JS file inside the proper subfolder (`ui/`, `data/`, etc.) |
| Using a plugin       | Place it under `assets/vendor/`                                         |
| Code review          | Ensure comments and naming match function purpose                       |

---

## ✅ Summary

| Concept              | Explanation                                 |
| -------------------- | ------------------------------------------- |
| **Folder Purpose**   | Holds your site’s JavaScript logic          |
| **Primary File**     | `app.js` — main controller                  |
| **Supporting Files** | `utils.js`, `ui/` components                |
| **Output**           | Interactive, dynamic site behavior          |
| **Linked From**      | `<script src="assets/scripts/app.js">`      |
| **Avoid Mixing**     | Don’t mix custom code with vendor libraries |

---

### ✨ Bottom Line

> The `assets/scripts/` folder is your website’s **control center** ⚙️ —
> it handles logic, interactivity, and dynamic behavior.
> Keep it modular, readable, and clean — and your site will stay fast, scalable, and easy to maintain. 🚀

---
