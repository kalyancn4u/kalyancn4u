# 🎬 `assets/media/` — Video, Audio & Motion Assets

Welcome! 👋
This folder stores all **multimedia files** used by your website — such as 🎥 **videos**, 🔊 **audio clips**, 🎞️ **background loops**, or 🧩 **animated motion graphics**.

> 💡 Think of this as your website’s **“media library”** —
> where everything that *moves, plays, or sounds* belongs.

---

## 🧱 Purpose of This Folder

The `media/` directory keeps **large, rich-media assets** separate from your core site files, ensuring:

* ✅ faster load times (via lazy loading or CDN hosting)
* ✅ better project organization
* ✅ easy updates or replacements without breaking the layout

---

## 📂 Recommended Folder Structure

```
assets/
└── media/
    ├── videos/
    │   ├── intro.mp4
    │   ├── hero-background.webm
    │   └── tutorial.mp4
    │
    ├── audio/
    │   ├── click.mp3
    │   └── background-loop.ogg
    │
    ├── animations/
    │   ├── logo-lottie.json
    │   └── loader.gif
    │
    ├── thumbnails/
    │   └── video-preview.jpg
    │
    ├── .gitkeep
    └── README.md   ← this file
```

> 🧩 You can adjust the subfolders depending on your project’s needs.
> Keeping videos, audio, and animation files separate improves clarity and load management.

---

## 🎥 File Type Examples

| Media Type              | Common Formats                    | Description                                 |
| ----------------------- | --------------------------------- | ------------------------------------------- |
| **Video**               | `.mp4`, `.webm`, `.ogg`           | Background loops, hero banners, tutorials   |
| **Audio**               | `.mp3`, `.ogg`, `.wav`            | Sound effects, voiceovers, background music |
| **Animation**           | `.json` (Lottie), `.gif`, `.webp` | Motion graphics, logo animations, loaders   |
| **Preview / Thumbnail** | `.jpg`, `.png`, `.webp`           | Static images for previews or fallbacks     |

---

## 🧩 How to Use Media in HTML

### 🎥 Embedding a Video

```html
<video autoplay muted loop playsinline>
  <source src="assets/media/videos/hero-background.webm" type="video/webm">
  <source src="assets/media/videos/hero-background.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

### 🔊 Adding Background Audio

```html
<audio autoplay loop>
  <source src="assets/media/audio/background-loop.mp3" type="audio/mpeg">
</audio>
```

### 🧠 Displaying an Animation (Lottie)

If you’re using [LottieFiles](https://lottiefiles.com/):

```html
<div id="logo-animation"></div>
<script src="https://unpkg.com/lottie-web@latest/build/player/lottie.min.js"></script>
<script>
  lottie.loadAnimation({
    container: document.getElementById('logo-animation'),
    renderer: 'svg',
    loop: true,
    autoplay: true,
    path: 'assets/media/animations/logo-lottie.json'
  });
</script>
```

---

## ⚙️ Optimization Tips (For Beginners)

| Tip                                        | Why It Matters                             |
| ------------------------------------------ | ------------------------------------------ |
| 🎞️ Use `.webm` for short background loops | Smaller size, great quality                |
| 🔈 Compress `.mp3` / `.wav` files          | Faster load and playback                   |
| 🌐 Host large files on a CDN (optional)    | Reduces server load                        |
| 📱 Use `playsinline` on mobile videos      | Prevents fullscreen autoplay interruptions |
| 💤 Lazy-load non-critical videos           | Improves initial page speed                |
| 🧾 Always include fallback formats         | Ensures cross-browser compatibility        |

---

## 🧠 File Size Guidelines

| Type            | Recommended Max Size | Note                                         |
| --------------- | -------------------- | -------------------------------------------- |
| Video           | ≤ 5–10 MB            | Optimize for web (short loops preferred)     |
| Audio           | ≤ 2 MB               | Use compressed `.mp3` or `.ogg`              |
| GIF / Animation | ≤ 1 MB               | Convert heavy GIFs to `.webp` or Lottie JSON |

---

## 🧾 Example Placeholder Files

When starting a new project, you can include:

```
assets/media/videos/.gitkeep
assets/media/audio/.gitkeep
assets/media/animations/.gitkeep
```

This ensures folders exist even before you add media files — helpful when syncing with GitHub.

---

## ⚖️ Best Practices

| ✅ Do                                               | ❌ Don’t                                   |
| -------------------------------------------------- | ----------------------------------------- |
| Use compressed web-friendly formats                | Upload raw `.mov` or `.wav` files         |
| Store source files outside repo (e.g., /raw_media) | Bloat repo with huge files                |
| Keep naming consistent (`hero-bg.webm`)            | Use random names (`video1.mp4`)           |
| Include fallbacks                                  | Assume every browser supports your format |
| Check licenses                                     | Use copyrighted media without permission  |

---

## 🔐 Licensing & Attribution

If your project uses external media (stock videos, icons, sounds):

* Always verify the **usage license** (Creative Commons, royalty-free, etc.).
* Attribute the creator if required (e.g., under CC-BY 4.0).
* Keep a simple `LICENSES.txt` file inside `assets/media/` if you have multiple credited files.

---

## 🧩 Relationship with Other Folders

| Folder          | Role                                 |
| --------------- | ------------------------------------ |
| `assets/img/`   | Static or decorative images          |
| `assets/media/` | Dynamic, playable, or animated media |
| `assets/icons/` | SVGs, favicons, vector symbols       |

> 🧭 Use `img/` for still images and `media/` for motion content.

---

## ✅ Summary

| Concept                | Description                                         |
| ---------------------- | --------------------------------------------------- |
| **Folder Purpose**     | Store videos, audio, and animated assets            |
| **Default Subfolders** | `videos/`, `audio/`, `animations/`, `thumbnails/`   |
| **Output Use**         | Embedded or background multimedia                   |
| **Default File**       | `.gitkeep` to track empty directories               |
| **Linked In**          | HTML `<video>`, `<audio>`, or via JS (e.g., Lottie) |

---

### ✨ Bottom Line

> The `assets/media/` folder is your site’s **creative studio** 🎬 —
> it holds every moving or sounding element that brings your design to life.
> Keep your media organized, lightweight, and web-optimized —
> your users (and your page-load times) will thank you! 🚀

---
