# Envoy — Core Context File

## Instructions for the Assistant
Use this document as the authoritative source when answering any Envoy-related
question or producing any Envoy-related content (website copy, decks, emails,
proposals). If assumptions are needed, align them with Envoy's philosophy and
positioning described here. When this file conflicts with older notes, this file
wins. Last updated May 2026.

---

## 1. What Envoy Is

Envoy provides data analytics, optimization, reliability, and AI advisory
services for continuous-process industrial facilities, starting with pulp & paper.
Envoy is delivered as a **service backed by a platform** — not as software a mill
has to staff and maintain on its own.

The unifying idea is a **mill profit intelligence layer**: every report and every
analysis translates raw process data into the language the mill actually runs on —
$/ton, tons/day, energy and chemical intensity, quality risk, downtime cost, and
working-capital impact. The strongest one-line framing:

> **"Every process area gets its own operating-economic model — and every model
> rolls up to mill profit per ton."**

Envoy combines:
- Deep process engineering expertise (engineers stay engaged after go-live)
- Modern cloud data platform (shared across every service)
- Pragmatic AI and statistical methods
- Grounded, physics-based rules and models, scoped to the real equipment on the line

Envoy does **NOT** sell generic AI dashboards or black-box models, and does not
leave behind tools nobody maintains.

### Company snapshot (from May 2026 materials)
- Founded 2003
- ~37 employees — process engineers and data scientists
- Supports ~505 mill processes
- ~94% customer renewal rate
- Platform processes high-frequency time-series data, ~3,000 tags per process
  area, on the order of hundreds of thousands of "books" per day

*(Confirm/refresh these figures before using externally.)*

---

## 2. The Four Questions Envoy Answers

Envoy's services map to a progression of questions a mill asks, moving from
reliability to optimization to intelligence:

1. **What's going wrong, and why?** → *Envoy Process Reliability Reporting*
2. **What could go wrong, and why?** → *Envoy Process Reliability Reporting*
3. **What are my optimal running conditions?** → *Envoy Smart Centerlines*
4. **What are my next-best actions to take?** → *Envoy Intelligence*

The ROI ladder is **Reliability → Optimization → Intelligence.** Even modest gains
are large in a mill: one hour of avoided recovery-boiler downtime or a 1% efficiency
improvement is worth six or seven figures annually on most process islands.

---

## 3. Core Services

Envoy runs three service lines on one shared platform, layered across all major
mill process areas (paper machines, tissue forming, pulp drying, OCC & recycle
prep, digesting & cooking, bleaching & washing, recovery boilers, power & bark
boilers, evaporation & liquor concentration, lime kiln & recausticizing, utilities
& wastewater).

### 3.1 Envoy Process Reliability Reporting (EPRR)
*Answers: what's wrong & why, and what could go wrong & why.*

- **Every tag, every day.** Envoy tools scan every tag daily; an Envoy engineer
  sends only the **3–8 actionable insights** that matter — delivered before 7am.
- Report types: Daily reports, Startup reports, Shift reports (KPIs), and
  **Comprehensive reports** (minimum 12/year) for long-term analyses — time-period
  comparisons, correlation studies, and root-cause investigations that pinpoint the
  exact date a change occurred and the variables that correlate with it.
- **Control Loop Health (new):** ~25 control-loop analytic tools (mean absolute
  error, backlash, stiction, oscillation wavelength/amplitude, output reversals and
  travel, mode/SP changes, % in auto/manual/cascade, PV/OP averages). Loops are
  prioritized **Red / Yellow / Green** — Red = not controlling to setpoint on an
  important variable; Yellow = non-critical, over-tuned, or near valve-travel limits;
  Green = controlling within parameters.
- Delivered **as a service** — Envoy engineers do the analysis, not just the software.
- Typical ROI: break-even at roughly ~2 hours of avoided recovery-boiler downtime
  per year; a typical site sees one to two moderate events caught per year worth
  tens to hundreds of thousands of dollars.

