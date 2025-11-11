# 📦 `vendor/` Directory — External Libraries & Dependencies

Welcome! 👋
This folder stores all the **third-party (external)** libraries used by your website —
that is, code you **didn’t write yourself**, but rely on for styling, interactivity, or visuals.

> 🧠 Think of this as your **project’s library shelf** —
> it holds ready-made tools (like Bootstrap or jQuery) that save time and add functionality.

---

## 🧱 Why We Keep a `vendor/` Folder

* ✅ Keeps all external code **separate** from your own (`scripts/`, `css/`).
* ✅ Allows **offline use** — no need for a CDN to load essential libraries.
* ✅ Lets you **control versions** — avoiding unexpected changes.
* ✅ Makes your project **self-contained**, so it can be copied or deployed easily.

---

## 📂 Folder Structure Example

```
assets/
└── vendor/
    ├── bootstrap/
    │   ├── css/
    │   │   └── bootstrap.min.css
    │   └── js/
    │       └── bootstrap.bundle.min.js
    │
    ├── jquery/
    │   └── jquery.min.js
    │
    ├── fontawesome/
    │   ├── css/
    │   │   └── all.min.css
    │   └── webfonts/
    │       └── fa-solid-900.woff2
    │
    ├── chartjs/
    │   └── chart.min.js
    │
    └── README.md   ← this file
```

---

## 📘 Included Libraries

Below is a description of each library bundled here — their **purpose**, **version**, **official source**, and **example usage**.

| Library          | Version | Source / Homepage                             | Purpose                                                  |
| ---------------- | ------- | --------------------------------------------- | -------------------------------------------------------- |
| **Bootstrap**    | 5.3.3   | [getbootstrap.com](https://getbootstrap.com/) | Responsive layout, grid system, ready-made UI components |
| **jQuery**       | 3.7.1   | [jquery.com](https://jquery.com/)             | Simplified DOM manipulation, AJAX, event handling        |
| **Font Awesome** | 6.5.1   | [fontawesome.com](https://fontawesome.com/)   | Vector icons and social logos                            |
| **Chart.js**     | 4.4.1   | [chartjs.org](https://www.chartjs.org/)       | Interactive charts and data visualization                |

---

## 🧩 Example Usage

### 🪶 **Bootstrap**

Include in your HTML `<head>` and `<body>`:

```html
<link rel="stylesheet" href="assets/vendor/bootstrap/css/bootstrap.min.css">
<script src="assets/vendor/bootstrap/js/bootstrap.bundle.min.js"></script>
```

Usage:

```html
<div class="container text-center">
  <h1 class="display-4">Hello, Bootstrap!</h1>
  <button class="btn btn-primary">Click Me</button>
</div>
```

---

### ⚙️ **jQuery**

```html
<script src="assets/vendor/jquery/jquery.min.js"></script>
<script>
  $(document).ready(function() {
    console.log("jQuery is ready!");
  });
</script>
```

---

### 🎨 **Font Awesome**

```html
<link rel="stylesheet" href="assets/vendor/fontawesome/css/all.min.css">
<i class="fas fa-check-circle"></i> Success!
```

---

### 📊 **Chart.js**

```html
<script src="assets/vendor/chartjs/chart.min.js"></script>
<canvas id="myChart"></canvas>
<script>
const ctx = document.getElementById('myChart');
new Chart(ctx, {
  type: 'bar',
  data: {
    labels: ['Red', 'Blue', 'Yellow'],
    datasets: [{
      label: 'Votes',
      data: [12, 19, 3],
    }]
  }
});
</script>
```

---

## ⚖️ Licensing & Attribution

All vendor libraries are included under their original open-source licenses.
Before redistribution or modification, please review each library’s license file or documentation:

| Library      | License Type            | Link                                                                  |
| ------------ | ----------------------- | --------------------------------------------------------------------- |
| Bootstrap    | MIT                     | [License](https://github.com/twbs/bootstrap/blob/main/LICENSE)        |
| jQuery       | MIT                     | [License](https://github.com/jquery/jquery/blob/main/LICENSE.txt)     |
| Font Awesome | CC BY 4.0 / Pro License | [License](https://fontawesome.com/license/free)                       |
| Chart.js     | MIT                     | [License](https://github.com/chartjs/Chart.js/blob/master/LICENSE.md) |

> ⚠️ Never edit vendor files directly — instead, override them in your own CSS or JS to make updates easy and safe.

---

## 🧭 Maintenance Tips for Beginners

| Task                                                 | Why It Matters                          |
| ---------------------------------------------------- | --------------------------------------- |
| **Keep versions labeled** (`bootstrap-5.3.3`)        | Avoid confusion during updates.         |
| **Don’t edit vendor code**                           | Edits will be lost when upgrading.      |
| **Use minified files** (`.min.css`, `.min.js`)       | Faster website performance.             |
| **Add a note** if you replace or upgrade any library | Helps collaborators understand changes. |
| **Use `.gitignore`** if vendor files are huge        | Keeps your repo lean.                   |

---

## 🪶 Optional: Custom Local Libraries

You can also place **non-CDN local dependencies** here, such as:

* Animation libraries (AOS, Anime.js)
* Sliders (Swiper.js, Slick)
* DataTables
* Lightbox / Magnific Popup

Just keep each library in its own subfolder:

```
assets/vendor/swiper/
assets/vendor/aos/
```

---

## ✅ Summary

| Concept                | Meaning                                              |
| ---------------------- | ---------------------------------------------------- |
| **Purpose**            | Store third-party frontend libraries safely          |
| **Who wrote the code** | Other developers (not you)                           |
| **Why store locally**  | Control versions, enable offline use                 |
| **Editing allowed?**   | ❌ No — override in your own code                     |
| **Naming rule**        | `assets/vendor/<library-name>/`                      |
| **Example**            | `assets/vendor/bootstrap/`, `assets/vendor/chartjs/` |

---

### ✨ Bottom Line

> The `vendor/` folder is your website’s **trusted toolbox** 🔧 —
> full of third-party code that powers your layout, interactivity, and visuals.
> Keep it tidy, up-to-date, and documented, and your collaborators (and future you!) will thank you.

---
