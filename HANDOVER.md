# Envoy Development Website 2.0 — Handover Document

**Last updated:** May 31, 2026

---

## Project Summary

We are rebuilding **envoydevelopment.com** as a fully custom HTML/CSS/JS static site, moving off ShowIt (the old platform). The new site is more detailed and content-rich than the current one, with dedicated solution pages and (planned) a Resources section and an "Intelligent Factory" thought-leadership page.

The site is **live** and deploying automatically (see Deployment below).

---

## Current Working Location (IMPORTANT — read first)

The live, current copy of the site is the cloned Git repo at:

`C:\Apps\EnvoyWebsite\envoywebsite`

**Edit there going forward.** The original `C:\Users\gordo\OneDrive\GJ Work Documents\Claude Apps\Website 2.0` folder was the first working copy, but its `.git` is broken and Git cannot run inside OneDrive (file locks). Do **not** run Git in the OneDrive folder. As of this update, the repo folder holds the most current pages.

**Reference plan doc:** `Envoy_Website_Redesign_Plan.md` (full content/architecture plan).

---

## Deployment

- **GitHub repo:** `gordonjones11/envoywebsite` (private)
- **Host:** Netlify — auto-deploys on every push to `main`
- **Live URL:** https://funny-kitten-305a48.netlify.app/ (could be renamed to e.g. `envoy-preview.netlify.app` via Netlify → Site configuration → Site information)
- **Config:** `netlify.toml` — no build command, publish repository root
- **Workflow:** edit files in the repo folder → GitHub Desktop → **Commit to main** → **Push origin** → Netlify redeploys (~1 min). Hard-refresh (Ctrl+Shift+R) to bust favicon/image caching.

---

## Files Built So Far

| File | Status | Notes |
|------|--------|-------|
| `index.html` | ✅ Complete | Home/landing page, all sections |
| `css/main.css` | ✅ Complete | Shared stylesheet for all pages (~660 lines) |
| `js/main.js` | ✅ Complete | Nav scroll, mobile menu, stat counters, fade-in observer |
| `process-reliability-reporting.html` | ✅ Complete | Solution page — Tier 1 |
| `smart-centerlines.html` | ✅ Complete | Solution page — Tier 2 |
| `envoy-intelligence.html` | ✅ Complete | Solution page — Tier 3 |
| `Envoy_Website_Redesign_Plan.md` | ✅ Reference | Full content/architecture plan |

### Still to build (referenced in nav but not yet created — links currently dead):
- `solutions.html` — Solutions Hub (overview/comparison of all 3 tiers)
- `intelligent-factory.html` — Thought leadership page
- `resources.html` + `resources/` — articles, whitepapers, anonymized case studies, glossary
- `about.html` — Enhanced About page
- `contact.html` — Contact / Demo Request page

---

## Site Architecture

```
Home
├── Solutions ▾ (dropdown)
│   ├── Solutions Hub (solutions.html)               [not built]
│   ├── Process Reliability Reporting  ✅
│   ├── Envoy Smart Centerlines        ✅
│   └── Envoy Intelligence             ✅
├── The Intelligent Factory (intelligent-factory.html) [not built]
├── Resources (resources.html)                         [not built]
├── About (about.html)                                 [not built]
└── Contact / Request a Demo (contact.html)            [not built]
```

---

## Brand & Design

