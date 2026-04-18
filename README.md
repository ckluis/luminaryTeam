# Luminary Planning

A multi-agent technical and go-to-market review framework. Drop in your codebase, feature spec, architecture decision, landing page, or launch plan and get a structured audit from 39 domain-expert personas — each independent, each adversarial, each synthesized into actionable recommendations.

---

## How It Works

Luminary runs a seven-phase protocol (Phase 0 – Phase 6) orchestrated by a neutral coordinator. Every claim must cite a specific artifact. No domain gets a pass for "nothing to report." Conflicts produce steelmanned debates, not silent compromise.

### Phase 0 — Intent Classification
Before the audit begins, the orchestrator classifies the target: what kind of artifact it is, which work dimensions (tags) it touches, which risk surfaces are live, and who the users / devices / locales are. Wrong classification here ripples through everything that follows, so ambiguity triggers a clarifying question rather than a guess.

### Phase 1 — Frame & Scope
The orchestrator restates the request, confirms the Phase 0 classification with the user (one correction window), and locks the roster.

### Phase 2 — Independent Audit
Each member audits from their domain lens alone. No cross-member coordination. No groupthink.

### Phase 3 — Red Flag Declaration
One blocking red flag per member, maximum. Forced prioritization. Must cite evidence.

### Phase 4 — Adversarial Clash
Members with conflicting positions debate directly. The steelman rule is enforced: you must argue the opponent's position charitably before your rebuttal — skipping it disqualifies the rebuttal. Members excluded from the initial roster may be pulled in mid-clash if the conflict touches their domain.

### Phase 5 — Synthesis
The orchestrator resolves conflicts into a structured recommendation matrix with clear owners and verification paths.

### Phase 6 — Iteration
Drill in on any finding. Request re-audits. Ask members to respond to new information.

---

## Priority Levels

| Level | Label | Meaning |
|---|---|---|
| **P0** | BLOCKER | Unsafe, incorrect, or irreversible. Work stops until resolved. |
| **P1** | CRITICAL | Significant risk. Deferral requires orchestrator approval + documented rationale. |
| **P2** | IMPORTANT | Quality/robustness gain. Defer to next phase with a tracked ticket. |
| **P3** | IMPROVEMENT | Non-blocking enhancement. Future work. |

---

## The 39-Member Roster

Each agent brings a specific domain, a defined personality, explicit conflict vectors, and a signature challenge question. Phase 0 picks the 5–10 relevant to your audit — you don't need all 39 every time.

### Engineering & Systems
| Agent | Domain | Core Focus |
|---|---|---|
| **Linus Torvalds** | Architecture & Maintainability | Modularity, justified complexity, no premature generalization |
| **John Carmack** | Performance & Optimization | Hot paths, memory layout, O(n) analysis — benchmarks not intuitions |
| **Grace Jansen** | Developer Experience & Tooling | Onboarding, readable code, useful errors, docs without tribal knowledge |
| **Arnauld Lauret** | API Design & Governance | Interface consistency, naming coherence, RFC correctness |
| **Alex Russell** | Web Performance & Frontend Platform | JS payload, Core Web Vitals, real-device performance discipline |
| **Charity Majors** | Infrastructure & Observability | Deployment pipelines, structured telemetry, SLOs, incident debuggability |
| **John Allspaw** | Resilience & Safety Engineering | Adaptive capacity, near-miss analysis, how systems fail under pressure |
| **James Bach** | Testing & QA Strategy | Whether tests find real bugs — not coverage, not CI green |
| **Bruce Schneier** | Security & Threat Modeling | Crypto correctness, auth/authz, secrets management, threat models |
| **Heather Meeker** | Open-Source Licensing & IP | License compatibility, SBOMs, model/dataset terms, trademark use |

### Product & Design
| Agent | Domain | Core Focus |
|---|---|---|
| **Steve Jobs** | Product Quality & Customer Experience | Whether it's genuinely great — not feature-complete, but inevitable |
| **Teresa Torres** | Product Discovery & Continuous Research | Opportunity-solution trees, outcomes over outputs, assumption testing |
| **Don Norman** | UX & Interaction Design | Mental models, affordance, feedback loops, error recovery |
| **Julie Zhuo** | UI & Visual Design Systems | Visual hierarchy, component consistency, design token discipline |
| **Peter Morville** | Information Architecture | Taxonomy, labeling, navigation, findability |
| **Torrey Podmajersky** | UX Writing & Microcopy | Interface voice, error messages, empty states, destructive-action clarity |
| **Matthew Butterick** | Typography | Type scale, measure, rhythm, reading flow |
| **Paula Scher** | Brand Identity Design | Logotype, mark, color system, identity coherence across surfaces |
| **Val Head** | Interface Motion Design | Easing, choreography, `prefers-reduced-motion`, functional vs. decorative |
| **Marcy Sutton** | Accessibility | WCAG compliance, keyboard nav, screen reader semantics, focus management |
| **Kat Holmes** | Inclusive Design | Mismatch between human ability and product assumption; "solve for one, extend to many" |
| **John Yunker** | Localization & Global Design | i18n architecture, l10n quality, global gateway, cultural assumptions |

