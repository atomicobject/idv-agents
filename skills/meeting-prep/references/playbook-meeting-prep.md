# Playbook Extracts — Meeting Prep

**Source**: `Notes/Fundraising AI Playbook Guide v3.pdf` ("The Fundraising + AI Playbook — A Practical Guide for Portfolio Founders, From Pre-Fundraise to Close, Portfolio Summit 2026"), 22 pages.

**Scope of this file**: All Stage 6 (Meeting Preparation) content the skill cites, plus cross-references the meeting-prep skill draws from (§1.4 Warm Intro Strategy, §7.2 Outreach Strategy, §7.4 cross-cutting AI guardrails). All quotes verbatim.

---

## Stage 6: Meeting Preparation (p.17)

> Goal: Walk into every investor meeting with deep knowledge of the fund, the partner, their portfolio, and a prepared response for likely objections.

---

## §6.1 Research Framework (p.17) — VERBATIM

> For every meeting, prepare a one-page brief covering the following:

| Research Area | What to Know | Where to Find It |
|---|---|---|
| Fund basics | Fund size, stage focus, investment pace, recent fund vintage | Fund website, PitchBook, LP disclosures |
| Partner background | Career history, board seats, areas of expertise, deal sourcing preferences | LinkedIn, podcast appearances, published writing, Twitter/X |
| Recent investments | Last 3–5 deals. What themes are they pursuing? What do these companies have in common with yours? | Crunchbase, fund blog, press releases |
| Portfolio overlaps | Any competitive or adjacent companies in the portfolio? If so, what is the narrative? | Portfolio page, PitchBook |
| Known concerns | What has this investor said publicly about your market, business model, or stage? | Interview transcripts, podcasts, Twitter/X |
| Mutual connections | Who do you know in common? Who introduced you? What is the relationship context? | LinkedIn, your CRM, intro source |
| Meeting format | How long? Who else will be in the room? Is this a first meeting, partner meeting, or full partnership? | Ask the investor or their team directly |

**Skill usage**: This table is the canonical structure for the §6.1 one-page brief portion of skill output. Each row maps 1:1 to a section in the brief. The "Where to Find It" column is what populates the `[FOUNDER TO RESEARCH: <where>]` markers when info is missing.

---

## §6.2 Objection Preparation (p.17–18) — VERBATIM

> Identify the 5–7 most likely objections and prepare clear, honest responses for each. Common objections by stage:
> - **Market too small:** Prepare bottoms-up TAM expansion logic and analogies to markets that grew unexpectedly.
> - **Competitive concerns:** Show your wedge, switching costs, or structural advantages. Acknowledge strong competitors honestly.
> - **Team gaps:** Explain your hiring plan with specific profiles and timelines. Show self-awareness about what is missing.
> - **Unit economics:** Walk through the path to profitability at scale. Show which levers improve with growth.
> - **Timing / "why now":** Identify the structural change (technology shift, regulatory change, behavior change) that makes this the right moment.
> - **Capital efficiency:** Demonstrate discipline in spending. Show what you achieved with prior capital relative to peers.

**Skill usage**: Use these six as the core objections list. Quote the framing verbatim per objection. Per §6.4 (below), tailor each as a **prep-response prompt** the founder fills in — do NOT generate a pre-baked response.

---

## §6.3 Meeting Execution Tips (p.18) — VERBATIM

> - Open with the insight, not the product. Lead with why the world is changing.
> - Listen more than you talk. The best meetings are conversations, not presentations.
> - Ask the investor what they need to get to a decision. Then deliver it.
> - End with clear next steps and a timeline. "I will send X by Y" is better than "let us stay in touch."

**Skill usage**:
- *"Lead with why the world is changing"* anchors the **Opening insight** prompt in the talking-points scaffold.
- *"I will send X by Y is better than 'let us stay in touch.'"* anchors the **Closing / next steps script** prompt. Quote verbatim.

---

## §6.4 Recommendation: Agent vs. Structured Workflow (p.18) — CRITICAL DESIGN CONSTRAINT — VERBATIM

> Our recommendation is to build Meeting Prep as a **structured workflow with lightweight AI assistance** rather than a full autonomous agent. The research components (fund profile, partner background, portfolio analysis) are well-suited to AI retrieval and summarization. The objection preparation and talking points benefit from templates and prompts but require founder judgment.

**Skill usage** — this is the most important rule the skill operates under:
- **Research components** (fund basics / partner background / recent investments / portfolio overlaps / known concerns / mutual connections / meeting format — i.e., §6.1 rows): AI summarizes from cited public sources or marks `[FOUNDER TO RESEARCH]`. **AI may produce content here.**
- **Objection preparation, talking points, asks**: AI provides templates and prompts. **Founder fills in the actual response.** AI does NOT produce a finished response or pretend to write in the founder's voice.

This is the single constraint that prevents the skill from becoming a black-box "here's your prep, good luck" agent. Every output section that requires founder judgment should end in `[FOUNDER TO DRAFT]` or `[FOUNDER TO LIST]` or similar — NOT a finished script.

---

## §6.5 Tools — Meeting Prep (p.18) — VERBATIM

