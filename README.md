# SMART English · Catalog Entry Maker v1.3

A small, dependency-free browser utility that generates ready-to-paste entries for the `catalog.js` file in the **SMART English — Digital Learning Showcase** (Web-Apps-Hub).

Fully client-side and offline-friendly—no build step, server, or external proxy required.

## What’s New in v1.3

- **Structured Sectioned UI:** Organized into three clear sections (*1. Identity & Classification*, *2. Description & Tech Stack*, and *3. Demo, Visuals & Video*) alongside a dedicated **Quick Auto-Fill from README.md** import box.
- **Safe Toolbar Separation:** Moved **↺ Reset Form** to the top-right template toolbar so it cannot be triggered accidentally next to **✦ Generate Catalog Block**.
- **Live Gradient Swatch Preview:** Displays a real-time color preview beside the **Card Banner Gradient** field as you type or switch presets.
- **YouTube URL Auto-Normalizer:** Automatically converts standard `youtube.com/watch?v=...`, `youtu.be/...`, `/shorts/`, and `/live/` links into `https://www.youtube.com/embed/...` format when generating the entry.
- **Full `catalog.js` Schema Parity:** Supports `era` (for Legacy Showcase grouping), `demo.note` (for `external-first` Storyline 360 modules), `videos` arrays, and live auto-slugging from the Title field.

## Features

- One-click presets for **New Application**, **Project / Family**, and **Legacy Entry**
- Local `README.md` extraction:
  - First `#` heading → Title (and auto-slug for ID)
  - Opening paragraph → Summary
  - First `https://` link → Demo URL
- Live auto-slug generation while typing the title (pauses automatically if you customize the ID)
- Automatic YouTube URL normalization for walkthrough videos
- Generates a properly escaped JavaScript object matching `window.SHOWCASE_CATALOG`
- One-click **Copy Code** and **Download .txt**
- Works directly from disk (`file://`) or on static hosting

## How to Use

1. Open `index.html` (or `catalog-entry-maker-v1.3.html`) in any modern browser.
2. Choose a template preset (**New Application**, **Project / Family**, or **Legacy Entry**).
3. Optionally upload a `README.md` file and click **Extract Fields** to pre-fill title, summary, and demo URL.
4. Review or complete the fields across the three sections:
   - For **Legacy** entries, fill the **Era** field so the item groups under the matching era heading.
   - For **Storyline 360** projects, set **Embed Mode** to `external-first` and optionally add a **Demo Note**.
   - To include a walkthrough video, paste any standard YouTube link (`watch`, `youtu.be`, `/shorts/`, or `/embed/`).
5. Click **✦ Generate Catalog Block**.
6. Click **Copy Code** (or **Download .txt**) and paste the object into the `window.SHOWCASE_CATALOG` array in `catalog.js` just before the closing `];`.

## Hosting / Local Use

- Single self-contained static HTML file with zero external dependencies.
- Keep it inside your local Web-Apps-Hub workspace (or a private tools directory) and double-click to launch offline, or host it on Cloudflare Pages, Netlify, or GitHub Pages.

## Notes

- All generated output is plain text and fully editable after pasting into `catalog.js`.
- Legacy entries without an `era` value default to a generic historical group—always populate the **Era** field for consistent grouping.

## Credits

Created by **Ehsan Ashour Zadeh** for **Ankara Yayıncılık / SMART English**  
Companion tool for the Web-Apps-Hub Showcase.  

---

Made to make adding new digital learning products to the Showcase faster, safer, and more consistent.