### Data, Analytics & AI
| Agent | Domain | Core Focus |
|---|---|---|
| **Joe Celko** | SQL & Data Modeling | Schema correctness, normalization, NULL semantics, query performance |
| **Martin Kleppmann** | Distributed Systems & Data | Event sourcing, consistency, idempotency, replication |
| **Eric Evans** | Domain Modeling | Bounded contexts, ubiquitous language, aggregate design |
| **Ralph Kimball** | Dimensional Modeling & Data Warehousing | Fact/dimension tables, grain discipline, SCD strategy, conformed dimensions |
| **Edward Tufte** | Data Visualization | Data-ink ratio, chartjunk, information density, whether viz encodes truth |
| **Hadley Wickham** | Data Science & Analytics | Tidy data, pipeline reproducibility, grammar of graphics |
| **Andrew Gelman** | Statistical Rigor | Metrics validity, A/B test power, false positive rates, overconfident inference |
| **Andrej Karpathy** | AI/ML & LLM Integration | Prompt injection, model evaluation, hallucination failure modes |
| **Timnit Gebru** | Responsible AI & Algorithmic Harm | Disparate impact, training data provenance, model cards, subgroup performance |

### Governance & Compliance
| Agent | Domain | Core Focus |
|---|---|---|
| **Ann Cavoukian** | Privacy & Data Governance | Privacy by Design, data minimization, PII handling, retention policy |

### Marketing, Brand & Community
| Agent | Domain | Core Focus |
|---|---|---|
| **David Ogilvy** | Advertising & Brand Copywriting | Headline craft, specific promises, research-led persuasion |
| **Seth Godin** | Marketing Strategy & Permission | Remarkable products, smallest viable audience, permission over interruption |
| **April Dunford** | Positioning & Go-to-Market | Best-at-something-for-somebody, competitive alternatives, sales narrative |
| **Ann Handley** | Content Marketing & Business Writing | Reader-first writing, voice consistency, useful-before-promotional |
| **Rory Sutherland** | Behavioral Marketing & Persuasion | Framing, signaling, perception engineering, irrational-but-real drivers |
| **Shawn Wang (Swyx)** | Developer Relations & Community | First-run experience, public signal, DevRel loops into product |
| **Daniele Procida** | Technical Writing & Docs Architecture | Diátaxis: tutorial, how-to, reference, explanation — kept distinct |

---

## Usage

### Option A — Full Team Audit
Paste the `luminaryPrompt.md` into a Claude project (or any LLM with large context). Include your codebase, spec, or architecture doc. The orchestrator runs Phase 0 (intent classification), selects the relevant subset, and runs the protocol.

### Option B — Single Agent
Load a specific `agent*.md` file for a focused single-domain review. Useful when you know the problem domain but want structured, rigorous feedback from that lens.

### Option C — Custom Roster
Select 3–7 agents whose domains cover your highest-risk areas. Paste `luminaryPrompt.md` plus the selected agent files. Specify "use only these members" in your prompt. (Phase 0 will still run on the classification — just constrained to your picks.)

---

## Protocol Rules

- **Phase 0 required** — intent classification runs before any audit. Ambiguity triggers a question, not a guess.
- **Cite or retract** — any claim without a specific code/spec artifact reference is inadmissible
- **Steelman enforced** — in adversarial clash, you argue the opponent's position before your rebuttal
- **One red flag maximum** — per member per audit cycle (forces real prioritization)
- **No silent pass** — "nothing to report" requires active investigation of edge cases
- **Orchestrator stays neutral** — mediates process and resolves deadlock, never takes domain positions
- **Synthesis is actionable** — every recommendation gets an owner and a verification path
- **Excluded members can be pulled in** — if a conflict surfaces a domain the orchestrator didn't select, the relevant member joins the clash

---

## File Structure

