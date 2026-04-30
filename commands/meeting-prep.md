---
description: Build a one-page prep brief for an investor meeting — fund profile, partner background, anticipated objections, rehearsal Q&A. IDV happy-path mode included.
---

Run the `meeting-prep` skill to build a structured prep brief for an investor meeting.

The user should provide:

**Required:**
- **Target investor** — at minimum a fund name. Better: + partner name. Best: + thesis / public web URL / LinkedIn.
- **Meeting context** — type (intro / partner / full partnership), duration, who else will be in the room.

**Optional but improves output:**
- Founder's deck (paste text or share file) — sharpens objection prep
- Founder's stage and company type (Pre-Seed / Seed / Series A; B2B SaaS / Marketplace / Consumer-PLG / Biotech-Deep Tech / Fintech / Hardware-Robotics)
- Mutual connection / intro source
- Prior touchpoints with this investor

**IDV happy-path mode**: If the user is prepping for an IDV / Invest Detroit / ID Ventures meeting — or mentions specific IDV programs (MIF, Venture 313, Metro 313, FAM) or specific IDV team members (Martin Dober, Patti Glaza, Lee Rawlings, Belvin Liles, Jeff Ponders, Prem Bodagala, 'Tember Shea) — the skill will branch into IDV-mode and use the public IDV org context loaded into `references/idv-org-context.md`. Trigger phrases include "prep me for IDV", "prepping for an IDV meeting", "prep for Invest Detroit".

**Web research**: The skill MAY use WebFetch for public sources (fund website, partner LinkedIn, podcast appearances) but will ask approval per request and fall back to `[FOUNDER TO RESEARCH: <where>]` markers when blocked, paywalled, or absent.

If the user has not yet provided target investor info, ask them now. Then optionally collect the rest.

Invoke the `meeting-prep` skill (in `skills/meeting-prep/SKILL.md`) and follow its instructions exactly. The skill is **deliberately a structured workflow, not an autonomous agent** (per playbook §6.4 p.18) — it produces scaffolding the founder fills in for objection responses, talking points, and asks. Do not duplicate logic here — the skill owns the §6.1 brief structure, the §6.2 objection list, the talking-points scaffold, the IDV-mode adjustments, and the output format.
