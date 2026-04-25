# Vagabond

A personal travel wishlist journal. Write notes, attach photos, organise by tags and continent, and switch between themes. Everything saves automatically in your browser.

---

## Features

**Journal pages**
Each place gets its own ruled page with a title, date, and freeform notes. Pages are numbered and styled to feel like a physical diary.

**Text formatting**
Per-entry controls for font family, font size, text colour, bold, italic, and underline. Six font choices ranging from classical serif to typewriter monospace.

**Photos**
Attach photos to any entry. They display as polaroids (with a natural tilt) or as flat frames. Individual photos can be rotated. Photos are stored as base64 data directly in the browser — no upload service required.

**Tags**
Create custom tags with a name, colour, and icon. Apply multiple tags to any entry. Tags are filterable from the sidebar. Existing tags can be edited or deleted from the manage panel.

**Continents**
Assign each entry to a continent for geographic filtering: Europe, Asia, Americas, Africa and Middle East, or Oceania.

**Themes**
Five visual themes — Parchment, Midnight, Forest, Rose, Slate — switchable at any time from the header. Theme preference is saved automatically.

**Views**
Toggle between a single-column journal view and a multi-column grid view.

**Search**
Live search across entry titles and body text.

**Auto-save**
All content saves to your browser's localStorage 500ms after any change. A small "saved" indicator confirms each write.

---

## Data and privacy

All data is stored in `localStorage` in the browser where you open the site. Nothing is sent to any server. This means:

- Your entries are private by default
- Data does not sync across devices or browsers
- Clearing your browser's site data will erase your entries
- Photos are embedded directly in the saved data — large numbers of high-resolution photos will increase storage size

If you want your journal to follow you across devices, a backend or cloud database would need to be added. This is not included in the current version.

---

## Customisation

The file is self-contained and readable. Common things you may want to change:

- **Default entries** — find `DEFAULT_ENTRIES` near the top of the script block and edit or remove them
- **Default tags** — find `DEFAULT_TAGS` and adjust the names, colours, and icons
- **Themes** — the `THEMES` object defines all colour values; add a new key to create a new theme
- **Fonts** — the `FONT_FAMILIES` array controls what appears in the formatting toolbar; any Google Font loaded in the `<link>` tag can be added here
- **Grid column width** — the grid view uses `minmax(380px, 1fr)`; adjust the pixel value to change card width

---

## Tech stack

- React 18 (loaded from unpkg CDN)
- Babel standalone (JSX transpilation in-browser)
- Google Fonts (Cormorant Garamond, Playfair Display, Lora, DM Sans, Josefin Sans, Special Elite)
- localStorage for persistence
- No build tools, no npm, no framework CLI

---

## Known notes

The browser console will show warnings about Babel source maps. These are cosmetic and do not affect the application. They come from the CDN-hosted Babel standalone build and cannot be suppressed without precompiling the JSX locally.

---

## License

Personal use. Do whatever you like with it.
