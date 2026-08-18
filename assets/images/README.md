# Images

The page ships with CSS-generated placeholders so it looks finished with no photos.
Drop real files in here and swap the placeholder rules in `styles.css`.

| File | Used by | Suggested size | Notes |
| --- | --- | --- | --- |
| `hero.jpg` | `.hero-media` | 2400×1400 | Wide shot of Ichan-Qala or Kalta Minor at golden hour |
| `about-1.jpg` | `.photo-tall` | 900×1260 | Portrait — Kalta Minor works well |
| `about-2.jpg` | `.photo-short` | 900×1020 | Portrait — city walls at dusk |
| `place-kalta-minor.jpg` | first card | 800×500 | |
| `place-itchan-kala.jpg` | second card | 800×500 | |
| `place-tosh-hovli.jpg` | third card | 800×500 | |
| `place-islam-khoja.jpg` | fourth card | 800×500 | |
| `og-cover.jpg` | social preview | 1200×630 | What shows in Telegram/WhatsApp link previews |

## Swapping a placeholder

In `styles.css`, replace the `background:` gradient with the photo:

```css
.hero-media {
  background: url("assets/images/hero.jpg") center / cover no-repeat;
}
```

For the cards, target them individually:

```css
.cards .card:nth-child(1) .card-media {
  background: url("assets/images/place-kalta-minor.jpg") center / cover no-repeat;
}
```

## Before you upload

- Export at ~80% JPEG quality and run them through an optimiser — hero photos
  routinely ship at 4 MB when they could be 300 KB.
- Convert to WebP if you can; every browser you care about supports it now.
- Use your own photos or properly licensed ones. Khiva is heavily photographed
  on stock sites, and a tourism site that gets a copyright complaint on day one
  is an avoidable problem.
