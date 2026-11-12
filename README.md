# Space Value Foundation — static site

A static site (HTML + CSS only, no JavaScript) summarising spacevaluefoundation.com.
Every page uses relative links, so the folder works on any host as-is.

## Files
- `index.html` — the one-page summary (home)
- `styles.css` — home page styling, animations and the star field
- `pages.css` — styling for all inner pages (typographic layout, breakout boxes, navigation cues)
- `blog.html` + `blog-*.html` — blog index and six posts
- `policies.html` + `*-policy.html` — policy hub and nine policies
- `support.html` — corporate and individual support
- `404.html` — not-found page (GitHub Pages uses it automatically)
- `sitemap.xml`, `robots.txt` — for search engines
- `img/` — images copied from the WordPress site (converted to WebP)

## Moving to a different address
The only absolute URL is `https://adewebb65.github.io/SVF/`. It appears in:
- the `<link rel="canonical">` and `og:url` tags at the top of each `.html` file
- `sitemap.xml`
- `robots.txt`

Find and replace `https://adewebb65.github.io/SVF/` with the new address (keep the trailing `/`) across all files. Nothing else needs to change.

## Forms
The WordPress forms (privacy, complaints, appeals, etc.) are replaced by email boxes that open
a message to info@spacevaluefoundation.com and list what to include.

## Browser support
Scroll-triggered build effects and the reading-progress bar use CSS scroll-driven animations
(Chrome, Edge, Opera, Safari 26+). Other browsers show all content fully, without the effects.

## Hosting on GitHub Pages
Pushes to `main` deploy via `.github/workflows/static.yml`.
