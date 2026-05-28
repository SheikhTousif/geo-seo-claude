# Client Tracking Sheet — Modern AI / AEO / GEO SEO Project

> Use this sheet to mark progress on every task and send transparent reports to clients.
> The companion CSV (`client-tracking-sheet.csv`) opens directly in **Google Sheets** or **Excel** and is the live working document. This Markdown file is a readable summary of the same structure.

---

## Sheet Columns (one row per sub-task)

| # | Column | What goes here |
|---|---|---|
| 1 | Phase | 1-17 |
| 2 | Phase Name | High-level stage (e.g. "Technical SEO Setup") |
| 3 | Work ID | `Phase.Work` (e.g. `5.3`) |
| 4 | Work Name | Mid-level group (e.g. "Performance / Core Web Vitals") |
| 5 | Sub-Work ID | `Phase.Work.SubWork` (e.g. `5.3.2`) |
| 6 | Task Description | Exact action to take |
| 7 | Deliverable to Client | Concrete artefact the client receives |
| 8 | Tools / Platforms | Software / service used |
| 9 | Est. Hours | Effort estimate |
| 10 | Timeline | Target day / week |
| 11 | Priority | High / Medium / Low |
| 12 | Status | Not Started / In Progress / Completed / Blocked / Pending Review |
| 13 | Planned Start | Date |
| 14 | Planned End | Date |
| 15 | % Complete | 0-100% |
| 16 | Assigned To | Owner |
| 17 | Client Approval | Pending / Approved / Revision Needed / N/A |
| 18 | Evidence / Proof Link | Screenshot / report / live URL |
| 19 | Remarks | Notes |

---

## Phase Summary (17 phases / ~250 sub-tasks)

| # | Phase | Focus | Approx Hours |
|---|---|---|---|
| 1 | Business Understanding & Entity Strategy | Discovery, ICP, UVP, topical authority pillars | 12-15 |
| 2 | Competitor Research | Local + semantic + AI-visible + content competitors | 12-14 |
| 3 | Keyword Research | Commercial / informational / conversational / AI / local | 12-14 |
| 4 | Website Structure Planning | IA, sitemap, URL pattern, silos, page inventory | 8-10 |
| 5 | Technical SEO Setup | SSL, CWV, schema, GA4 / GSC / GTM / call tracking | 25-30 |
| 6 | On-Page SEO Optimisation | Home, service, location, about, contact | 30-35 |
| 7 | Google Business Profile (GMB) | Setup, categories, photos, posts, Q&A, reviews | 22-26 |
| 8 | Content Strategy & Creation | Pillars, clusters, FAQs, glossary, multimedia | 45-55 |
| 9 | Local SEO & Citations | NAP, tier-1, industry, bulk, local link building | 28-35 |
| 10 | AI Search Optimisation (AEO / GEO) | Citability, llms.txt, AI crawlers, entity, E-E-A-T | 18-22 |
| 11 | Google Ads & Paid Search | Search, LSA, PMax, retargeting, CRO landing pages | 28-34 |
| 12 | Social Media & Outreach | Channels, content, engagement, influencers | Ongoing |
| 13 | Email Marketing & Lead Nurture | ESP, lead magnets, automations, newsletter | 16-20 |
| 14 | CRO & Conversion Optimisation | Heatmaps, funnel, A/B tests | Ongoing |
| 15 | Reputation & Reviews | Acquisition, response, repurposing | Ongoing |
| 16 | Analytics / Reporting / Client Comms | Looker, rank tracking, weekly / monthly / QBR | Ongoing |
| 17 | Ongoing Optimisation & Maintenance | Monthly / quarterly / annual recurring work | Recurring |

---

## What's New vs the Original Plan

The CSV adds these missing or under-developed areas from `LOCAL_BUSINESS_VISIBILITY_PROJECT_PLAN.md`:

1. **Phase 12 — Social Media & Outreach** (was only in the ATGIC strategy file, not the main plan).
2. **Phase 13 — Email Marketing & Lead Nurture** (welcome / abandon / review / win-back automations).
3. **Phase 14 — CRO & Conversion Optimisation** (heatmaps, A/B tests, form / hero experiments).
4. **Phase 15 — Reputation & Reviews** as a dedicated, ongoing track (not buried inside GMB).
5. **Phase 10 — AEO / GEO additions** beyond the original Phase 7:
   - Wikidata / Crunchbase / Wikipedia entity work
   - `sameAs` graph links
   - Editorial / fact-check / correction policy pages
   - Share-of-voice tracking on AI engines
6. **Tracking depth additions**:
   - Microsoft Clarity / Hotjar behaviour tracking
   - Local-pack grid tracking (Local Falcon / GeoGrid)
   - Offline conversion import (CRM closed-won)
   - Enhanced conversions
7. **Client transparency layer (Phase 16)**:
   - Looker Studio master dashboard
   - Weekly status email + change-log
   - Before/after screenshot proof folder
   - Quarterly business review (QBR) + Annual strategy deck

---

## Status Legend (use these exact values for filtering)

- **Not Started** — task hasn't begun
- **In Progress** — actively being worked on
- **Pending Review** — waiting for client / internal sign-off
- **Blocked** — cannot proceed (note reason in Remarks)
- **Completed** — done, evidence attached
- **N/A** — does not apply to this client

## Priority Legend

- **High** — must-do for ranking / lead generation
- **Medium** — important but not blocking
- **Low** — nice-to-have / opportunistic

## Client Approval Legend

- **Pending** — waiting for client review
- **Approved** — client signed off
- **Revision Needed** — client requested changes (note in Remarks)
- **N/A** — internal task, no client approval required

---

## How to Use

1. Open `client-tracking-sheet.csv` in Google Sheets or Excel.
2. Freeze the top row and add filters.
3. Fill **Planned Start / Planned End / Assigned To** at kickoff.
4. Update **Status** and **% Complete** as you work.
5. For every completed sub-task, drop a link in **Evidence / Proof Link** (screenshot, GSC link, live URL, Loom, etc.).
6. Once a week, filter by Status = "Completed (this week)" and send the client a digest from Phase 16 → 16.2.1.
7. Once a month, generate the Looker Studio report (16.1.1) and a QBR deck quarterly (16.2.3).