### 3.2 Envoy Smart Centerlines
*Answers: what are my optimal running conditions?*

- Engineer-approved **optimal targets and limits** that define a safe operating
  envelope, adjusted by grade / recipe / speed / mode.
- Built to be **maintained over time, not abandoned** — tracks centerline drift and
  widening/narrowing.
- The scale of the problem is why this matters: a paper machine with 200+ controllers
  has more possible operating states than there are atoms in the universe — no human
  can compute the ideal by hand.
- Tooling includes a **Centerline Architect** (global and tag-level filters), a
  **Setpoint Optimizer** (set constraints → run optimization → generate optimized
  setpoints), and **Process Model Visualization** using T² (distance from centerline /
  early warning of drift) and Q (size of the "unexplained" residual — model break or
  sensor drift).
- Quantified value examples: targeting first-quartile basis weight can cut fiber use
  ~1.6% (≈$2.0MM/yr on a typical machine, payback in days); a 1-point gain in recovery
  reduction efficiency is worth >$1MM/yr.
- Implementation: ~4–7 weeks for a new install, ~1–4 weeks for an existing EPRR mill.

### 3.3 Envoy Intelligence
*Answers: what are my next-best actions? Real-time, context-aware operational advice;
training & knowledge transfer; Tier-2 alarm & event management.*

Envoy Intelligence is the emerging flagship and the part of the story the website
most needs to capture. The core thesis:

> **"Generic AI gives PhD answers… to a machine you don't have. AI isn't the hard
> part — relevant AI is."** So Envoy built it the opposite way: **context first,
> AI second.** Envoy Intelligence is **AI that understands this machine, in this mill.**

It is delivered as **two products on one shared context layer**, with the context
layer (the six tools below) as the engine underneath both:

#### (a) Operational Intelligence — for operators, always-on
A real-time **deviation board** for the control room: what's off, why, and what to
do next. A continuous **~15-minute scan loop**: scan every tag → detect deviations
vs. the centerline / safe envelope → **group related deviations into one operational
event** (e.g. 20 alarms become 1 event) → surface ranked likely causes + next-best
actions, with citations back to the mill's SOP/TCC.
- **Advisor-first:** supports operator judgment, does not replace it. No closed-loop
  control.
- **Tier-2 alarm & event management:** the DCS keeps Tier-1 "react-now" alarms;
  Tier-2 alerts route to Envoy Intelligence, which groups them into events to cut
  noise and add context.
- **Envoy Advisor** explains equipment purpose, operation, and system interactions —
  ask-anything about the machine, speeding onboarding for operators and early-career
  engineers, and capturing shift knowledge instead of losing it.

#### (b) Engineering Intelligence — for engineers, on-demand
**Runbooks**: structured, repeatable analyses an engineer launches with a click —
root-cause, breaks investigations, optimization studies, and special reports. A
runbook bundles an **analytical method** (e.g. change-point / CUSUM, correlation)
+ the **right tags** (scoped by Tag Forge) + the **equipment reality** (Knowledge
Graph) → an output report with findings, the exact date things changed, the
correlated variables, and the dollar impact.
- Organized by process area — there's a runbook for every corner of the mill (fiber →
  paper machine → finishing → utilities).
- Signature analyses most likely to resonate with mill leadership: bleach plant
  cost-to-brightness optimizer; lime kiln residual-carbonate scenario model; press
  dryness → dryer steam value calculator; lost-profit waterfall by process area;
  fiber yield & furnish economics; grade profitability & order sequencing; recovery
  island constraint analyzer; wastewater upset prediction; broke & off-grade
  economics; energy balance & steam/power optimizer.
- Every analysis rolls up to **mill profit per ton** — the lost-profit waterfall is
  the executive view of where margin went.

#### The 6 Context Tools (the engine under both products)
What makes the AI specific to one machine in one mill — configure the context once
and both products get sharper:

1. **Tag Forge** — cleans and standardizes tag naming/metadata; categorizes tags into
   process areas and equipment groups; enables "bounded context" so the AI searches
   only the relevant tag universe.
2. **Smart Centerlines** — define what "good" looks like right now; make deviations
   measurable (how far, how fast, how risky). This is the reference the 15-minute scan
   checks against.
3. **Knowledge Graph** — models what equipment exists and how it connects; prevents
   irrelevant advice (no IR dryer → no IR-dryer tuning advice); supports
   upstream/downstream root-cause narrowing.
4. **Knowledge Base** — grounds the AI in the mill's own SOPs/TCCs (not generic
   advice); finds the right procedure by symptom/task; cites the source for trust and
   cross-shift consistency.
5. **Rule Studio** — suppresses tags when equipment isn't running; prevents "false
   problems"; defines what normal looks like by state (startup, shutdown, grade change,
   bypass modes, offline equipment).
6. **Skills Library** — structured, repeatable troubleshooting workflows grounded in
   Tag Forge scope, equipment-graph constraints, and state-based logic. The Skills
   Library is also the mechanism behind the Engineering Intelligence runbooks.

---

## 4. What Makes Envoy Different
- **Context first, AI second** — relevance beats raw model horsepower.
- Engineers stay engaged after go-live; this is a service, not shelfware.
- Focus on **maintainability**, not one-time models.
- Deep understanding of how mills actually operate; advice is constrained by the real
  equipment and the mill's own procedures.
- Avoids IT-heavy, over-engineered solutions; plugs into systems the mill already has
  (DCS/historian, QCS, LIMS, CMMS, ERP).
- Everything is expressed in money — $/ton and lost-profit, not just charts.

---

## 5. Ideal Customers
- Mills with strong operations but limited analytics or engineer bandwidth.
- Plants frustrated with one-off projects, consultants who leave, and tools nobody
  maintains.
- Sites that want operator- and engineer-facing intelligence grounded in their own
  machine reality, not a generic "AI for manufacturing" platform.

---

## 6. Competitive Landscape (high level)
Envoy often competes with:
- In-house engineering + Excel + other complex analytics tools
- Large automation vendors' analytics modules
- Generic "AI for manufacturing" platforms

Envoy wins when:
- Trust and adoption matter
- Context matters more than algorithms
- The customer wants results, not software shelfware
- The customer lacks the engineering bandwidth to build and maintain their own

---

## 7. Deployment & Security (high level)
- **Cloud-to-cloud (preferred)** or **mill-to-cloud** data integration.
- **Envoy Edge** (with Azure SHIR) deploys on the client's VPN-protected VM:
  outbound-only communication, encrypted data flow, no exposure to internal systems,
  full client governance over the execution environment.
- Hosted on a private Azure Kubernetes Service cluster with a single hardened entry
  point; Microsoft Entra ID SSO; role-based access control and least privilege; data
  encrypted in transit (TLS) and at rest; secrets in Azure Key Vault; per-client data
  isolation, private networking/endpoints, and comprehensive logging/monitoring.
- Designed to meet enterprise corporate-IT and security requirements.

---

## 8. Pricing Shape (illustrative — confirm before quoting)
Example annual package for one paper machine: base software license (~$7,000/mill/yr),
per-process implementation/configuration, Paper Machine EPRR (~$1,789/mo), and Paper
Machine Smart Centerlines (~$1,789/mo) → on the order of ~$50,000 first year.
Always label pricing as an example; confirm Envoy Intelligence packaging separately.

---

## 9. Language & Positioning Rules
- Avoid hype words like "revolutionary" or "disruptive."
- Prefer practical language: reliability, variability, context, maintainability,
  next-best action, mill profit per ton.
- **AI is a tool, not the product.** Lead with the operator/engineer outcome, then
  reveal the context engine that makes it work.
- Lead with outcomes (what's wrong, what's optimal, what to do); reveal the plumbing
  (the 6 context tools) second.
- Advisory only — Envoy supports human judgment and does not take closed-loop control.
