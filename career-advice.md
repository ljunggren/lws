# Career Advice — Wensheng

A strategic memo, grounded in the actual Boozang codebase and the decisions that held up over years.

---

## 1. What the evidence shows

You built a test-automation platform — custom JS framework, Docker test runner, browser extension, Node services, Playwright integration — mostly alone, before AI-assisted development was a thing. The platform has survived:

- **Node.js 14 → 20 → 24** without touching core architecture
- **Mongoose 6 → 8** and the callback-to-async/await transition
- **Puppeteer → Playwright** migration
- Years of production use at scale

The `bz` journal and anti-patterns log are, in aggregate, a portrait of code that ships and keeps shipping. The state machine in `logService.js` (init → ready → run → end, with timeout recovery and wakeup logic) is the tell: every edge case there is a handler for an edge case that actually happened.

**That's the signal.** Durable architecture is rare. Most custom frameworks die in 6 months; yours is still the spine of a production platform a decade later.

---

## 2. Your superpowers — amplify these

### Reliability engineering as a default stance

You design for the failure mode first. The coop protocol, self-healing browser lifecycle, issue-reset counting to prevent infinite loops — these are things most engineers add *after* incidents. You added them before.

**How to amplify:** this is your differentiator. Name it. The industry is full of engineers who write happy-path code. Reliability thinking is rare, senior-level, and hard to teach. Lead with it.

### Full-stack integration

Browser extensions, Node services, Docker containers, Xvfb display management, Playwright automation — most engineers specialize in one layer. You compose across all of them, and the interfaces hold.

**How to amplify:** the "thin spec, layered integration" approach generalizes. It's applicable to any platform company building multi-surface products.

### Pragmatism over ideology

Using `console.log` as an event bus is unorthodox. It also works, crosses the browser/Node boundary cleanly, and needs zero dependencies. Most senior engineers would reject it on principle; you shipped it and it survived.

**How to amplify:** this is "taste," and it's hard-won. Most of the time, it'll look like "doing the unfashionable thing." Don't let external fashion pressure compromise it.

---

## 3. Growth edges — the leverage opportunities

These are not skill gaps. They're places where more of your time goes to things only you can do.

### a. Externalize tacit knowledge

The anti-patterns log has two entries. The journal has dozens of hard-won lessons (Express `req.query` immutability, minified error names, Mongoose `strictQuery`, `findByEmail` callback mismatch). Most of this only lives in your head.

**Risk:** if you're the only one who knows why a line of code exists, the codebase can't scale beyond you — and you can't scale beyond the codebase.

**Move:** record one "war story" per week — a 5-minute voice note or a paragraph — tied to a file and a commit. Over a year that's a living design doc. Claude + Mats can convert those into anti-patterns log entries, onboarding docs, or blog posts without you writing them twice.

### b. Shift from "only person who writes" to "person who reviews and teaches"

You're already the Architect in the Scout/Propose/Decide pattern. The more Claude+Mats scout and propose, the more your marginal hour goes to decisions and direction — which is higher-leverage than hands-on typing.

**Move:** treat AI-assisted modernization (mongoose migration, callback cleanup, CI fixes) as a productivity multiplier, not as something that reduces your scope. Your scope moves up, not down.

### c. Public surface

Right now, the platform's durability is invisible outside Boozang. "Framework I built in 2015 still runs production workloads in 2026" is a rare résumé line — and rarer as a talk or blog series. It's evidence of senior judgment in a way a coding challenge or FAANG title isn't.

**Move:** see §5.

---

## 4. Twelve-month strategic moves

Pick 2–3, not all 6.

| # | Move | Effort | Payoff |
|---|------|--------|--------|
| 1 | Lead Boozang's AI-native test generation (you're already on `ai-new`) | High | Core product + positions you as AI+QA expert |
| 2 | Open-source one piece — the console-bus framework or coop protocol | Medium | Public artifact; hiring/recruiting magnet |
| 3 | Speak at a test-automation or Node conference (TestBash, NodeConf, etc.) | Medium | Visibility; network; validates positioning |
| 4 | Write a "10 years of one framework" essay series | Low–Medium | Thought leadership; compounds over time |
| 5 | Codify the `.agent/` system (escalation levels, team roles) into a reusable pattern | Low | Positions you as an authority on AI+senior-eng collaboration |
| 6 | Formal principal-engineer competency framework for Boozang (self-assessed against a public ladder) | Low | Makes the next conversation — title, comp, or exit — legible |

Recommended combo if you can only pick two: **#1 + #3.** Lead the product's AI direction, and make that work visible externally.

---

## 5. Positioning options

Three realistic futures, not mutually exclusive.

### a. Principal / Staff Engineer at a larger company

Your skills compose well for Shopify, Datadog, Stripe, Cloudflare, Vercel — anywhere infrastructure reliability matters. The test-automation niche is a great story for a Developer Experience or Platform org.

**What's needed:** external signal. Right now your résumé reads "long tenure at one company." With a talk, an OSS project, or a published essay, it reads "long tenure building durable infrastructure — here's the receipts."

### b. CTO / Technical co-founder at Boozang

You arguably already are this. Making it official (title, equity clarity, visibility to customers) changes how prospects, hires, and investors see the company.

**What's needed:** this is a conversation with Mats. Surface it.

### c. Independent — consulting, advising, or a new product

Test automation + AI is an under-exploited wedge. You have both the technical depth and the production battle scars. Consulting at a principal-engineer hourly rate is realistic once public surface exists.

**What's needed:** external visibility (§5a) + a focused thesis (e.g. "reliable AI-driven QA for regulated industries").

---

## 6. Working with AI — lead, don't cede

The modernization work happening in `bz` right now (Mongoose upgrades, callback cleanup, CI fixes) used to be work only you could do. Now Claude + Mats can scout and propose most of it, and you decide.

This is **leverage**, not replacement. Three habits that keep it leverage:

1. **Stay ruthless about merge authority.** The codebase is the architect's source of truth. AI-generated code that doesn't match your style is noise — send it back.
2. **Use AI for the things that bored you.** Documentation generation, anti-patterns log entries, upgrade checklists, onboarding docs. Let it do the writing; you do the reviewing.
3. **Lead product AI features, don't just approve them.** `ai-new` is the most strategic branch in the repo. Own the architecture of how AI fits into the product — that's where the next moat is.

---

## 7. What to do next week

- **Pick two moves from §4.** Not six. Two.
- **Start the war-story habit.** Next time you fix a production issue, write two paragraphs: what broke, what you learned. File it under `.agent/memory/anti-patterns.md`. One entry this week.
- **Have the title conversation with Mats** (§5b). Whatever the answer, it clarifies the next 12 months.

---

*You built something that works. The next chapter is making the fact that it works — and why — visible to everyone who should know.*
