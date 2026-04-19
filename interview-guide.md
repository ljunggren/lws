# Career Interview Guide — Wensheng, 2026

*A structured conversation to help Wensheng pick a direction in the LLM-era software dev market. Not a lecture — a set of honest questions with enough market context to answer them well.*

---

## Start here — 5 questions, ~10 minutes

**Don't read the rest of this guide yet.** Answer these five questions first. The rest of the doc is Mats's analysis and options — it'll land better after you've already said what you think.

### How to run it in Claude

```bash
cd lws && claude
```

Then paste this prompt (Chinese or English — Claude will match your language):

> 请一次问我一个问题，等我回答后再问下一个。不要总结我的回答，不要讲课。追问一次不清楚的地方，然后进行下一题。五个问题结束后，简短告诉我你听到了什么，但不要给建议。
>
> *Or in English: Ask me one question at a time. Wait for my answer. Don't summarize or lecture. Follow up once if my answer is unclear, then move on. After the five, tell me briefly what you heard — no advice yet.*

### The 5 questions

1. **What work in the last 12 months made you lose track of time?** (Shipping `ai-new`? A production fire? A refactor? Teaching someone?)
2. **When you use an LLM on the Boozang codebase, does it help or get in the way? Why?**
3. **Your custom framework (CtrlDriver, logService, appBuilder) is genuinely great — and it's also the thing LLMs struggle most to work with.** If you were starting Boozang today, would you build on top of your framework, or on top of React + Vercel AI SDK? Why?
4. **Do you want your day-to-day to include more AI, less, or the same?**
5. **Stable salary + benefits, or equity upside + variance?** Employed at a company, or independent?

### After the 5

Skim **§3 (the six career paths)** only. Your answers above will narrow it to 1–2 candidates automatically. Pick a tentative one.

Only if you want deeper calibration after that, continue to §2 (where Mats rated you on 10 dimensions with evidence), §1 (DORA 2025 market brief), and §4 (the full 22 questions). None of it is required. The 5 questions + one path choice is enough to act on.

You can also read `mats-profile.md` in this repo — Mats rated himself on the same framework, including what he's done to close his own gaps. Fairness cuts both ways.

---

## 0. How to use the full guide (optional)

Run this as a 90-minute conversation (or solo reflection). Five parts:

1. **Market brief** — 10 min. What's actually changing in software dev with LLMs.
2. **Honest baseline** — 15 min. Where Wensheng is today, scored 1–5 with evidence.
3. **Six career paths** — 20 min. Realistic options with upskilling specifics.
4. **Interview questions** — 30 min. The questions that reveal which path fits.
5. **Decision matrix** — 15 min. Weight the paths, pick two to try.

End state: Wensheng has picked a primary path (and optionally a backup), committed to 2–3 upskilling moves for the next 90 days, and written one paragraph on how he'll know it's working.

---

## 1. Market brief — what's actually happening (2025–2026)

Based on the **DORA 2025 State of AI-assisted Software Development** (Google Cloud, ~5,000 respondents):

- **AI adoption is near-universal.** 90% of devs use AI; 80%+ report it increased productivity. *The question is no longer "should we adopt" — it's "how do we extract value."*
- **AI is an amplifier, not a tool.** It magnifies high-performers and high-functioning orgs. It also magnifies dysfunction. Bad codebase + AI = more bad code, faster.
- **Trust gap is real.** 30% of devs report little or no trust in AI-generated code. The scarce skill is **critical validation** — knowing when the AI is confidently wrong.
- **AI helps individual effectiveness the most.** Throughput improves, but **delivery instability increases.** Systems haven't caught up to the speed.
- **Platform engineering is now the foundation.** 90% adoption. Orgs with strong internal platforms extract much more AI value. Poor DX kills AI ROI.
- **Seven team profiles, not one.** From "harmonious high-achievers" to "legacy bottleneck." AI doesn't move teams between profiles; the surrounding system does.

**What this means for individual engineers:**

| The commodity | Still scarce (and getting scarcer) |
|---|---|
| Writing CRUD, boilerplate, glue code | System design that holds up at scale |
| Translating requirements to code | Knowing what *not* to build |
| Implementing specs in mainstream frameworks | Reliability engineering for AI-accelerated systems |
| Copy-paste from Stack Overflow / an LLM | Critical review of AI output — catching confident wrongness |
| Maintaining one stack | Orchestrating agents, tools, and evals |

