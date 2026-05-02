# Terra Development Group — Marketing Site

Single-page marketing homepage for **Terra Development Group**, a high-efficiency custom home builder serving northern New Jersey.

**Live site:** https://www.perplexity.ai/computer/a/terra-development-group-WqmhNOG4T9GqQO78XJWACw

---

## Stack

Pure static site — no build step, no dependencies.

- HTML5
- CSS (custom properties, CSS Grid, Flexbox, `clamp()` responsive type)
- Vanilla JS (mobile menu, scroll-aware header)
- Inline SVG logo (T-on-stepped-foundation, navy + gold)
- Google Fonts: Fraunces (serif display) + Inter (body)

## Design

- **Palette:** Navy `#1A3A5C`, Gold `#C4A24A`, Cream `#FAF7F1`
- **Typography:** Fraunces for headings (editorial serif), Inter for body
- **Aesthetic:** Editorial luxury builder — generous whitespace, photography-led, restrained

## Structure

```
terra-site/
├── index.html       # Single-page site
├── styles.css       # All styles (~700 lines)
├── images/          # Hero + section imagery (Unsplash-licensed)
│   ├── hero.jpg
│   ├── interior.jpg
│   ├── process.jpg
│   ├── detail.jpg
│   ├── kitchen.jpg
│   └── blueprint.jpg
└── README.md
```

## Sections

1. **Header** — sticky, scroll-aware with backdrop blur
2. **Hero** — full-bleed photo, dual CTA (Start a Project + Client Portal Login)
3. **Approach** — editorial two-column intro
4. **Why Terra** — four value cards (efficiency, transparency, portal, NJ expertise)
5. **Process** — 10-phase build sequence with sticky photo
6. **Inspiration** — direction studies (architecture, materials, craft)
7. **Values quote** — operating philosophy
8. **Contact** — service area, email, portal link, inquiry form
9. **Footer** — wordmark + nav

## Client portal

The header **Client Login** button, hero CTA, and contact section currently anchor to a `#client-portal` placeholder section on the homepage ("Launching soon"). Once the dashboard is published to a permanent public URL, swap the five `#client-portal` anchor hrefs in `index.html` for the real URL.

## Local development

Just open `index.html` in a browser, or serve the directory:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Image licensing

Hero and section imagery is licensed under the [Unsplash License](https://unsplash.com/license) — free for commercial use, no attribution required. Images will be replaced with real Terra project photography as homes are delivered.

## Deployment

Static bundle — drop into any host (S3 + CloudFront, Netlify, Vercel, GitHub Pages, etc.).
