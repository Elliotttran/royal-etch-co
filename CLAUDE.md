# CLAUDE.md — Petaluma Glass Works

## Project Context
Static website for a one-person glass etching business in Petaluma, CA. No e-commerce — this is a portfolio + lead generation site. The owner does custom glass etching for two main audiences: car/garage guys and wedding/event clients.

## Architecture
- Pure static HTML/CSS/JS — no framework, no build step
- All pages live in `public/`
- Each HTML file is self-contained with inline `<style>` and `<script>` tags
- Deploy target: Netlify (publish dir: `public/`)

## Design System
- **Palette:** Cream `#F5F0E8`, Ink `#1A1612`, Rust `#A0522D`, Gold `#B8942E`, Warm White `#FAF8F4`
- **Fonts:** Playfair Display (display/headings), DM Sans (UI/nav/labels), Libre Baskerville (body prose)
- **Aesthetic:** Americana heritage craft — warm, textured, premium but approachable. NOT slick/techy.
- **CSS variables** are defined in `:root` on each page — keep consistent across all files

## Key Patterns
- Scroll-reveal animations via IntersectionObserver (`.reveal` class)
- Sticky nav with scroll-triggered compact state (`nav.scrolled`)
- Mobile: hamburger toggle, stacked grids
- Page heroes use `page-hero` class with radial gradient overlays
- Noise texture overlay via SVG filter on `body::before`

## Pages
| File | Purpose |
|------|---------|
| `index.html` | Homepage — hero, project cards, services preview, about preview, testimonial, contact |
| `services.html` | Detailed services — 4 service blocks, process, pricing, FAQ |
| `about.html` | Story, values, workshop gallery, testimonials, local roots |
| `quote.html` | Lead form — project type, budget, timeline, sidebar with pricing + contact |

## What's Placeholder
- All images are dark `<div>`s with emoji icons — need real photos
- Contact info (email, phone, Instagram) are fake — need real values
- Testimonials are example quotes
- Stats ("100+ projects") are approximate

## Conventions
- Section labels: `.section-label` (small caps, rust color)
- Headings: Playfair Display, use `<em>` for italic/rust accent words
- Buttons: `.btn-primary` (dark fill) and `.btn-secondary` (outline)
- Cards/containers: 1px solid `var(--border)` with `var(--warm-white)` bg
- All links between pages use relative paths (`services.html`, not `/services.html`)

## When Making Changes
- Keep the Americana craft aesthetic — no modern/techy UI patterns
- Maintain the warm color palette — avoid cool tones, blues, purples
- Both audiences (car guys + wedding clients) should feel at home on every page
- Typography hierarchy matters — Playfair for impact, Libre Baskerville for reading, DM Sans for UI
- If extracting shared CSS, put it in `public/styles.css` and link from all pages
- Test mobile layout — hamburger nav, single-column stacking
