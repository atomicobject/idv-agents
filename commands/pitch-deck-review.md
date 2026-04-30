---
description: Score your pitch deck against IDV's playbook — 10 dimensions, red flags, concrete suggestions.
---

Run the `pitch-deck-review` skill on the founder's pitch deck.

The user should provide one of:
- Pasted deck text (slide by slide)
- A Google Slides URL (with content they can paste if the URL can't be fetched)
- A PDF or PPTX upload

If the user has not yet provided a deck, ask them to share it now. Then optionally collect stage (Pre-Seed / Seed / Series A), company type (B2B SaaS / Marketplace / Consumer-PLG / Biotech-Deep Tech / Fintech / Hardware-Robotics), and target investor — these improve the output but are not required.

Invoke the `pitch-deck-review` skill (in `skills/pitch-deck-review/SKILL.md`) and follow its instructions exactly. Do not duplicate logic here — the skill owns the rubric, the playbook citations, and the output format.
