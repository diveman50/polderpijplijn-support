# Grim Reader Templates

A template changes the look and feel of Grim Reader: colors, fonts, and background images. Templates are distributed as `.grimtemplate` files (a standard zip archive with a custom extension).

## Installing a template

**Option 1 — Share sheet / Files app**
Send the `.grimtemplate` file to your iPhone or iPad via AirDrop, Mail, or Files, then tap it and choose **Open with Grim Reader**.

**Option 2 — In-app import**
Go to **Settings → Appearance → Import template** and pick the file.

The template is installed immediately and selected automatically.

---

## File structure

```
mytemplate.grimtemplate      ← zip archive
├── template.json            ← required
├── background.jpg           ← optional
├── header.png               ← optional
└── footer.png               ← optional
```

Image files can have any name; you reference them by filename from `template.json`. The `template.json` file may be in the root of the zip or inside a single subdirectory — both work.

---

## template.json reference

See [`example.json`](example.json) for a ready-to-use starting point.

### Identity

| Field | Type | Required | Description |
|---|---|---|---|
| `id` | string | yes | Unique identifier — lowercase letters, digits and hyphens only |
| `name` | string | yes | Display name shown in the app |
| `description` | string | yes | Short description |
| `author` | string | yes | Your name |

### Colors

All color fields take a hex string: `"#RRGGBB"` (with `#`, six digits).

| Field | Required | Description |
|---|---|---|
| `color_primary` | yes | Main accent color — section titles, highlights |
| `color_secondary` | yes | Secondary accent |
| `color_background` | yes | App background color |
| `color_text` | yes | Default text color |
| `color_accent` | yes | Interactive accent — buttons, links, toggles |
| `color_muted` | yes | Muted color for captions and secondary text |

### Typography

Use the **PostScript name** of the font (see [`fonts.md`](fonts.md) for the full list).

| Field | Required | Description |
|---|---|---|
| `font_heading` | yes | Font used for headings |
| `font_body` | yes | Font used for body text |
| `font_mono` | yes | Monospace font |

If a font name is not found, iOS falls back to the system font.

### Images

| Field | Type | Description |
|---|---|---|
| `image_background` | string \| null | Filename of the full-screen background image |
| `image_header` | string \| null | Header decoration (reserved for future use) |
| `image_footer` | string \| null | Footer decoration (reserved for future use) |
| `image_book_card_bg` | string \| null | Book card background (reserved for future use) |

#### Image guidelines

| Field | Recommended size | Format | Max file size |
|---|---|---|---|
| `image_background` | ≥ 1290 × 2800 px | JPG | 3 MB |
| `image_header` / `image_footer` | Any | PNG (transparency supported) | 1 MB |

Keep the main subject **centered** — edges are cropped on smaller screens.

### Shape

| Field | Type | Required | Recommended range |
|---|---|---|---|
| `corner_radius` | number | yes | 8 – 20 |
| `shadow_radius` | number | yes | 0 – 10 |

---

## Tips

- Use `Georgia` or `Baskerville` for a classic reading feel; `Avenir` or `Helvetica Neue` for a clean modern look.
- Keep `color_background` light and `color_text` dark (or vice versa) for readable contrast.
- Decorative fonts like `Zapfino` or `Noteworthy` work well for `font_heading` but are hard to read as body text.
- The **Standard** template uses system colors and is not affected by `color_*` fields — only custom templates apply these values.
