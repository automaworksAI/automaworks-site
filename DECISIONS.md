# Open Decisions & Placeholders

Track every placeholder in the v1 scaffold. Resolve before launch.

## Must resolve before launch

| # | Item | Current placeholder | Owner | Status |
|---|------|---------------------|-------|--------|
| 1 | Brand name | `AutomaWorks` | Emerson | ✅ Resolved 2026-04-16 |
| 2 | Custom domain | `automaworks.ai` | Emerson | ✅ Resolved 2026-04-16 — purchased |
| 3 | Calendly URL | `https://calendly.com/emerson-automaworks/30min` | Emerson | ✅ Resolved 2026-04-16 — live |
| 4 | GA4 measurement ID | `G-XXXXXXXXXX` (2 occurrences in `index.html`) | Emerson | Pending |
| 5 | OG image | `/assets/img/og-image.jpg` (file does NOT yet exist, 1200×630) | Emerson | Pending |
| 6 | Favicon set | `/assets/img/{favicon.ico, icon-192.png, icon-512.png, apple-touch-icon.png}` (files do NOT yet exist) | Emerson | Pending |
| 7 | Guarantee phrasing | "ROI in 60 days, or we work for free until you get it" — keep, or wire measurement framework? | Emerson | Pending |
| 8 | Testimonials | Three illustrative (Marco R. / Dr. Dana L. / Sarah K.) — replace with real, label as illustrative, or remove section? | Emerson | Pending |
| 9 | Phone number | Not present in nav. Add? | Emerson | Pending |
| 10 | Search Console verification | No meta tag in `<head>` yet | Emerson | Pending — add after deploying |
| 11 | "A Day in the Life" moments | Six illustrative scenarios across niches in `#moments` section. Currently framed honestly as "everyday moments" rather than real client logs. Replace with real Automa run-data once available. | Emerson | Pending |
| 12 | AI agent name | Section uses neutral "Handled" label. No agent persona named yet (USH case study uses "Sophie"). Decide if AutomaWorks ships a named house assistant ("Automa", "Auto", etc.) before adding it to copy. | Emerson | Pending |

## Deferred to v1.1

- Add fifth core module: "Organic Visibility / Local SEO"
- Live Chatbase ("Automa") bot embed
- Multi-step contact form with industry qualifier (currently CTAs go to Calendly + mailto)
- Dedicated case-study pages per niche
- Blog / content engine for SEO
- Free audit lead magnet (PDF that drops after Calendly booking)
- Video walkthrough of Sophie in the hero
- Client login area for Care Plan dashboard
- Spanish-language version

## Where placeholders appear

Quick reference for find-and-replace before launch:

```
automaworks.ai          → real domain
G-XXXXXXXXXX            → real GA4 measurement ID
calendly.com/automaworks/audit  → real Calendly link
emerson@usaish.com      → confirm correct contact email (currently real)
```

## Notes from build

- Scaffold built 2026-04-16, vanilla HTML/CSS/JS, no build step.
- Reference prototype preserved at `ai-automation-landing.html` for future visual diff.
- Brief preserved at `claude-code-brief.md`.
