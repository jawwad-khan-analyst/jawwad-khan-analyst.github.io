# Jawwad Khan — Data & Financial Analyst Portfolio

A single-page portfolio built with **semantic HTML5** and the **Tailwind CSS CDN**, with
**extensive built-in SEO** ready for Google Search Console.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The complete portfolio (all sections, SEO meta, JSON-LD, dark/light toggle) |
| `robots.txt` | Crawler directives + sitemap reference |
| `sitemap.xml` | Sitemap for Search Console submission |
| `README.md` | This file |

## SEO features included

- **Unique, descriptive title** and meta description (right-length, keyword-rich, non-spammy)
- **Canonical URL**, `robots`/`googlebot` meta directives
- **Open Graph + Twitter Card** tags for rich social sharing
- **JSON-LD structured data** (Schema.org): `ProfilePage` → `Person` (with `sameAs`,
  `email`, `jobTitle`, `knowsAbout`) and `WebSite`
- **E-E-A-T signals**: named author, real contact email, About content, linked GitHub profile
  with `rel="me"` (helps Google associate profiles with you)
- **Semantic landmarks**: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`,
  one `<h1>` with a logical heading hierarchy
- **Accessibility** (also an SEO/quality signal): skip link, `aria-label`s, `alt`-free
  decorative SVGs marked `aria-hidden`, `:focus-visible` outlines, keyboard-friendly toggle
- **Performance**: inline SVG favicon (no extra request), `preconnect`/`dns-prefetch` for
  external origins, no images (CSS-gradient thumbnails), static HTML content (fully crawlable
  without JavaScript)
- **Mobile-friendly**: responsive layout, correct `viewport`, tap-highlight removed
- **Theme-aware `theme-color`** meta for both light and dark mode

## Before you deploy — remaining placeholders

Your domain (`https://jawwad-khan-analyst.github.io/`) is already configured everywhere —
canonical, Open Graph, Twitter, JSON-LD, `robots.txt`, and `sitemap.xml`.

1. **`og-image.png`**: create a 1200×630 social preview image and upload it to your site root,
   or remove the `og:image`/`twitter:image` tags.
2. **Projects**: the four projects use realistic sample content. Swap descriptions,
   tags, and links for your real work; replace the `#` Live Demo links.
3. **Experience**: replace sample companies/dates with your actual history (keep the
   `<time datetime>` attributes machine-readable).
4. **Stats** in the hero: update to real numbers.

## Google Search Console — getting indexed (latest workflow)

1. **Deploy** the folder to any static host (GitHub Pages, Netlify, Vercel, Cloudflare Pages…).
2. **Verify ownership** in [Google Search Console](https://search.google.com/search-console):
   - Add your property (Domain or URL-prefix).
   - Use **HTML tag** verification: paste the meta tag GSC gives you into the `<head>` of
     `index.html`, or use **DNS** verification if you control DNS.
3. **Submit the sitemap**: in GSC → *Sitemaps* → enter `sitemap.xml` → Submit.
4. **Request indexing**: *URL Inspection* → paste `https://yourdomain.com/` → **Request Indexing**.
5. **Re-check after edits**: Google ignores bots.txt changes for up to a day; sitemap changes
   are picked up on recrawl. Use *URL Inspection* again after meaningful updates.
6. **Monitor**: *Performance* (impressions/clicks), *Page Experience* (Core Web Vitals), and
   *Enhancements* (structured data validation) in GSC.

## Production note — Tailwind CDN

The Play CDN (`cdn.tailwindcss.com`) is perfect for this template but is **not recommended for
production** (it adds ~300 KB JS and warns in console). When you're ready:

```bash
npm install tailwindcss @tailwindcss/cli
npx @tailwindcss/cli -i input.css -o styles.css --minify
```

Replace the `<script src="https://cdn.tailwindcss.com">` tag with a `<link rel="stylesheet"
href="styles.css">`, and move the `tailwind.config` into `tailwind.config.js` with
`darkMode: "class"`. The `dark:` classes and the toggle will keep working unchanged.

## Local preview

Just open `index.html` in a browser, or serve it:

```bash
npx serve .
```
