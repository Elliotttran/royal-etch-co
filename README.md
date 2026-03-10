# Petaluma Glass Works

Custom glass etching business website. Static site, 4 pages, designed for Netlify deployment.

## Pages
- `index.html` — Homepage
- `services.html` — Services & pricing
- `about.html` — About, story, testimonials
- `quote.html` — Quote request form

## Stack
Pure HTML/CSS/JS. No build tools, no framework. Google Fonts loaded via CDN.

## Local Development
Just open any `.html` file in a browser, or run a local server:

```bash
npx serve .
# or
python3 -m http.server 8000
```

## Deployment
Designed for Netlify. Just drag the folder into Netlify or connect a Git repo.

For form handling, add `netlify` attribute to the form tag or use Formspree.