> Meeting prep (proposed) | Meeting Prep Workflow (Open) | Structured template + AI-powered research brief per investor meeting

**Skill usage**: This is the tool callout that defines what the skill is. "Structured template + AI-powered research brief" — both halves matter. Template = founder-completed scaffolding (§6.4 design constraint). Research brief = AI-summarized public-source content (§6.1 rows).

---

## §1.4 Warm Intro Strategy (p.5) — Tier Framework for Mutual Connections

> Cold outreach can work, but warm introductions remain the highest-conversion path to investor meetings. Build a three-tier intro strategy:

| Tier | Source | When to Use |
|---|---|---|
| **Tier 1 — Direct connections** | Your existing investors, advisors, board members, and trusted founder network | Highest-priority targets where personal endorsement carries the most weight |
| **Tier 2 — Warm two-hops** | A mutual connection you both know but haven't activated; LinkedIn second-degree paths with a clear reason for the intro | Mid-priority targets; needs explicit framing for why this match makes sense |
| **Tier 3 — Cold-with-personalization** | Direct outreach with a specific reason tied to the investor's portfolio, writing, or stated thesis | When no warm path exists; requires homework to land |

**Skill usage**: For the §6.1 "Mutual connections" row in the brief, layer this tier framework when the founder asks "how strong is my warm path to this investor?" — Tier 1 = strong direct, Tier 2 = warm two-hop, Tier 3 = cold-with-personalization. Don't fabricate Tier 1 connections that don't exist (per §7.4).

---

## §7.2 Outreach Strategy (p.19) — "One Clear Ask"

> Pre-meeting outreach principles:
> - **Personalize the first line.** Reference something specific to the investor (a recent investment, a podcast, a tweet) — not "I admire your work."
> - **One clear ask.** A second meeting? A term sheet review? An intro to a portfolio CEO? Pick one. Multiple asks dilute the signal.
> - **Brief is better than long.** Three sentences > three paragraphs.
> - **Make the next step easy.** Suggest two specific times. Attach the deck. Pre-empt the friction.

**Skill usage**: The **"One clear ask"** principle anchors the **One clear ask** prompt in the talking-points scaffold (Step 4D). Quote verbatim. The founder picks ONE ask — never a menu.

---

## §7.4 Where AI Helps and Where It Hurts (p.20) — Cross-Cutting — VERBATIM

| AI Should Help With | AI Should NOT Do |
|---|---|
| Drafting initial outreach templates that the founder edits | Sending any message autonomously |
| Summarizing investor backgrounds for personalization | Generating mass-personalized outreach at scale (investors can tell) |
| Suggesting follow-up timing based on engagement signals | Deciding which investors to deprioritize or drop |
| Identifying talking points based on investor interests | Fabricating connections or shared interests that do not exist |
| Formatting and proofreading | Replacing the founder's authentic voice with AI-generated language |

**Skill usage** for meeting-prep specifically:
- **DO** summarize investor backgrounds for personalization (§6.1 rows from public sources, with citation).
- **DO** identify talking points based on investor interests (the talking-points scaffold).
- **DO NOT** fabricate connections or shared interests (§6.1 "Mutual connections" row — if the founder didn't tell you about a connection, don't invent one).
- **DO NOT** replace the founder's authentic voice with AI-generated language (every objection response and talking point ends in `[FOUNDER TO DRAFT]`, never a finished script).

---

## Cross-References (for context, not directly quoted in skill output)

- §1.2 Readiness Scorecard (p.4) — overall fundraise readiness; meeting-prep assumes the founder is already past this gate.
- §2.5 Valuation & Terms (p.9): *"Be precise in your ask. Ranges signal uncertainty. Pick a number and defend it."* — relevant to the §7.2 one-clear-ask principle.
- §3.2 How Much to Raise (p.11): *"Target 18–24 months of runway post-close."* — relevant to objection #6 (Capital efficiency).
- §9.1 What to Capture (p.21–22) — post-meeting framework feeds into next-meeting prep (v2.0 enhancement: chain meeting-prep across a sequence with the same investor).

---

## Out-of-Scope (Closed Items)

These stages are referenced in the playbook for context but should NOT inform this skill:

- **§4.2 Investor Targeting Agent (Closed)** (p.13) — proprietary IDV deal-flow capability. Don't pull from this section.
- **§5.3 Process Management — Multi-Agent System (Closed)** (p.16) — proprietary. Don't pull from this section.
- **Stage 8 Reference Architecture** (p.21) — not in v1.0 scope.

---

## Notes for Skill Author

1. **Quote, don't paraphrase.** When the skill cites the playbook, use the exact language above. Page numbers required.
2. **§6.4 is the constraint.** Every objection / talking-point / ask output section must end with `[FOUNDER TO DRAFT]` or `[FOUNDER TO LIST]` — never a finished script. The founder writes their own words. AI scaffolds.
3. **§7.4 is universal.** No fabricated connections, no replacing founder voice, no autonomous action.
4. **Closed-section boundary.** Don't pull from §4.2 or §5.3. Those are IDV-internal capabilities outside the founder-facing skill.
