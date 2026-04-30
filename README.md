# idv-agents

Fundraising AI skills for Invest Detroit Ventures portfolio founders, built by Atomic Object. Drop your pitch deck in Claude Cowork and get IDV-grade feedback in minutes.

> **Status**: v1.0.0 — ready for the IDV Portfolio Summit, May 13, 2026.

## What's in here

Four skills, each available as both a slash command and an auto-trigger:

| Skill | Slash command | What it does |
|---|---|---|
| **Pitch deck review** | `/pitch-deck-review` | Scores your deck 1–5 across the 10 dimensions in the IDV Fundraising + AI Playbook §2.1, surfaces red flags from the playbook's Deck Pitfalls box verbatim, and gives an overall readiness rating tied to §1.2. |
| **KPI recommendations** | `/kpi-recommendations` | Recommends the 5–8 KPIs investors will actually focus on for your company type and stage — verbatim from playbook §1.3 with definition, why-it-matters, how-to-calculate, and healthy range. Flags vanity-metric anti-patterns and previews the next-stage KPI shift. |
| **Diligence gaps** | `/diligence-gaps` | Scans your data room against IDV's official Due Diligence Checklist across all four sections (Business Overview / Financials / Fundraising / Corporate and Legal Docs), severity-tags each gap ([BLOCKER] / [TYPICAL FOR STAGE] / [NICE TO HAVE]), and catches cross-document numerical inconsistencies when contents are provided. |
| **Meeting prep** | `/meeting-prep` | Builds a structured-workflow prep brief per playbook §6.1 — fund basics, partner background, recent investments, anticipated objections, and 5–8 likely questions — plus a talking-points scaffold the founder fills in. Workflow, not autonomous agent (per playbook §6.4). |

## Install

See [INSTALL.md](./INSTALL.md) for the full walkthrough. Quick version:

```
/plugin marketplace add atomicobject/idv-agents
/plugin install idv-agents@idv-agents
```

## Prerequisites

- A paid Claude account (this plugin runs on your Claude tokens, not IDV's)
- Claude Cowork installed
- A pitch deck, KPI dashboard, data room snapshot, or target investor in mind — depending on which skill you're running

## Source of truth

Skills cite the **IDV Fundraising + AI Playbook (Portfolio Summit 2026)** verbatim where applicable, with page numbers. Output is grounded in IDV-curated criteria, not generic LLM advice.

## Attribution & License

Built by [Atomic Object](https://atomicobject.com) for [Invest Detroit Ventures](https://idventures.com).

Licensed under MIT — fork it, modify it, ship it. If you build something useful on top, we'd love to hear about it (john.fisher@atomicobject.com).

## Workshop attendees

If you're at the Portfolio Summit on May 13, 2026: install ahead of the session per INSTALL.md. We'll do the rest live.
