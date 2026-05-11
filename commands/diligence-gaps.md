---
description: Scan your data room against IDV's diligence checklist — flag missing items, surface cross-document inconsistencies, prioritize fixes.
---

Run the `diligence-gaps` skill on the founder's data room.

The user should provide one of:
- **Pasted file list** — names of every file in the data room, one per line
- **`ls`-style dump** — terminal output from `ls`, `tree`, or similar
- **Manual inventory** — natural-language description ("I have a deck, a financial model, and a cap table")

**Required** (the skill will ask if missing):
- **Stage** — Pre-Seed / Seed / Series A or later. Severity tagging depends on stage; the skill will not scan without it.

Optional (improves the output but not required):
- **Company type** — B2B SaaS / Marketplace / Consumer-PLG / Biotech & Deep Tech / Fintech / Hardware & Robotics (Biotech / Deep Tech / Hardware triggers the "Technical documentation" item as required)
- **Are you actively raising?** — affects whether "if applicable" items become required
- **File contents** — paste deck text, financial model summary, or cap table data to enable the cross-document consistency check (numerical facts only in v1.0)

If the user has not yet provided a file list or inventory, ask them to share it now. **v1.0 is text-input only** — no URL ingestion. If the user shares a Drive/Notion/Dropbox link, ask them to paste a file list instead.

Invoke the `diligence-gaps` skill (in `skills/diligence-gaps/SKILL.md`) and follow its instructions exactly. Do not duplicate logic here — the skill owns the IDV-checklist citations, the severity tagging, the cross-document consistency rules, and the output format.
