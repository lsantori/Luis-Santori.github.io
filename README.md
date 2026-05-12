# Luis E. Santori — Academic Website

A static, hand-written academic site. No build step. Open `index.html` in a browser to view locally; upload everything to any static host (GitHub Pages, Netlify, Cloudflare Pages, your department's web space) to publish.

## File layout

```
santori-site/
├── index.html             ← Home / About
├── research.html          ← Research interests in depth
├── publications.html      ← Publications, presentations, awards, funding
├── blog.html              ← Notebook (blog) index
├── styles.css             ← Shared stylesheet for the whole site
└── posts/                 ← Blog posts
    ├── why-hilbert-19.html
    ├── first-weeks-at-purdue.html
    └── notes-on-de-giorgi.html
```

## Design notes

- **Typography**: Fraunces (variable, for display) and EB Garamond (body), loaded from Google Fonts. Both editorial serifs, well suited to a mathematics site.
- **Palette**: warm paper cream `#efe6d2`, warm dark ink `#1c1611`, and a deep oxblood accent `#7a2424`. All defined as CSS variables at the top of `styles.css`.
- **Responsive**: mobile breakpoint at 760px. Cards collapse to single column, the masthead glyph hides, navigation reflows.

## Adding a new blog post

1. Copy any existing file in `posts/` to a new filename, e.g. `posts/my-new-post.html`.
2. Update the `<title>`, the `<meta name="description">`, the date in `.post-head .post-date`, the `<h1>` (use `<em>` for italic emphasis in the accent color), and the article body.
3. In `blog.html`, add a new `<a class="post-row">` block at the top of the `.post-list` section pointing at your new file. Earlier-dated posts move down.

## Customizing the look

- Swap the **palette**: change the CSS variables `--bg`, `--ink`, `--accent`, etc. in the `:root` block at the top of `styles.css`.
- Swap the **fonts**: change the Google Fonts `<link>` in every HTML file's `<head>` and the `--display` / `--body` variables in `styles.css`.
- Swap the **glyph**: the small SVG in the masthead of `index.html` (crescent + curve) can be replaced with any inline SVG of your choosing — a tile graph, a Riemann surface, whatever you prefer.

## Notes on the content

The CV-derived facts (advisors, awards, publications, presentations) come straight from the 2025 CV you provided. The three sample blog posts are placeholder writing — fully replace them with your own voice when you're ready.

The home page lists "Currently reading" entries and a "thesis manuscript" as if mid-stride; adjust as the year unfolds.
