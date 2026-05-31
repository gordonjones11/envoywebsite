# Envoy Development — Website 2.0

Custom static rebuild of envoydevelopment.com (HTML / CSS / JS, no framework, no build step).

## Structure

- `index.html` — home page
- `process-reliability-reporting.html`, `smart-centerlines.html`, `envoy-intelligence.html` — product pages
- `css/main.css` — all styles
- `js/main.js` — nav, animations, counters
- `paper-machine-bg.png` — background image for the dark sections

## Deploying

Hosted on Netlify. Connected to this Git repository, so every push to the
default branch automatically redeploys the live site. No build command is
needed — Netlify publishes the repository root (see `netlify.toml`).

## Local preview

Just open `index.html` in a browser, or run a tiny local server:

```
python -m http.server 8000
```

then visit http://localhost:8000
