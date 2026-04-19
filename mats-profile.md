# Mats — Peer Profile

*Shared alongside the interview guide so you can see where I stand using the same 1–5 framework, with one extra column: what I've actually done to close my gaps. Same honesty rules — cite evidence, don't soften.*

---

## 1. Why this exists

The interview guide rates you on 10 dimensions. It would be unfair to hand you an honest assessment without sharing mine using the same framework. We're working on the same problem — how software engineers stay valuable in the LLM era — from different starting points.

**Where we're the same:** engineering depth, systems thinking, domain judgment.
**Where we're the mirror:** I score high on LLM fluency and knowledge externalization and low on custom-framework reliability engineering. You score the inverse. That's the opportunity — the two profiles combined cover the full stack of the LLM-era software org.

---

## 2. Honest baseline — where I stand (same framework as §2 of the interview guide)

| Dimension | Score | Evidence | What I've done to close the gap |
|---|---|---|---|
| **Engineering depth** | **4** | 22 years enterprise. MongoDB 4→8 migration on production (9,200+ lines, 14 releases in 17 days, zero data loss). Shipped production AI at LANDR (TypeScript monorepo, Gemini 2.0, MCP). | N/A — this is a strength. The 4 (not 5) reflects that I don't build bespoke frameworks from scratch the way you do. Different shape. |
| **Reliability engineering** | **3** | Can ship under pressure (5 releases in 24 min debugging token auth). Built `.agent/` escalation framework (L0–L3). Anti-patterns log. | **Done:** built the reliability framework for human-AI systems (decision flows, escalation levels, anti-pattern logs) across 10+ repos. **Gap:** haven't designed self-healing infrastructure from scratch (that's your lane). |
| **Systems thinking** | **5** | M.Sc. Complex Adaptive Systems, Chalmers. Published paper on particle aggregation in random flows (Physical Review E, 2005). Sees feedback loops, not just tasks — the "white-glove trap" diagnosis on the RA engagement came from pattern recognition, not a framework. | N/A — strength. |
| **Domain depth** | **4 (agentic methodology) / 5 (enterprise integration)** | Two domains. 12 years delivering to tier-1 telcos on-site (Sprint, T-Mobile, Vodafone, Bell, Rogers, Telefonica, China Unicom, Telenor). 2 years refining agentic methodology daily. | N/A on enterprise. On agentic methodology, closing gap through daily practice across 10+ repos. |
| **LLM / AI-assisted dev fluency** | **5** | Shipped production AI product (Gemini 2.0 + MCP) at LANDR. Built 3 MCP servers. Multi-model fluent (Claude Opus/Sonnet, Gemini Flash/Pro). Daily practitioner across product, infra, testing, CI/CD, docs. | **Done:** went from zero to shipping in ~18 months by committing to daily practice + refining methodology in public repos. |
| **Modern ecosystem fluency** | **4** | TypeScript monorepo at LANDR. React, Express, MCP, Vercel AI SDK–adjacent patterns. Current on the stack. | **Done:** LANDR engagement was the forcing function — TypeScript + React + modern tooling became daily work. Not 5 because it's 2 years, not 10. |
| **Public surface / thought leadership** | **2** | LinkedIn active. Zero published blog posts. Zero conference talks. Extensive infrastructure but invisible in the "AI" conversation externally. | **In progress:** built the agentic-coder profile, the three-backgrounds positioning doc, case studies (Beeye, Devin), consulting packages (AI Collaboration Systems, Enterprise Agentic Consulting). Video script for "testing for vibe coding" in `bz-business/product/`. **Still open:** nothing published under my name yet. This is my #1 gap. |
| **Teaching / knowledge externalization** | **4** | 10+ repos with `.agent/` directories. Escalation levels, decision flows, anti-patterns logs, memory systems, team-role definitions. Open-source-ready methodology, currently in private repos. | **Done:** the `.agent/` system itself. **Still open:** none of it is externally accessible. Moving this to a public template is a 2026 priority. |
| **Product strategy** | **3** | Built and ran Boozang 10 years — that's product ownership. Has instincts (training wheels, productisation over dependency, success-factor gating). | **In progress:** packaging the RA transformation thesis into a repeatable methodology. **Still open:** no VP-Product title at a bigger company. No formal product training (no Reforge, no Lenny's, no CPO track). |
| **Executive presence / comms (board-level)** | **2** | No direct PE board experience. Currently operates one level down from client comms (Nick owns the relationship on RA). Haven't presented transformation findings to investors. | **In progress:** co-presenting with Nick on the RA report is the plan. "Getting reps" is the path — no shortcut. **Still open:** this closes through practice over the next 12 months, not coursework. |
| **Sales / business development** | **3** | Ran Boozang commercially for 10 years. SPIN selling certified. B2B sales training. Good relationship instincts (LinkedIn/Stan interactions). | **Still open:** Boozang didn't scale commercially — honest assessment. First consulting engagements need a Nick-like partner until I have my own book. |
| **Enterprise services understanding** | **4** | 12 years inside tier-1 telco delivery. Knows how services orgs work, bill, and get stuck. Ran independent consulting engagements. | **Still open:** haven't personally led a services-to-product transition at an org (Boozang was product-native from day one). |

