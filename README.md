# 🏴‍☠️ pmail

**pmail** stands for *Pirate Mail*. Why? Because.

This repository holds the landing page of [pmail.gr](https://pmail.gr), the email server of a true netizen, hosted in the high seas of the internet.

## Structure

```
.
├── index.html             # English page (default)
├── el/index.html          # Greek page
├── 404.html               # "lost at sea" page, served by GitHub Pages for missing paths
├── style.css              # shared styles for all pages
├── og-image.png           # 1200×630 social preview image
├── apple-touch-icon.png   # 180×180 home-screen icon for iOS
├── CNAME                  # custom domain for GitHub Pages (pmail.gr)
├── LICENSE                # MIT
└── README.md
```

### The page

`index.html` and `el/index.html` share the same layout; only the text differs. No JavaScript.

- **`<head>`**: title, description, canonical URL, `hreflang` links between the two languages, Open Graph and Twitter card tags (using `og-image.png`), an inline SVG favicon (a pirate-flag envelope), the Apple touch icon and the fonts.
- **Fonts**: Nunito from Google Fonts. Nunito has no Greek glyphs, so M PLUS Rounded 1c is loaded as a fallback and covers Greek text with a similar rounded look; the browser only downloads the subsets it needs.
- **`style.css`**: all styling, driven by a few CSS variables in `:root` (`--bg`, `--fg`, `--muted`, `--accent`, `--accent-hover`). Dark theme, centered layout, a short fade-in that is disabled for users who prefer reduced motion.
- **`<body>`**, top to bottom:
  1. `.lang-switch`: link to the other language (EN ⇄ ΕΛ), top right
  2. `h1.title`: the 🏴‍☠️ pmail heading
  3. `.subtitle`: the tagline
  4. intro paragraph
  5. `<section>` with the "why", the list of other projects (`ul.projects`), the Ko-fi link (`.coffee`) and the sign-off (`.signoff`)
  6. `.dots`: closing ornament

When you change the text, change it in both `index.html` and `el/index.html`.

## Running locally

No build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server
```

## Deployment

The site is served by GitHub Pages from the `main` branch; `CNAME` points it at `pmail.gr`. Pushing to `main` publishes it.

## License

[MIT](LICENSE) © Christos Koulaxizis
