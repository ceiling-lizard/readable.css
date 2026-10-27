# readable.css

**A zero-config, drop-in CSS library that instantly turns raw HTML into beautifully typeset, long-form reading.**

![Version](https://img.shields.io/badge/version-1.0.0-1a5fb4?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-1a5fb4?style=flat-square)
![Size](https://img.shields.io/badge/size-4.5%20KB-1a5fb4?style=flat-square)


No classes, no wrapper divs, no JavaScript. Just link the file and write.

</div>

---

## Features

- **Optimal Measure:** Caps text width at `65ch` (~65 characters) so lines never stretch edge-to-edge on wide monitors.
- **Typography:** 18px base size, 1.6 line-height, normal kerning, and font smoothing for crisp, comfortable reading.
- **Automatic Dark Mode:** Respects `prefers-color-scheme` out of the box, using soft off-black and off-white to prevent glare.
- **Full Semantic Styling:** Automatically styles headings, paragraphs, code blocks, blockquotes, tables, images, lists, and inline elements (like `<mark>` and `<kbd>`).
- **Accessible:** Includes visible focus rings for keyboard navigation, smart text selection colors, and proper contrast ratios.
- **Media Safe:** Images, videos, and iframes are forced to scale within the text column, preventing horizontal scrolling on mobile.

---

## The Files

The library is available in two typographic flavors, each with a standard and minified version:

| File | Description |
| :--- | :--- |
| **`readable.css`** <br> **`readable.min.css`** | **Georgia.** Uses the native Georgia font (with system fallbacks). Best for zero external requests and users on Windows/Mac. |
| **`gelasio.css`** <br> **`gelasio.min.css`** | **Gelasio.** Imports the Gelasio web font from Google Fonts. Best for a consistent, elegant serif look on *all* devices, including Android. |

---

## Usage

Add the stylesheet to the `<head>` of your HTML document. 

**To use the Gelasio version (Recommended):**
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ceiling-lizard/readable.css@main/gelasio.min.css">
```

To use the Georgia version:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ceiling-lizard/readable.css@main/readable.min.css">
```

Note: Replace @main with a specific commit hash or version tag for production to avoid aggressive CDN caching.

Then, simply write plain HTML inside your <body>:

```html
<h1>The Quiet Art of Reading</h1>

<p>This is a paragraph of text. It automatically gets a comfortable measure and line height.</p>

<blockquote>
  "Typography is the craft of endowing human language with a durable visual form."
</blockquote>
```

---

## Customization

You can easily override the default colors by targeting the :root CSS variables in your own stylesheet:

```css
:root {
  --reading-bg: #FAF9F6;        /* Background color */
  --reading-fg: #333333;       /* Main text color */
  --reading-accent: #1a5fb4;   /* Link color */
  --reading-code-bg: #f0ece6;  /* Code block background */
}
```

---

## License

MIT