**The shift:** engineers who only write code are being commoditized. Engineers who *architect systems, validate AI output, design agent workflows, and ship reliable AI-native products* are the scarcest they've ever been.

---

## 2. Honest baseline — where Wensheng is today

*Scored 1–5 using Mats's framework. Notes cite concrete evidence from `bz` and `bz-docker-playwright-ex3`. Wensheng should challenge any score that doesn't match how he sees himself.*

| Dimension | Score | Notes |
|---|---|---|
| **Engineering depth** | **5** | Built CtrlDriver (reactive data-binding framework in pure JS), logService (console-log-based event bus + state machine with self-healing), custom bundler (`appBuilder.js`). Framework survived Node 14→24, Mongoose 6→8, Puppeteer→Playwright. Rare. |
| **Reliability engineering** | **5** | Every edge case has a handler because it actually happened (see `logService.js` — `tryWakeup`, `issueResetCount`, coop protocol, timeout recovery). This is the thing LLMs can't do. |
| **Systems thinking** | **5** | Integrates browser extension + Node service + Docker + Xvfb + Playwright coherently. Most engineers specialize in one layer; he composes across all. |
| **Domain depth (test automation)** | **5** | 10+ years. Knows edge cases nobody documents. |
| **LLM / AI-assisted dev fluency** | **2** | On `ai-new` branch building AI test generation, but coding style (idiosyncratic, globals, custom framework) is the *opposite* of what LLMs are good at. Not currently using LLMs as a force multiplier on his own daily work. |
| **Modern ecosystem fluency (TS, React, LLM SDKs)** | **2** | Codebase is pre-ES6 style — `var`, `function`, globals, `_` prefixes, jQuery. Great for shipping; a gap for interoperability with 2026 tooling and libraries. |
| **Public surface / thought leadership** | **1** | Zero externally visible artifacts. The durability story ("framework I built in 2015 still runs production in 2026") is invisible outside Boozang. |
| **Teaching / knowledge externalization** | **2** | `.agent/memory/anti-patterns.md` has two entries. Most of the hard-won knowledge lives only in his head. |
| **Product strategy** | **3** | Built and ran Boozang's platform layer for a decade. Has instincts. Hasn't formally owned product strategy externally. |
| **Executive presence / comms** | **?** | Not enough signal in the repos to rate. Ask in §4. |

### Overall: 3.2 / 5 — with a rare 5/5/5/5 core

**The asymmetry is the story.** Four dimensions at the ceiling (depth, reliability, systems, domain). Three at the floor (LLM fluency, public surface, modern ecosystem). The top-end is genuinely rare. The bottom-end is fixable in 6–12 months *if chosen deliberately*.

**What this implies:** the career decision is not "should I get better at X" — he's already world-class where it matters. The question is **which of the low-scoring dimensions to invest in, because that choice defines the path.**

---

## 3. Six paths — realistic options

Each path names the positioning, the upskilling plan, the target market, and the tradeoff.

### Path A — Reliability Architect for AI-Native Systems

> "I've spent 10 years building systems that don't fall over. Now I build the ones that make AI systems not fall over."