### Colors (CSS variables in `:root`, `css/main.css`)
- Primary dark green: `--green-800: #1a5c38`
- Medium green: `--green-600: #238a5e`
- Deep brand green (dark section wash, favicon): `--dark-green: #0d3d22` (logo sampled at ~#266b47)
- Light green bg: `--green-50: #f0faf5`
- Font: Inter (Google Fonts)

### Favicons (from user-supplied pack — replaced earlier auto-generated versions)
`favicon.ico`, `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`, `android-chrome-192x192.png`, `android-chrome-512x512.png`, `site.webmanifest`. Linked in `<head>` of all four pages. (Note: the live ShowIt site has no usable favicon to lift — these come from the pack Gordon supplied.)

### Landing-page dark-section backgrounds (equipment photos under a green wash)
- Pain Points → `paper-machine-bg.png`
- Data Pipeline → `digester-bg.png`
- Stats → `yankee-dryer-bg.png`
- CTA → `recovery-boiler-bg.png`
- `lime-kiln-bg.png` is available but **not yet placed**.

### Product-page hero images (transparent PNGs, so the swoosh shows through; drop below text on mobile ≤768px)
- Process Reliability Reporting → `eprr-hero.png`
- Smart Centerlines → `sc-hero.png` (centered, not right-aligned, on that page)
- Envoy Intelligence → `ei-hero.png`

### Section breaks ("ledge" effect) — landing page
Alternating light/dark bands separated by **45° angled "ledge" dividers**. Each dark band is clipped into an octagon: top ledge ~25% across, bottom ledge ~75% across, both rising left→right so slopes stay parallel. Controlled by `--slant`, `--ledge-top`, `--ledge-bot` in `:root`. Dark sections use the deep-green wash graded lighter→darker left to right.

### Hero (landing page)
Low background "swoosh"; "Where Paper Science Meets" in thinner weight 500; bold gradient "Data Science" inside an outlined box with a small period tucked inside; generous bottom padding before the dark band.

### Solution-page eyebrow labels
Format: `Tier 1 — Foundation:&nbsp;&nbsp;&nbsp;Envoy Process Reliability Reporting` (three non-breaking spaces after the colon — plain spaces collapse in HTML). Same pattern for Tier 2 / Smart Centerlines and Tier 3 / Envoy Intelligence.

### Headlines of note
- Process Reliability Reporting H1: "Process issues **flagged** before your shift begins." (We *flag/surface* issues, we do not *resolve* them — keep wording accurate.)

---

## Critical Content Rules (Gordon's Preferences)

### AI Language Policy — IMPORTANT
- **Tier 1 (Process Reliability Reporting):** NO AI references. Statistics, rules-based, deterministic, engineer-reviewed. Can say "code and formulas inform the models" but NOT "AI."
- **Tier 2 (Envoy Smart Centerlines):** NO AI references. "Multi-variable statistical modeling," "statistically derived," "deterministic outputs."
- **Tier 3 (Envoy Intelligence):** AI is fine and expected — this is the transformation tier.
- **Reason:** Some customers are old-school and anti-AI; they must not feel excluded by Tier 1/2 messaging.

### Tone
- Warm and accessible for mill superintendents and ops managers.
- Technical depth welcome but explained in plain language.
- "Engineers who've stood where you stand" — human expertise is the key differentiator.

### Stats (current correct values)
- **500+** mill processes monitored
- **94%** client renewal rate
- **500+** years of combined mill experience
- **20+** in-house engineers
- Founded **2003**

### Hero subtext (exact copy to preserve)
> "Envoy transforms real-time operational data into actionable insights that drive reliability, efficiency, and profitability for pulp and paper mills."

### Tier 1 description
Should say **"Envoy engineers analyzing your data overnight"** — not "your engineering team."

---

## Inline SVG Diagrams (built, no external images needed)

| Diagram | Location | Description |
|---------|----------|-------------|
| Data Pipeline Flow | `index.html` | 3,000 tags → models → ~100 exceptions → engineers → 3–8 insights |
| Delivery Workflow Timeline | `process-reliability-reporting.html` | Nightly pipeline steps with timestamps |
| Operating Window Chart | `smart-centerlines.html` | Time-series with grade-change event and optimal-window shading |
| System Architecture | `envoy-intelligence.html` | Mill data → ML/Rules/KB → Envoy Advisor → Mill Team |

---

## CSS / JS Architecture Notes

- `css/main.css` is the single shared stylesheet; solution-page styles live in a labeled section near the bottom.
- Each HTML file has only a small `<style>` block for the fade-in utility.
- `js/main.js`: sticky nav shadow, mobile menu toggle, stat counter animation, smooth scroll, fade-in-on-scroll observer.
- All pages share the same nav + footer HTML (copied manually — no templating).

---

## Content Plan for Remaining Pages

### solutions.html (Solutions Hub)
Tier-ladder diagram (3 levels), mill coverage map (all process areas), feature comparison table, links to the 3 solution pages.

### intelligent-factory.html
Vision ("the paper mill of the future is being built today"), maturity roadmap (Reactive → Monitored → Optimized → Intelligent), why-now (aging workforce, cost pressure, ML advances), Envoy's role.

### resources.html + ~10 articles
1. From 3,000 Tags to 8 Insights: Inside the Envoy Data Pipeline
2. Understanding CUSUM Control Charts in Paper Machine Monitoring
3. What Are Smart Centerlines — And Why Do They Change Everything?
4. Grade Change Runnability: How Centerlines Cut Transition Time
5. Physics-Based Machine Learning: Why First Principles Beat Pure Data
6. The Intelligent Mill: A Roadmap for Pulp and Paper's Digital Future
7. Predicting Paper Machine Breaks Before They Happen
8. Control Loop Health: The Hidden Driver of Process Stability
9. Why Morning Reports Change How Mills Operate
10. Root Cause Analysis at the Mill: From Event to Action

All case studies are **anonymized** (no named mills — customers don't want "dirty laundry" publicized).

### New hero/background image prompt style (if more art is needed)
> "Wide-angle interior of a [equipment] in a pulp/paper mill, dramatic industrial lighting, steam rising, cinematic photorealistic style, high contrast, desaturated tones, no people, no text. Suitable as a dark website background." (Generate wide/16:9; transparent PNG for hero figures.)

---

## Known Quirks / Gotchas

- **Stale bash cache:** the sandbox shell sometimes shows an outdated view of files (truncated tails, wrong line/brace counts). The Read/Write/Edit file tools are the source of truth — trust them over bash for file contents.
- **`css/main.css` truncation:** a save glitch has cut the file off mid-line more than once, near the "Intelligent Factory Teaser" / "Product Page Responsive" section at the end, dropping the trailing rules. If end-of-file styles (product-page mobile rules, if-teaser) go missing, check and repair there first. Always verify brace balance after big edits.
- **Leftover clutter in repo folder** (unused; safe to delete or "Ignore file" in GitHub Desktop): `Hero Image - EPRR.png`, `Hero Image - SC.png`, `Hero Image - EI.png`, `envoy-development-favicon-pack.zip`, `_favprev.png`, old `favicon-16.png` / `favicon-32.png`, and possibly `Paper Machine Background Picture.png`.

---

## Open Items / Possible Next Steps

1. Build the remaining pages (solutions hub, intelligent factory, resources, about, contact) — nav links to them are currently dead.
2. Place or drop the unused `lime-kiln-bg.png`.
3. Rename the Netlify URL to something cleaner.
4. Compress hero/background PNGs (some ~1.7–2.7 MB) for faster loads.
5. Re-check the GitHub repo public/private setting if sharing changes (currently private).

---

## How to Continue

Start the next session by sharing this file and the plan doc, e.g.:
> "Here's the handover doc. Let's continue the Envoy website — start with [solutions hub / intelligent factory / resources / etc.]."

Edit in `C:\Apps\EnvoyWebsite\envoywebsite`, then Commit + Push in GitHub Desktop to deploy.
