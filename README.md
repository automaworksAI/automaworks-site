# AutomaWorks Marketing Site

Single-page marketing and lead-capture site for AutomaWorks, a done-for-you AI automation agency serving small businesses in Southern California.

Goal: drive qualified small-business owners to book a free 30-minute Automation Audit via Calendly.

## Stack

- Vanilla HTML, CSS, JavaScript — no build step
- Google Fonts: Fraunces (display) + Inter (body)
- Google Analytics 4 (stubbed — replace measurement ID before launch)
- Calendly link CTAs (placeholder URL — replace before launch)
- Designed for GitHub Pages with a custom domain

## Project structure

```
/
├── index.html              Main landing page
├── 404.html                Custom not-found page
├── CNAME                   Custom domain (automaworks.ai placeholder)
├── robots.txt
├── sitemap.xml
├── site.webmanifest
├── README.md
├── DECISIONS.md            Open questions and placeholders to resolve before launch
├── claude-code-brief.md    Full build brief
├── ai-automation-landing.html  Original prototype (reference only)
└── assets/
    ├── css/styles.css      All site styles
    ├── js/main.js          Scroll-reveal + GA4 cta_click tracking
    └── img/                Favicons, OG image, app icons (NOT YET CREATED)
```

## Run locally

No build step. Two options:

**Python:**
```
python3 -m http.server 8000
```

**Node (if you have it):**
```
npx serve .
```

Then open http://localhost:8000.

## Edit copy

All copy lives in `index.html`. Sections are commented in the original prototype but preserved as semantic landmarks here. The headline structure uses italicized emphasis via `<em>` tags inside `<h1>` and `<h2>`.

## Edit visuals

All styling lives in `assets/css/styles.css`. Design system colors and spacing are defined as CSS custom properties at the top of the file. Change once, everywhere updates.

## Deploy to GitHub Pages

1. Push this repo to GitHub (public, or private with Pages enabled).
2. Settings → Pages → build from `main` branch, `/ (root)`.
3. Update `CNAME` with your real custom domain (currently `automaworks.ai`).
4. Configure DNS at your registrar:
   - CNAME record from `www` → `<github-username>.github.io`
   - Apex (`@`) → 4 A records pointing at GitHub Pages IPs (185.199.108-111.153)
5. Enable "Enforce HTTPS" in Pages settings (after cert provisions, ~10 min).
6. Verify in Google Search Console (add the verification meta tag to `index.html` `<head>`).
7. Submit `sitemap.xml` to Search Console.

## Pre-launch checklist

See `DECISIONS.md` for placeholders that MUST be replaced before going live:
- [ ] Final domain in `CNAME`, OG tags, JSON-LD, sitemap, robots
- [ ] Real Calendly URL (currently `https://calendly.com/automaworks/audit`)
- [ ] GA4 measurement ID (currently `G-XXXXXXXXXX`)
- [ ] Real OG image at `/assets/img/og-image.jpg` (1200×630)
- [ ] Favicon set in `/assets/img/`
- [ ] Decide on guarantee phrasing (see DECISIONS.md)
- [ ] Decide on testimonials (currently illustrative — see DECISIONS.md)

Verify before launch:
- [ ] All CTAs route to real Calendly link
- [ ] OG validated at https://www.opengraph.xyz/
- [ ] Rich results pass at https://search.google.com/test/rich-results
- [ ] Lighthouse ≥95 on deployed URL (desktop)
- [ ] Tested on real mobile device

## Analytics

GA4 events tracked:
- `page_view` (default)
- `cta_click` with `cta_id`, `cta_label`, `cta_href` — fires on any element with `data-cta` attribute

## Accessibility

- Skip-to-main link
- Visible focus states (bronze outline)
- Semantic landmarks (`<main>`, `<nav>`, `<header>`, `<footer>`, `<article>`, `<section>`, `<figure>`)
- All decorative SVGs marked `aria-hidden="true"`
- FAQ uses native `<details>`/`<summary>` (keyboard-accessible by default)
- `prefers-reduced-motion` disables floating cards and scroll-reveal
- Reveal animations gracefully degrade without JS

## License

All rights reserved. Proprietary.
