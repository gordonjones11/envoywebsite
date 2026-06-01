# Envoy Website Redesign Plan
*Draft v1 — May 2026*

---

## The Goal

The current site is clean and well-branded but undersells what Envoy actually does. Someone landing on it understands "daily reports for mills" but doesn't grasp the sophistication of the analytics, the depth of the three-tier product suite, or Envoy's position as the leading intelligent-factory partner for pulp and paper. The redesign fixes that by adding depth, technical credibility, and a resource library that establishes Envoy as a thought leader — not just a service vendor.

**Keep:** Logo, brand colors, photography style, tagline, overall tone  
**Change:** Site architecture, content depth, product storytelling, add Resources + Intelligent Factory sections

---

## Site Architecture

### Navigation (revised)
```
Home  |  Solutions ▾  |  The Intelligent Factory  |  Resources  |  About  |  Request a Demo
```

The Solutions dropdown exposes the three product pages directly — removing the extra click through a hub.

---

## Page-by-Page Plan

### 1. Home Page (Revamp)

**Goal:** Compel a mill superintendent or VP Operations to want to learn more. Establish Envoy as the serious, engineering-led analytics partner for pulp and paper.

**Sections:**

**Hero**  
Keep the swoosh background and brand feel. Update headline to lean harder into the outcome, not the method.  
*Current:* "Where Paper Science Meets Data Science"  
*Option:* "The Intelligent Mill Starts Here" (position the full journey) or keep existing tagline but add a punchy subhead about all three tiers.

**The Problem (enhanced)**  
Keep the four pain points (downtime, instability, cost, lean teams) but give each more texture — one concrete sentence describing what this actually feels like on a mill floor.

**How Envoy Solves It — Product Suite at a Glance**  
A new three-column section showing all three tiers side by side, with a brief description and a "Learn More" link for each. This replaces the current vague "actionable insights" section and immediately shows the product depth.

**The Data Pipeline (new diagram)**  
A visual showing: 3,000 tags → Statistical/Process/Rules models → 100 exceptions → Envoy Engineers → Daily Report. This is one of the most compelling parts of the Envoy story and it's invisible on the current site.

**Why Envoy (keep, light enhancement)**  
Current section is good — keep the five bullets, maybe add one more point about the intelligence tier.

**Stats Bar**  
434 process areas | 95% renewal | 500+ years experience | 20 engineers | Founded 2003

**Testimonial Carousel**  
Add 2–3 quotes (can be anonymized by role/region). The current one quote from "US Mill Superintendent" is good — expand it.

**CTA**  
Keep "Request a Demo" as primary CTA throughout.

---

### 2. Solutions Hub (Revamp)

**Goal:** Orient visitors to the three tiers and help them self-select the right starting point.

**Sections:**

**Hero**  
"A solution for every stage of the journey to an intelligent mill."

**Tier Ladder Diagram (new)**  
A vertical progression diagram showing:  
- Tier 1: Envoy Process Reliability Reporting (Foundation)  
- Tier 2: Envoy Smart Centerlines (Optimization)  
- Tier 3: Envoy Intelligence (Transformation)  
Each tier builds on the last. The diagram makes the natural upgrade path obvious.

**Mill Coverage Map (new)**  
A visual listing all process areas covered (Paper Machines, Tissue, Digesters, Bleach Plant, Recovery Boilers, Power Boilers, Evaporators, Lime Kiln/Recaust, Wastewater, OCC/Recycle) — showing breadth.

**Feature Comparison Table (new)**  
Side-by-side comparison of what's included in each tier. Prospects can scan this to understand exactly what they'd be getting.

**Links to Three Product Pages**

---

### 3. Envoy Process Reliability Reporting (New Dedicated Page)

**Goal:** Show the depth and rigor behind what looks like "just a daily email." This is the hardest product to sell because it sounds simple — the page needs to communicate the engineering sophistication underneath.

**Sections:**

**Hero**  
"Stay ahead of your next outage — before your shift starts."

**What It Is**  
3–4 paragraphs explaining the service: daily email before 7 AM, 3–8 engineer-reviewed insights, based on overnight analysis of your mill's process data. Emphasis on the "no dashboards, no extra work" angle.

**The Daily Report Deep Dive**  
Explain what's in a daily report: what kinds of issues are surfaced (energy anomalies, process deviations, control loop degradation, pre-break signatures, off-quality signals). Use one or two blurred/example report images.

