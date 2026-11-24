# SMART English · Catalog Entry Maker v1.4

A dependency-free browser utility that generates validated, ready-to-paste entries for the `catalog.js` file in the **SMART English — Digital Learning Showcase** (Web-Apps-Hub).

Fully client-side and offline-friendly—no build step, server, or external proxy required.

## What’s New in v1.4

- **Included Modules / Child Builds Repeater:** Add nested `children` items (`title`, `subtitle`, `summary`, and optional direct `url`) for multi-grade families like **SMART Readers** or multi-mode demos like **SMART Match & Catch**.
- **Duplicate ID Guard (`catalog.js` Loader):** Load your existing `catalog.js` file once to extract all existing IDs and get an instant warning if a new slug collides with an existing route.
- **Required Field Validation:** Validates essential fields (`Title`, `ID`, `Summary`, and `Era` for Legacy items) before generating output so incomplete blocks never reach your catalog.
- **Card Banner Gradient Dropdown:** Choose from 12 curated presets (Ocean Sky, Deep Navy, Sunset Ember, Warm Amber, Emerald Meadow, Archive Plum, etc.) with a live swatch preview, or select **Custom CSS gradient…** to enter your own.
- **Offline Clipboard Fallback:** Automatically selects the generated block and falls back gracefully if browser clipboard permissions are restricted under `file://`.
- **README URL Verification Notice:** Flags extracted HTTPS URLs so you verify they point to the playable demo rather than a documentation link.

## Features

- One-click template presets for **New Application**, **Project / Family**, and **Legacy Entry**
- Local `README.md` extraction (first `#` heading, opening paragraph, and first `https://` link)
- Live auto-slug generation while typing the title (pauses automatically if you customize the ID)
- Automatic YouTube URL normalization (`watch`, `youtu.be`, `/shorts/`, and `/live/` → `/embed/`)
- Generates properly escaped JavaScript objects matching `window.SHOWCASE_CATALOG`
- One-click **Copy Code** (with offline selection fallback) and **Download .txt**

## How to Use

1. Open `catalog-entry-maker-v1.4.html` (or `index.html`) in any modern browser.
2. *(Optional)* Load your existing `catalog.js` under **2. Duplicate ID Guard** so the tool can check for duplicate slugs.
3. Choose a template preset (**New Application**, **Project / Family**, or **Legacy Entry**) or upload a `README.md` file under **1. Auto-Fill from README.md**.
4. Complete the required fields (`Title`, `ID`, `Summary`) and choose a **Card Banner Gradient** from the dropdown.
5. For multi-grade or multi-module projects, click **+ Add Child Module** under **4. Included Modules / Child Builds** to add each sub-item.
6. Click **✦ Generate Catalog Block**, then copy or download the output and paste it into `window.SHOWCASE_CATALOG` inside `catalog.js` before the closing `];`.

## Hosting / Local Use

- Single self-contained static HTML file with zero external dependencies.
- Keep it inside your local Web-Apps-Hub workspace (or a private tools directory) and double-click to launch offline, or host it on Cloudflare Pages, Netlify, or GitHub Pages.

## Credits

Companion tool for the Web-Apps-Hub Showcase for **Ankara Yayıncılık / SMART English**.
Created by **Ehsan Ashour Zadeh**.

---

Made to make adding new digital learning products to the Showcase faster, safer, and more consistent.
