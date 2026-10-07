# 🏴‍☠️ pmail

**pmail** stands for *Pirate Mail*. Why? Because.

This repository holds the landing page of [pmail.gr](https://pmail.gr), the email server of a true netizen, hosted in the high seas of the internet.

## Structure

```
.
├── index.html   # the whole site: markup + inline CSS, no JavaScript
├── CNAME        # custom domain for GitHub Pages (pmail.gr)
├── LICENSE      # MIT
└── README.md
```

### The page

`index.html` is a single, self-contained page:

- **`<head>`**: title, description, Open Graph tags and an inline SVG favicon (a pirate-flag envelope).
- **`<style>`**: all styling, driven by a few CSS variables in `:root` (`--bg`, `--fg`, `--muted`, `--accent`, `--accent-hover`). Dark theme, centered layout, a short fade-in that is disabled for users who prefer reduced motion.
- **`<main>`**, top to bottom:
  1. `.title`: the 🏴‍☠️ pmail heading
  2. `.subtitle`: the tagline
  3. intro paragraph
  4. `<section>` with the "why", the list of other projects (`ul.projects`), the Ko-fi link (`.coffee`) and the sign-off (`.signoff`)
  5. `.dots`: closing ornament

## Running locally

No build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server
```

## Deployment

The site is served by GitHub Pages from the `main` branch; `CNAME` points it at `pmail.gr`. Pushing to `main` publishes it.

## License

[MIT](LICENSE) © Christos Koulaxizis