**Comprehensive Reports**  
Explain the four comprehensive report types:
- **Correlation Studies** — finding hidden relationships between variables
- **Root Cause Analysis** — tracing an event backward to its origin
- **Time Period Comparisons** — comparing mill performance before/after a change
- **Control Loop Health** — assessing whether your PID loops are actually doing their job

**Analytics Methods (new section — builds credibility)**  
Brief explanation of the statistical tools used:
- **CUSUM (Cumulative Sum) Charts** — detecting subtle shifts in process mean that standard SPC misses
- **Time Series Analysis** — identifying trends and seasonality in process data
- **Quartile Analysis** — understanding the distribution of performance across operating conditions
- These can be shown with the existing blurred chart images

**The Delivery Workflow Diagram (new)**  
A diagram showing the nightly pipeline: Data collection → Model processing → Exception flagging → Engineer review → Report generation → 7 AM delivery

**What Clients Say**  
Testimonials/quotes from mill leadership.

**CTA + Fast Start**  
"Most clients are live within a week." Request a Demo.

---

### 4. Envoy Smart Centerlines (New Dedicated Page)

**Goal:** Explain what a centerline is, why it matters, and why Envoy's approach (statistical + AI-informed, not just averages) is different.

**Sections:**

**Hero**  
"Run every grade at its best — every time."

**What Is a Centerline?**  
Plain-language explanation: a centerline defines the ideal target value (or range) for each key process variable, specific to a grade and production rate. When variables drift outside their optimal windows, runnability suffers. Centerlines give operators a clear target to return to.

**The Problem Without Centerlines**  
Grade changes are chaotic. Operators rely on memory or tribal knowledge. New operators don't know where things should be. Senior expertise walks out the door when people retire.

**How Envoy Smart Centerlines Work**  
- Statistical analysis of your historical data to identify the operating conditions that correlate with best performance
- AI-informed optimization layered on top
- Grade- and rate-specific targets, not one-size-fits-all
- Live tracking: your current variables shown against their optimal windows

**The Centerline Concept Diagram (new)**  
A time-series chart showing a process variable over time, with an optimal operating window shaded in green, showing excursions out of window and their correlation with quality/runnability events.

**Benefits**  
- Reduced grade change time
- Faster startup recovery after breaks
- Consistent quality across shifts
- Capture and preserve senior engineer knowledge

**Includes Everything in Process Reliability Reporting**

**CTA**

---

### 5. Envoy Intelligence (New Dedicated Page)

**Goal:** This is the flagship/vision product. The page should be aspirational — positioning Envoy as the partner for the intelligent mill of the future — while staying grounded in what it actually delivers today.

**Sections:**

