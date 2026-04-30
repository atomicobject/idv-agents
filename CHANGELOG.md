# Changelog

All notable changes to `idv-agents` are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] — 2026-04-30

Initial release. Built for the Invest Detroit Ventures Portfolio Summit on May 13, 2026.

### Added

- **`pitch-deck-review`** — Scores a founder's pitch deck 1–5 across the 10 dimensions in the IDV Fundraising + AI Playbook §2.1, surfaces red flags from the Deck Pitfalls box verbatim, and gives an overall readiness rating tied to playbook §1.2. Includes a tightened competitor-naming guardrail to prevent niche-market hallucination.
- **`kpi-recommendations`** — Recommends the 5–8 KPIs investors focus on for the founder's company type and stage, verbatim from playbook §1.3 (definition + why-it-matters + how-to-calculate + healthy range). Flags vanity-metric anti-patterns from §1.1 with funnel-context calibration, frames output as headline metrics for the monthly investor update, and previews the next-stage KPI shift.
- **`diligence-gaps`** — Scans a founder's data room against IDV's official Due Diligence Checklist using IDV's exact wording across the four sections (Business Overview / Financials / Fundraising / Corporate and Legal Docs). Severity-tags each gap ([BLOCKER] / [TYPICAL FOR STAGE] / [NICE TO HAVE]), previews the page-2 "Information we are evaluating in Diligence" categories, and catches cross-document numerical inconsistencies when contents are provided.
- **`meeting-prep`** — Builds a structured-workflow prep brief for a specific investor meeting per playbook §6.1 — fund profile, partner background, recent investments, portfolio overlaps, anticipated objections, 5–8 likely questions, and a talking-points scaffold the founder fills in. Includes IDV happy-path mode that distinguishes IDV's three fund relationships (direct funds, MIF state-program recipient, Venture 313 founding partner). Designed as a workflow with lightweight AI assistance, not a full autonomous agent, per playbook §6.4.

### Sources

All four skills cite the following IDV-curated, founder-facing materials verbatim where applicable, with page or section numbers:

- **IDV Fundraising + AI Playbook (Portfolio Summit 2026)** — canonical source for `pitch-deck-review`, `kpi-recommendations`, and `meeting-prep`.
- **IDV Due Diligence Checklist** — canonical source for `diligence-gaps` checklist items, section structure, and exact wording.

### Distribution

- Public GitHub repo: `https://github.com/atomicobject/idv-agents`
- Offline install zip: `dist/idv-agents-1.0.0.zip` (also attached to the GitHub release)

[1.0.0]: https://github.com/atomicobject/idv-agents/releases/tag/v1.0.0
