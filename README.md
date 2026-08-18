# Karvon — Landing Page

Static landing page for **Karvon**, a tourism aggregator for Khiva, Urgench and the
Khorezm region of Uzbekistan.

Live at **[karvon-khiva.uz](https://karvon-khiva.uz)**.

## What this is

Plain HTML and CSS, no build step, no framework, no dependencies. Open `index.html`
in a browser and it works. That is deliberate — the page is a placeholder while the
Telegram bot and backend are built, and it should stay cheap to host and edit.

```
index.html              Everything — markup, plus ~60 lines of JS for language + nav
styles.css              All styling
assets/images/          Photos go here (see the README inside)
```

## Languages

The page ships in English, Russian and Uzbek. Switching is handled by a small
script at the bottom of `index.html`:

- Any element with `data-i18n="some.key"` gets swapped on language change.
- English lives in the HTML itself; Russian and Uzbek live in the `STRINGS` object.
- To add a string: add `data-i18n="my.key"` to the element, then add `"my.key"`
  to both `STRINGS.ru` and `STRINGS.uz`. A missing key falls back to English
  rather than breaking.

## Local preview

Just open the file, or serve it if you prefer:

```bash
python3 -m http.server 8000
```

## Images

The page uses CSS-generated placeholders so it looks complete without any photos.
See `assets/images/README.md` for the file list and how to swap them in.

## Roadmap

- [ ] Real Khiva photography
- [ ] Live Telegram bot link (currently a placeholder)
- [ ] Featured hotels and places pulled from the Karvon API
- [ ] Per-language URLs for SEO (`/ru/`, `/uz/`) instead of client-side switching
