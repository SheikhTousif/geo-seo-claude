# Tracking Sheet — Client Reporting Guide

This guide explains how to operate the **`client-tracking-sheet.csv`** as a single source of truth for project execution **and** weekly / monthly client reporting.

---

## 1. Set up the sheet (one-time)

1. Upload `client-tracking-sheet.csv` to Google Drive and open it with Google Sheets.
2. **File → Save as Google Sheets**.
3. **View → Freeze → 1 row**.
4. **Data → Create a filter**.
5. Apply conditional formatting on the **Status** column:
   - `Not Started` → grey
   - `In Progress` → yellow
   - `Pending Review` → blue
   - `Blocked` → red
   - `Completed` → green
6. Apply a colour scale on **% Complete** (0% red → 100% green).
7. Optional: add a Pivot Table with rows = Phase, values = AVG of % Complete → instant phase-level progress meter.

---

## 2. Fill in the planning columns at kickoff

For each row, fill:

- **Assigned To** — single owner (don't share ownership)
- **Planned Start** / **Planned End** — calendar dates
- **Priority** — already pre-set; tweak per client

Lock the rest of the columns to "in-progress edit only" so the plan doesn't drift.

---

## 3. Daily / weekly execution rhythm

### Daily (5 min per task)
- Move tasks to **In Progress** when you start.
- Drop the proof link in **Evidence / Proof Link** before marking **Completed**.

### Every Friday (15 min)
- Filter by `Planned End ≤ next Friday` → that's your next-week scope.
- Filter by `Status = Completed AND Planned End in this week` → that's your client digest.

---

## 4. Client Reporting Cadence

### Weekly status email (Phase 16 → 16.2.1)
Send a short email every Friday with three sections:
1. **Done this week** — pull rows where Status flipped to Completed in the last 7 days.
2. **In progress** — pull rows where Status = In Progress.
3. **Blocked / decisions needed** — pull rows where Status = Blocked OR Client Approval = Pending.

Template:

```
Subject: [Client Name] — Weekly SEO update — Week of {date}

DONE THIS WEEK
- 5.5.2 LocalBusiness schema implemented and validated → {proof link}
- 7.2.7 GMB description live (750 chars, KW-rich) → {proof link}

IN PROGRESS
- 8.2.2 Cluster blog #3 — drafted, in editorial QA
- 9.4.1 Bulk citations — 47 of 100 submitted

BLOCKED / NEEDS YOU
- 7.1.2 GMB verification — postcard not received yet, please confirm address
- 11.3.1 LSA — need a copy of insurance certificate

Numbers this week:
- Indexed pages: 12 (+3)
- Tracked KWs in top 100: 41 (+9)
- GMB calls: 14 (+6)

Full sheet: {link to live Google Sheet}
```

### Monthly performance report (Phase 16 → 16.2.2)
- Generate Looker Studio export (PDF).
- Record a 5-minute Loom walking the client through the dashboard.
- Attach a CSV export of the tracking sheet, filtered to "completed in this month".

### Quarterly business review (Phase 16 → 16.2.3)
- 12-slide deck: Goals → KPIs vs goal → Wins → Losses → Plan for next quarter → Asks.

### Annual strategy & roadmap (Phase 16 → 16.2.4)
- Year-on-year delta, ROI, market shifts, next-year plan & budget.

---

## 5. Proof Link Rules (transparency layer)

For every row marked **Completed**, the **Evidence / Proof Link** column **must** contain one of:

| Task type | Acceptable proof |
|---|---|
| Technical change | Before/after screenshot + GSC / PageSpeed / Rich Results URL |
| Content publish | Live URL + first-indexed timestamp from GSC |
| Schema / robots / llms.txt | Validator screenshot + raw URL of the file |
| GMB action | Screenshot of the GMB dashboard with timestamp |
| Citation submit | Live listing URL |
| Backlink | Live URL of the page where the link sits + Ahrefs snapshot |
| Ad change | Google Ads change-history screenshot |
| Report sent | Drive link to the PDF + email send timestamp |

Store all proof in a single `proof/` folder in Drive, organised as `proof/{phase}/{work-id}/{date}-{slug}.{ext}`. This becomes the client's audit trail.

---

## 6. Optional dashboards on top of the sheet

In a second tab (`Dashboard`), build:
- **Phase progress** — `=AVERAGEIF(Sheet1!A:A, 1, Sheet1!O:O)` per phase number.
- **Status distribution** — `COUNTIF` per status.
- **Overdue tasks** — rows where `Planned End < TODAY()` and Status ≠ Completed.
- **This week's burn-down** — count of completed rows per day in last 7 days.

---

## 7. Adapting per client

Not every client needs every row. At kickoff:
- Mark non-applicable rows as **Status = N/A** (don't delete — keep them for the audit trail).
- For multi-location clients, duplicate rows 6.3.* and 7.* per location.
- For e-commerce / SaaS clients, swap LocalBusiness schema rows for Product / Service / SoftwareApplication schema.
