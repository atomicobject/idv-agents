---
description: Recommend the metrics investors will actually focus on for your company type and stage — drawn from IDV's playbook §1.3.
---

Run the `kpi-recommendations` skill for the founder.

The user should provide:
- **Company type** — one of B2B SaaS / Marketplace / Consumer-PLG / Biotech & Deep Tech / Fintech / Hardware & Robotics
- **Stage** — Pre-Seed / Seed / Series A or later

Optionally (improves the output but not required):
- Their **current KPIs** — text list, dashboard description, or a recent deck/investor update
- **Business model details** — pricing, GTM motion, customer segment

If the user has not yet provided company type and stage, ask for both. If they describe a business model that doesn't cleanly map to one of the six §1.3 categories, ask them to pick the closest match — the skill will flag the substitution in output.

Invoke the `kpi-recommendations` skill (in `skills/kpi-recommendations/SKILL.md`) and follow its instructions exactly. Do not duplicate logic here — the skill owns the playbook citations, the vanity-metric calibration, and the output format.