```
luminaryProcess/
├── luminaryPrompt.md          # Master orchestrator + protocol (includes Phase 0)
├── agentLinusTorvalds.md
├── agentJohnCarmack.md
├── agentGraceJansen.md
├── agentArnauldLauret.md
├── agentDonNorman.md
├── agentJulieZhuo.md
├── agentJoeCelko.md
├── agentMartinKleppmann.md
├── agentEricEvans.md
├── agentSteveJobs.md
├── agentJamesBach.md
├── agentBruceSchneier.md
├── agentAndrejKarpathy.md
├── agentCharityMajors.md
├── agentMarcySutton.md
├── agentAnnCavoukian.md
├── agentEdwardTufte.md
├── agentHadleyWickham.md
├── agentAndrewGelman.md
├── agentDavidOgilvy.md
├── agentSethGodin.md
├── agentAprilDunford.md
├── agentAnnHandley.md
├── agentRorySutherland.md
├── agentTorreyPodmajersky.md   # UX writing & microcopy
├── agentRalphKimball.md        # Dimensional modeling & warehousing
├── agentMatthewButterick.md    # Typography
├── agentPeterMorville.md       # Information architecture
├── agentTeresaTorres.md        # Product discovery
├── agentJohnAllspaw.md         # Resilience & safety engineering
├── agentTimnitGebru.md         # Responsible AI & algorithmic harm
├── agentAlexRussell.md         # Web performance & frontend platform
├── agentDanieleProcida.md      # Docs architecture (Diátaxis)
├── agentKatHolmes.md           # Inclusive design
├── agentValHead.md             # Motion design
├── agentHeatherMeeker.md       # OSS licensing & IP
├── agentPaulaScher.md          # Brand identity
├── agentShawnWang.md           # Developer relations & community
└── agentJohnYunker.md          # Localization & global design
```

---

## Conflict Map

Some members reliably clash. These tensions are features, not bugs — they surface real trade-offs.

### Classic tensions
- **Carmack vs. Evans** — Performance optimization vs. domain model purity
- **Jobs vs. Bach** — Ship great things fast vs. prove nothing is broken first
- **Kleppmann vs. Torvalds** — Embrace distributed complexity vs. keep it simple and modular
- **Schneier vs. Karpathy** — Deterministic threat models vs. probabilistic LLM failure modes
- **Cavoukian vs. Majors** — Data minimization vs. instrument everything for observability
- **Ogilvy vs. Godin** — Classical persuasion at scale vs. remarkable products that earn permission
- **Dunford vs. Ogilvy** — Crisp positioning first vs. great copy leading the work
- **Sutherland vs. Gelman** — Psycho-logic and perception vs. measurable statistical rigor
- **Handley vs. Ogilvy** — Useful-before-promotional vs. persuasion-first selling
- **Godin vs. Jobs** — Deliberately build a tribe/permission asset vs. assume a great product markets itself

### New tensions from the expanded roster
- **Podmajersky vs. Ogilvy** — In-product helpful voice vs. persuasive advertising voice
- **Kimball vs. Celko** — Dimensional denormalization for analytics vs. 3NF discipline
- **Butterick vs. Zhuo** — Typographic craft vs. design-system token scale
- **Morville vs. Norman** — Structural IA fixes vs. interaction-level fixes
- **Torres vs. Jobs** — Evidence-led discovery vs. visionary product taste
- **Allspaw vs. Majors** — Adaptive capacity and human recovery vs. telemetry-first reliability
- **Gebru vs. Karpathy** — Deployment harm on named populations vs. benchmark-led capability
- **Gebru vs. Cavoukian** — Collecting demographic data to audit fairness vs. data minimization
- **Russell vs. Carmack** — Web payload and real-device performance vs. backend/CPU hot-path focus
- **Russell vs. Grace** — Shipped JS cost vs. developer experience conveniences
- **Head vs. Sutton** — Expressive motion vs. vestibular/`prefers-reduced-motion` safety
- **Meeker vs. Torvalds** — License-text compliance vs. pragmatism
- **Scher vs. Zhuo** — Brand identity point of view vs. product UI system neutrality
- **Holmes vs. Sutton** — Inclusive design as practice vs. WCAG as compliance floor
- **Yunker vs. Dunford** — Per-market positioning vs. US-default GTM translated outward
- **Procida vs. Handley** — Reference docs must not narrate vs. content-first voice
- **Swyx vs. Ogilvy** — Developer community loops vs. classical persuasive advertising

---

## What It's Not

Luminary is not a replacement for human judgment. It's a forcing function — a structured way to ensure the right questions get asked before decisions get made. The synthesis is a starting point for your team's conversation, not the end of it.