**Hero**  
"Your best senior engineer — always on call, with instant recall of decades of experience."  
(Borrow the existing copy — it's genuinely compelling.)

**What Envoy Intelligence Is**  
Envoy Intelligence combines real-time process monitoring, physics-based machine learning models, and engineer-vetted response playbooks into a single AI-orchestrated system. It doesn't just alert you to problems — it tells you what's causing them and what to do about it.

**The Envoy Advisor**  
The real-time alert interface: how it works, what triggers an alert, how alerts are delivered, what information accompanies each alert (context, likely cause, recommended action).

**Physics-Based Machine Learning**  
This deserves a real explanation:
- Unlike pure data-driven ML, physics-based (or hybrid) models embed known process relationships as constraints
- This means predictions hold up even in operating regimes with sparse historical data
- Example: a physics-informed model "knows" that you can't increase steam pressure beyond the boiler's design limits — it doesn't have to learn this from data
- Results in more reliable predictions and fewer false positives than black-box approaches

**Failure-Cause-Fix (new section)**  
The knowledge base of real operational events: when a specific failure pattern is detected, the system surfaces the most likely causes and the engineer-recommended corrective actions — drawn from Envoy's 20+ years of mill experience and 500+ years of engineer knowledge.

**Predictive Insight**  
How far in advance can issues be detected? What kinds of failures are most predictable? (Without overpromising — stay specific and honest.)

**Architecture Diagram (new)**  
A system architecture diagram showing: Real-time data feed → Physics-based ML models + Rules Engine + Knowledge Base → Envoy Advisor → Mill operator. With engineer oversight shown as a parallel track.

**The Vision: The Intelligent Mill**  
Short section linking to The Intelligent Factory page.

**Includes Everything in Smart Centerlines**

**CTA**

---

### 6. The Intelligent Factory (New Page — Thought Leadership)

**Goal:** Position Envoy as the strategic partner for where pulp and paper is going, not just where it is. This page is about industry leadership, not sales. It should feel more editorial than product-focused.

**Sections:**

**Hero**  
"The paper mill of the future isn't a concept. It's being built today."

**What Is the Intelligent Factory?**  
Definition: a mill that uses real-time data, machine learning, and engineer expertise to operate continuously at or near optimal conditions — anticipating problems rather than reacting to them, capturing institutional knowledge rather than losing it, and improving over time rather than staying static.

**The Maturity Roadmap Diagram**  
A progression diagram with four stages:  
1. **Reactive** — Problems identified after they occur. Reliance on experience and intuition.  
2. **Monitored** — Daily reports flag early signals. Process deviations caught before they cascade. (Envoy Tier 1)  
3. **Optimized** — Operating variables consistently tracked against ideal targets. Grade changes predictable and fast. (Envoy Tier 2)  
4. **Intelligent** — Predictive models anticipate failures. AI-orchestrated responses reduce operator burden. Institutional knowledge codified and always available. (Envoy Tier 3)

**Why Now**  
The forces driving urgency: aging workforce and retirement of senior engineers, increasing cost pressure, industry consolidation, advances in ML that finally work reliably in process industries, and 20+ years of Envoy's accumulated mill data and knowledge.

**Envoy's Role**  
How Envoy bridges the gap: human expertise + machine intelligence. Why this combination is better than pure automation or pure human judgment.

**Industry Perspective**  
2–3 short editorial points on where the industry is heading (trends in predictive maintenance, digital twins, sustainability requirements, etc.).

**CTA: Start the Journey**  
Link to Solutions Hub and Request a Demo.

---

### 7. Resources (New Section)

**Goal:** Build organic search traffic, establish thought leadership, give prospects reasons to return to the site, and provide sales support materials.

#### Articles & Insights (10 articles to build)

| # | Title | Product Tie-in | Audience |
|---|-------|---------------|----------|
| 1 | From 3,000 Tags to 8 Insights: Inside the Envoy Data Pipeline | Process Reporting | Technical |
| 2 | Understanding CUSUM Control Charts in Paper Machine Monitoring | Process Reporting | Technical |
| 3 | What Are Smart Centerlines — And Why Do They Change Everything? | Centerlines | General |
| 4 | Grade Change Runnability: How Centerlines Cut Transition Time | Centerlines | Operations |
| 5 | Physics-Based Machine Learning: Why First Principles Beat Pure Data in Process Industries | Intelligence | Technical |
| 6 | The Intelligent Mill: A Roadmap for Pulp and Paper's Digital Future | Intelligence / Factory | Strategic |
| 7 | Predicting Paper Machine Breaks Before They Happen | Intelligence | Operations |
| 8 | Control Loop Health: The Hidden Driver of Process Stability | Process Reporting | Technical |
| 9 | Why Morning Reports Change How Mills Operate | Process Reporting | General |
| 10 | Root Cause Analysis at the Mill: From Event to Action | Process Reporting | Operations |

#### Technical Whitepapers (2–3 longer documents)
- "The Case for Physics-Informed ML in Pulp and Paper"
- "Centerline Strategy for Paper Machine Runnability"
- "Building the Intelligent Mill: A Practical Framework"

#### Case Studies
- 2–3 anonymized case studies (e.g., "Tissue Mill Reduces Breaks by X% in 90 Days")

#### Mill-Type Coverage Guide
- A page or download showing which process areas Envoy covers and what kinds of issues each monitoring program catches

#### Glossary
- Definitions of key terms: CUSUM, centerline, process tag, runnability, control loop, etc. Good for SEO and for educating prospects.

---

## Diagrams to Build (Claude Can Create These)

All of these can be built as SVG diagrams — no image generation needed.

| Diagram | Page | What It Shows |
|---------|------|---------------|
| Data Pipeline Flow | Home + Process Reporting | 3,000 tags → models → 100 exceptions → engineers → report |
| Product Tier Ladder | Solutions Hub | Three tiers stacked vertically, each building on the last |
| Daily Report Timeline | Process Reporting | Nightly data → 7 AM delivery workflow |
| CUSUM Concept Chart | Process Reporting / Resources | How CUSUM detects shifts that SPC misses |
| Centerline Operating Window | Smart Centerlines | Time series with optimal range shaded, excursions shown |
| Envoy Intelligence Architecture | Envoy Intelligence | Real-time data → ML models → Advisor → Operator |
| Intelligent Factory Maturity | Intelligent Factory | Four-stage progression: Reactive → Monitored → Optimized → Intelligent |
| Mill Coverage Map | Solutions Hub | All process areas shown as a connected mill diagram |

---

## Hero Image Prompts (for ChatGPT Image Generation)

These are prompts to generate hero/section images using ChatGPT's image tool. Style note for all: photorealistic, cinematic lighting, industrial but clean, blue-green color palette echoing Envoy brand colors, no people's faces shown or blurred.

**Home Hero:**  
"Wide-angle interior of a modern paper machine hall. Dramatic overhead industrial lighting. Subtle translucent data visualization overlays floating in the air — time series lines, process variable readouts. Cool blue-green color cast. Atmospheric, slightly misty from steam. No visible faces. Cinematic photography style."

**Process Reliability Reporting:**  
"A paper mill control room at dawn. Large monitors showing process trend charts and data dashboards. A single hand holding a tablet displaying a morning report. Warm light from the monitors contrasts with early morning light through industrial windows. Calm, focused atmosphere. No visible faces."

**Smart Centerlines:**  
"Abstract visualization of a paper machine process: translucent bands of soft green light representing optimal operating windows, with thin data lines flowing through them. Industrial metal surfaces in background, out of focus. Clean, precise aesthetic. Blue-green palette."

**Envoy Intelligence:**  
"Futuristic paper mill operations center. Multiple large curved screens displaying predictive analytics, alert dashboards, and 3D process models. Warm amber alert indicators contrast with cool blue interface elements. Dramatic overhead lighting. No visible faces. High-tech but believable."

**The Intelligent Factory:**  
"Aerial or wide perspective inside a massive modern paper mill. Clean, well-lit production floor. Subtle golden data streams flowing between machinery, suggesting connectivity and intelligence. Dawn or early morning light. Aspirational, forward-looking. Cinematic."

**Resources Hero:**  
"Clean, minimal overhead shot of an engineer's desk: printed charts with handwritten annotations, a laptop showing data visualizations, a coffee mug, a mill floor in the background through large windows. Warm natural light. Editorial photography style."

---

## Build Approach

### Phase 1 — Foundation (agree on architecture and content first)
1. Finalize this plan (your feedback)
2. Build the full Home page as HTML
3. Build the Solutions Hub page
4. Review and iterate on design/feel before building the rest

### Phase 2 — Product Pages
5. Envoy Process Reliability Reporting
6. Envoy Smart Centerlines
7. Envoy Intelligence
8. Build all 8 inline SVG diagrams

### Phase 3 — New Content
9. The Intelligent Factory page
10. Resources landing page + 10 articles
11. Whitepapers (as downloadable PDFs or long-form pages)

### Phase 4 — Polish
12. Consistent design pass across all pages
13. Mobile optimization
14. Image prompt generation for ChatGPT (above)
15. Final review before handing to web team for deployment to ShowIt or new platform

### Technology Note
The current site runs on ShowIt (a hosted website builder). For the rebuild, we have two options:
- **Stay on ShowIt:** Export the new content/design as a guide for a ShowIt designer to implement
- **Move to a new platform:** Build the site as standalone HTML/CSS/JS that can be deployed to any host (Netlify, Vercel, etc.) — this gives more control over the diagrams and interactive elements

Recommend discussing platform choice before Phase 1 is complete.

---

## Open Questions for Gordon

1. **Platform:** Stay on ShowIt or move to a custom build?
2. **Diagrams:** Want all 8 diagrams built inline (SVG), or some as separate static images?
3. **Resources:** Should articles be full long-form pages, or shorter ~500-word insight cards?
4. **Case Studies:** What level of detail can we share? Anonymous stats only, or named mills?
5. **Tone shift:** Current site is warm and accessible. Should the new site be more technical/authoritative for a more sophisticated buyer, or keep the same approachable tone?
6. **Images:** Do you want to generate new hero images via ChatGPT, or use the existing mill photography from ShowIt?

---

*Next step: Gordon reviews, answers open questions, then we build Phase 1.*