### Overall: 3.6 / 5

**The asymmetry, mirrored:** I'm strong where you're developing (LLM fluency, modern ecosystem, methodology externalization). I'm weak where you're strong (custom reliability engineering, deep framework work). I'm weak in a place you *might* also be weak (public surface) — that's shared territory.

---

## 3. What I've done in the last 18 months to close gaps

Concrete moves, not intentions:

- **Shipped a production AI product** (LANDR, 2024–present) — closed the LLM-fluency gap from "reads blog posts" to "ships in production"
- **Built 3 MCP servers** — moved from "uses MCP" to "understands the protocol well enough to design against it"
- **Executed MongoDB 4→8 migration on Boozang** using the methodology — proof that AI collaboration works on my own production system, not just someone else's
- **Refined the `.agent/` system across 10+ repos** — moved from ad-hoc chat prompts to a repeatable, audited methodology
- **Packaged consulting offerings** (AI Collaboration Systems, Enterprise Agentic Consulting) with credential pages, case studies, engagement models — the scaffolding is built; now I need first clients willing to be named
- **Wrote case studies** (Beeye, Devin) that map my methodology to concrete outcomes
- **Started RA engagement** with Nick — this is where the board-level-comms gap gets closed through reps
- **Built `bz-agent`** — zero-dependency npm package scaffolding `.bz/` directory for any repo. Methodology → distributable.

**What I have NOT done yet (gaps still open):**

- ❌ Published anything under my name on an external platform (blog, Substack, LinkedIn long-form, Medium, conference)
- ❌ Given a public talk
- ❌ Open-sourced the `.agent/` system as a public template
- ❌ Presented transformation findings directly to a board
- ❌ Closed a consulting engagement where I'm the lead contact (not behind Nick)

**The pattern:** I've built a lot of infrastructure and shipped real work. I haven't translated that into external visibility. That's the next 12 months' main job.

---

## 4. Why I'm sharing this with you

Three reasons:

1. **Fairness.** Asking you to do an honest self-assessment without offering one in return is cheap.
2. **Signal.** You can see from this table that I don't believe low scores are shameful — I put a 2 on executive presence in writing. That's the standard for your assessment too. The goal isn't to score high; it's to *know your actual shape* so you can deploy yourself well.
3. **Complementarity.** Our profiles together cover territory neither of us covers alone. Whatever path you pick in the interview guide, the question of whether we work together on it is worth raising explicitly.

---

## 5. What I'd rate myself in 12 months if the plan works

If the public-surface and executive-presence work lands:

- Public surface: 2 → 4 (2–3 published essays, 1 talk, `.agent/` template public)
- Executive presence: 2 → 3 (co-presented 2–3 engagements, led 1 directly)
- Product strategy: 3 → 4 (RA transformation thesis battle-tested on 2 more engagements)

Everything else: same or incremental.

**Where I'd still be a 2 or 3 at the end of 2026:** sales/BD (needs repeat client success, not more infra), and honestly — I might discover I prefer being the "depth behind the deal" rather than the deal-closer. That's a real question, not just a gap.

---

## 6. Peer notes — where we'd complement each other

If you picked **Path C (Agent/MCP Architect)** or **Path A (Reliability Architect for AI-Native Systems)** from the interview guide, we overlap at exactly the right seam:

- Me: LLM/MCP fluency + methodology + enterprise access
- You: custom-framework reliability + deep systems + domain depth
- **Together:** "Enterprise AI Quality Engineering" — the `bz-business/strategy/three-backgrounds.md` thesis, but both names on it.

That's not a pitch for you to pick Path C. It's a note that *if* you pick it, the door is open to do it together rather than apart.

---

*Source files feeding this profile: `bz-business/mats-ljunggren-agentic-coder.md`, `bz-business/mats-ljunggren-agentic-engineer-cv.md`, `bz-business/strategy/fitness-eval-ai-product-lead.md`, `bz-business/strategy/three-backgrounds.md`, `bz-business/consulting/ai-collaboration-systems.md`, `bz-business/consulting/enterprise-agentic-consulting.md`.*
