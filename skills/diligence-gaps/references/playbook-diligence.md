# Playbook Extracts — Diligence Gaps

**Source**: `Notes/Fundraising AI Playbook Guide v3.pdf` ("The Fundraising + AI Playbook — A Practical Guide for Portfolio Founders, From Pre-Fundraise to Close, Portfolio Summit 2026"), 22 pages.

**Scope of this file**: Playbook content NOT redundant with the IDV Due Diligence Checklist. The playbook §2.3 Data Room section is content-identical to the IDV checklist (see `idv-diligence-checklist.md` — that's the canonical source for the file-list and "what investors evaluate" content). This file holds the unique playbook content the skill needs: §2.6 (Diligence Gap Analysis principles), §1.2 row (stage-aware readiness), §2.7 (tool suggestions), and §7.4 (cross-cutting AI guardrails).

---

## §1.2 Fundraising Readiness Scorecard — Materials & Data Room row (p.4)

> Before entering a raise, founders should honestly assess readiness across five dimensions. Score each 1–5 and discuss gaps with your lead investor or advisor.

| Dimension | What "Ready" Looks Like | Red Flags |
|---|---|---|
| Materials & data room | Deck, model, data room 80%+ complete | No deck, no model, no organized diligence materials |

**Skill usage**: Use the "80%+ complete" phrasing as the bar for stage-aware severity. A founder with 20% of the checklist filled at active-raise time is in red-flag territory; a founder at 80%+ is ready.

---

## §2.3 Data Room — Framing Quote (p.7)

> The data room should be 80–90% complete before outreach starts. Investors form impressions of operational quality based on how organized your diligence materials are. Use our firm's due diligence checklist below as your core data room framework.

> *Successful fundraising is an exercise in effectively managing relationships and sharing the story of how your business is primed to grow. Your dataroom should transparently help investors understand your vision, your key relationships, and how you've navigated your path to be a strong candidate for investment.*

**Note**: The checklist content that follows §2.3 in the playbook is content-identical to the IDV checklist — pull from `idv-diligence-checklist.md` instead, using IDV's exact wording.

---

## §2.6 Diligence Gap Analysis (p.10) — VERBATIM

> Before investors start digging, do their job for them. Identify and close the gaps proactively.
> - Run through the data room checklist in Section 2.3 and flag every item that is incomplete, missing, or weak.
> - Prioritize gaps by severity: what would cause an investor to pause or pass?
> - Assign owners and deadlines for each gap. Track progress in a shared document.
> - Common gaps: messy cap table, unsigned IP assignments, missing board minutes, unclear unit economics, no customer references prepared.

**Skill usage**:
- The framing quote *"Before investors start digging, do their job for them."* (p.10) opens the skill output's principles section.
- The severity question *"what would cause an investor to pause or pass?"* (p.10) anchors the `[BLOCKER]` severity definition.
- The five common gaps are the canonical anti-pattern list — quote them verbatim where applicable to the founder's situation: *"messy cap table, unsigned IP assignments, missing board minutes, unclear unit economics, no customer references prepared."*

---

## §2.7 Tools — Diligence-related (p.10)

> Diligence prep (proposed) | Diligence Gap Agent (Open) | Scans materials against our firm's checklist and surfaces missing items

**Tool callouts the skill may suggest (light touch, ≤1 mention per item)** — drawn from §2.7 and adjacent playbook tool tables:

- **Carta** — for cap table management, vesting schedules, and SAFE/CN tracking
- **Pulley** — alternative cap table tool
- **DocSend** — for sharing materials with view tracking
- **Notion / Google Drive / Dropbox** — for data room organization
- **Clerky / Stripe Atlas** — for formation documents (incorporation, bylaws, founder agreements)
- **Ironclad / Common Paper / standard SAFE templates (Y Combinator)** — for contracts and SAFEs

**Skill usage**: Cap at one tool mention per missing item. Match the tool to the gap (e.g., "Carta for cap table" — not "Carta for everything"). Do not push tools the founder did not ask about; suggest only when relevant to a flagged gap.

---

## §7.4 Where AI Helps and Where It Hurts (p.20) — Cross-Cutting

| AI Should Help With | AI Should NOT Do |
|---|---|
| Drafting initial outreach templates that the founder edits | Sending any message autonomously |
| Summarizing investor backgrounds for personalization | Generating mass-personalized outreach at scale (investors can tell) |
| Suggesting follow-up timing based on engagement signals | Deciding which investors to deprioritize or drop |
| Identifying talking points based on investor interests | Fabricating connections or shared interests that do not exist |
| Formatting and proofreading | Replacing the founder's authentic voice with AI-generated language |

**Skill usage** for diligence-gaps specifically:
- Do NOT fabricate gaps in materials the founder didn't share (analogue to "Fabricating connections… that do not exist").
- Do NOT rewrite the founder's documents (analogue to "Replacing the founder's authentic voice").
- DO format the missing-items list and prioritize by diligence sequence (analogue to "Formatting and proofreading", "Suggesting follow-up timing").

---

## Notes for Skill Author

1. **The checklist is in `idv-diligence-checklist.md`, not here.** This file is for the principles, severity framing, tool list, and cross-cutting guardrails.
2. **Quote §2.6 verbatim** — the *"Before investors start digging, do their job for them."* line is the marquee framing for the skill's output.
3. **Common-gaps list is reusable.** When a founder is missing cap table cleanliness, IP assignments, board minutes, unit-economics clarity, or customer references — quote the §2.6 list verbatim and flag.
4. **Stage-aware severity from §1.2** — the "80%+ complete" bar comes from the §1.2 Materials & data room row. Use it to calibrate `[TYPICAL FOR STAGE]` vs `[BLOCKER]`.