- **Why it fits:** Wensheng's reliability stance is the exact skill AI-accelerated teams lack. DORA explicitly calls out delivery instability as the downside of AI adoption. That's his forest.
- **Upskill (6 months):** LLM observability (Langfuse, Langsmith, Braintrust), eval-driven development (Inspect, DeepEval, promptfoo), AI SLOs/SLIs, guardrail frameworks (Guardrails AI, NeMo), failure-mode analysis for agentic systems.
- **Target:** Platform teams at AI-native startups; advisory work for enterprises with chaotic AI adoption (Mats's consulting thesis).
- **Tradeoff:** Less code, more policy/process design. If he's happiest with his hands in a codebase, this may feel too abstract.

### Path B — AI QA / Test Intelligence Specialist

> "Test automation meets LLMs: I architect systems that tell you which failures actually matter."

- **Why it fits:** Direct extension of Boozang + the `ai-new` branch. Nobody else has 10 years of test automation plus actually-shipped AI features.
- **Upskill:** Browser agents (Browserbase, Stagehand, Skyvern), LLM-as-judge patterns, test generation from specs (CodiumAI, Meticulous), eval harnesses, RAG over test reports.
- **Target:** Continue at Boozang (as AI-QA product lead) or move to a DevTools vendor (Datadog, Sentry, GitHub, PlayWright team) doing test intelligence.
- **Tradeoff:** Stays in the test-automation niche. Salary ceiling lower than generalist platform work.

### Path C — Agent / MCP Architect

> "I design systems where AI agents actually work — tools, state, recovery, coordination."

- **Why it fits:** His `logService.js` is *already* an agent coordination framework (task dispatch, state machine, recovery, heartbeats). Re-applying that pattern to LLM agents is a small conceptual leap with a huge market demand.
- **Upskill:** MCP spec (Anthropic), function calling & tool use (Claude SDK, Vercel AI SDK), agent orchestration (LangGraph, Inngest, Temporal for agents), multi-agent protocols (A2A, AutoGen), durable execution patterns.
- **Target:** Agent-infra startups, AI platform teams, senior/staff roles at Anthropic/OpenAI/Vercel/Cursor, or independent consulting.
- **Tradeoff:** Bleeding-edge space; tooling churn is intense. Needs appetite for constant re-learning.

### Path D — Full-Stack AI Product Builder

> "I build AI-native products end to end: model, tools, UI, evals, infra."

- **Why it fits:** He already is full-stack. The gap is the modern frontend + streaming/agent UI layer.
- **Upskill:** TypeScript, React/Next.js, Vercel AI SDK, streaming UIs, RSC patterns, modern component libraries (shadcn/ui), Tailwind. *This is the biggest lift — months of deliberate practice with AI as copilot.*
- **Target:** Founding engineer / tech lead at an AI-first product startup. Or relaunch Boozang's UI with this stack.
- **Tradeoff:** Years of pre-ES6 muscle memory to unlearn. High effort. High payoff if the modernization sticks.

### Path E — Open-Source Maintainer / Public Engineer

> "I build battle-tested infrastructure that the ecosystem depends on — and I do it in public."

- **Why it fits:** He has assets that could become OSS (console-log event bus pattern, browser lifecycle manager, coop protocol). The durability story is rare; the *public* version doesn't exist yet.
- **Upskill:** Tech writing (short essays, design docs), conference CFP submission (TestBash, NodeConf, StrangeLoop — though StrangeLoop ended in 2024, so: NodeConf, ViteConf, AI Engineer Summit), OSS packaging (modern npm + TS + semver + CI/CD), community building.
- **Target:** DevRel/staff eng with public profile; foundation/maintainership role; speaking + consulting independent track.
- **Tradeoff:** Slow compounding. Year 1 is mostly output with little return. Year 2–3 is where visibility pays off.

### Path F — Technical Co-founder / CTO (formalized at Boozang or new venture)

> "I've built and scaled it once. I can do it again, this time AI-native from day zero."

- **Why it fits:** He's already the technical half of a founding team in practice. Formalizing it (title, equity, external visibility) changes what's possible.
- **Upskill:** Company-building vocabulary (PLG metrics, retention curves, activation), fundraising fluency, hiring senior ICs, executive comms (board-level storytelling). These are Mats's current gap from the `fitness-eval` doc — pair learning is possible.
- **Target:** Boozang CTO (official), or co-found a new AI-test-automation company (paired with a GTM co-founder).
- **Tradeoff:** Zero-to-one energy vs. steady-state depth. Higher variance on outcome. Requires enthusiastic "yes" on company-building, not just engineering.

---

## 4. Interview questions

Ask these slowly. Write answers down. Patterns matter more than individual replies.

### 4.1 Energy & fulfillment

1. **What work in the last 12 months made you lose track of time?** (Shipping `ai-new`? A production fire? A refactor? Teaching?)
2. **What work drained you even when it "went well"?**
3. **When you imagine a great Tuesday 3 years from now — what does it look like?** (Alone coding? Pairing? Reviewing? Speaking? Meeting customers?)
4. **What's the last thing you built that someone *else* was excited about?** Who was it, and why were they excited?

### 4.2 The LLM question

5. **When you use an LLM on the Boozang codebase, does it help or get in the way?** Why?
6. **Do you want your day-to-day to include more AI, less, or the same?** (No wrong answer — this selects between paths.)
7. **Who's doing work right now that you admire?** (Specific names, blogs, GitHub profiles, talks.) What specifically about what they do?
8. **Do you want the *outcome* AI produces (faster shipping, less toil), or do you want to *shape* how AI works (frameworks, protocols, reliability)?**

### 4.3 Public surface

9. **How do you feel about writing publicly?** (Essays, blog posts, design docs.) Energy drain or neutral?
10. **How do you feel about speaking at conferences?** Would one well-received talk per year be fun, or a tax?
11. **If a potential employer Googled you today, what would you *want* them to find?**
12. **Would you rather be known by 10,000 developers for a framework, or by 50 hiring managers for a reputation?**

### 4.4 Risk & structure

13. **Stable salary + benefits, or equity upside + variance?** (Salary range if you know it.)
14. **Employed at a company, or independent (consulting / contracting)?**
15. **If Boozang stayed exactly where it is for 3 more years, would you be content?**
16. **What's your 3-year financial goal?** (Keeps compensation conversations honest.)

### 4.5 The codebase question (hard but important)

17. **Your custom framework (CtrlDriver, logService, appBuilder) is genuinely great — and it's also the thing an LLM struggles most to work with.** If you were starting Boozang today, would you build on top of your framework, or on top of something like React + Vercel AI SDK? *Why?*
18. **Does the cost of "only Wensheng can maintain this" outweigh the benefit of "this exact architecture shipped reliably for 10 years"?** What would change your mind?
19. **If we added a mainstream frontend and typed backend on top of your core engine, would that feel like an upgrade or a concession?**

### 4.6 Team & leverage

20. **Do you want to write more code, or more *leverage* on other people's code (reviews, teaching, architecture docs)?**
21. **Would you enjoy teaching a junior engineer to match your standard, or is that a chore?**
22. **In the Scout/Propose/Decide pattern with Mats and Claude, what feels right and what feels wrong?**

### 4.7 The forced choice

*After working through the above, force a ranking:*

Rank the six paths (A–F) on two axes — 1 (low) to 5 (high):

|  | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| **Excitement** — I want to do this | | | | | | |
| **Feasibility** — I can realistically invest in it in 2026 | | | | | | |

**Product of the two scores** = priority for the next 90 days. Pick the top one as primary; the second as backup.

---

## 5. Decision matrix — pick a direction

After the interview, fill this out:

### 5.1 My primary path (next 12 months)

Path letter: **_____**

Positioning one-liner (rewrite in your own words):
> _______________________________________________

### 5.2 Upskilling commitments (next 90 days)

Pick 2–3 maximum. Concrete. Time-boxed.

| # | Commitment | Evidence of progress by day 90 |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |

**Examples per path (for inspiration, not prescription):**

- **Path A:** Ship one Langfuse/Langsmith dashboard for Boozang's AI features. Write one eval harness with 20 labeled cases.
- **Path B:** Prototype an LLM-as-judge classifier for Boozang test failures. Publish one post on "AI triage for test results."
- **Path C:** Build one MCP server exposing Boozang's test modules as tools. Ship a LangGraph workflow that uses it.
- **Path D:** Rewrite one IDE feature in React + TS + Vercel AI SDK. Measure productivity before/after.
- **Path E:** Extract the console-log event bus as an npm package. Write one essay: "The framework I built in 2015 still runs production in 2026."
- **Path F:** Draft the Boozang CTO job description. Sit down with Mats on equity, title, and customer visibility.

### 5.3 How I'll know it's working (day 90 check)

Write one paragraph. Concrete signal — not a feeling.

> _______________________________________________

### 5.4 What I'm *not* doing

Equally important. The paths *not* chosen — name them and commit to ignoring them.

> _______________________________________________

---

## 6. Notes for Mats running the interview

- **Don't sell a path.** The honest scores in §2 already point toward A, C, and F (the paths that leverage his rare strengths without forcing a full modernization). Let him arrive there.
- **Watch for path D (full-stack modernization).** It's the most expensive and the one he's most likely to say yes to out of obligation or ego. If he picks it, ask twice.
- **The codebase question (§4.5) is the one he'll be least comfortable with.** Ask it gently. His framework *is* genuinely great, and acknowledging that first makes it possible to discuss its tradeoffs honestly.
- **End with a concrete 90-day plan, not a 3-year vision.** The 3-year vision shifts. The 90-day plan is what actually compounds.

---

*Sources grounding this guide: `bz-business/wensheng.md`, `bz-business/strategy/fitness-eval-ai-product-lead.md` (rating system), `bz-business/strategy/three-backgrounds.md` (positioning), `bz-business/refs/2025_state_of_ai_assisted_software_development.pdf` (DORA), `bz/.agent/memory/journal.md` (code survival evidence), and the actual Wensheng-authored files: `bz/clientApp/ideApp/system/CtrlDriver.js`, `bz/appBuilder.js`, `bz-docker-playwright-ex3/logService.js`.*
