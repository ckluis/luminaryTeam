# Luminary Planning

**v2.1** · A multi-agent technical and go-to-market review framework. Drop in your codebase, feature spec, architecture decision, landing page, or launch plan and get a structured audit from 40 domain-expert personas — each independent, each adversarial, each synthesized into actionable recommendations and, when you ask for one, a sequenced execution plan. The orchestrator echoes its version at the top of every audit, so transcripts are self-identifying.

---

## How It Works

Luminary runs a seven-phase protocol (Phase 0 – Phase 6) orchestrated by a neutral coordinator, with literal phase-gate lines so no phase can be silently skipped or merged — and a resume rule so truncated runs continue instead of restarting. Every claim must cite a specific artifact. No domain gets a pass for "nothing to report." Conflicts produce steelmanned debates, not silent compromise.

### Phase 0 — Intent Classification
Before the audit begins, the orchestrator classifies the target: what kind of artifact it is, which work dimensions (tags) it touches, which risk surfaces are live, and who the users / devices / locales are. It closes with an **evidence inventory** — what was actually provided vs. merely referenced — and a coverage statement, because verdicts bind only to evidence the members can see. Wrong classification here ripples through everything that follows, so ambiguity triggers a clarifying question rather than a guess.

### Phase 1 — Frame & Scope
The orchestrator restates the request, confirms the Phase 0 classification with the user (one correction window), and locks the roster. If the agent files aren't loaded, it writes a persona card per selected member so voices stay distinct. The reply ends here — the audit starts fresh in the next turn.

### Phase 2 — Independent Audit
Each member audits from their domain lens alone. Independence is literal: no member may reference or build on another's output. Every citation is a direct quote (≤20 words) plus its location — a bare line number is not a citation. Verdicts (PASS / CONCERNS / FAIL / INSUFFICIENT EVIDENCE) derive mechanically from each member's own findings, and each finding carries a proposed priority.

### Phase 3 — Red Flag Declaration
At most one blocking red flag per member — zero is fine when nothing blocks. Forced prioritization. Must cite quoted evidence, and every flag is a P0 claim: synthesis either accepts it as a P0 or downgrades it with documented reasoning. Categories: SECURITY, CORRECTNESS, DATA INTEGRITY, USER IMPACT, BUSINESS IMPACT, COMPLIANCE. A convergence audit follows — if the members all agree, that's a failure signal, and the orchestrator forces the two most opposed lenses to clash anyway.

### Phase 4 — Adversarial Clash
Members with conflicting positions debate directly. The steelman rule is enforced: you must argue the opponent's position charitably before your rebuttal — skipping it disqualifies the rebuttal. Clash is bounded to two exchanges per conflict; unresolved conflicts escalate to an orchestrator ruling with the dissent recorded verbatim. Members excluded from the initial roster may be pulled in mid-clash if the conflict touches their domain.

### Phase 5 — Synthesis
Opens with a citation-verification pass (fabricated or misplaced quotes get findings downgraded to UNVERIFIED — they cannot block) and a per-member scoreboard so runs are comparable. Then the orchestrator resolves conflicts into a structured recommendation matrix with final priorities, clear owners, and verification paths. When you asked for a plan, Phase 5b converts the matrix into sequenced workstreams with milestones and dependencies — without reopening any decision.

### Phase 6 — Iteration
Drill in on any finding. Request re-audits. Re-audits follow a delta contract: only changed artifacts get re-checked, each finding transitions explicitly (RESOLVED / REGRESSED / UNCHANGED / WITHDRAWN), and only the member who declared a red flag can clear it — by citing the artifact that resolves it.

---

## Priority Levels

| Level | Label | Meaning |
|---|---|---|
| **P0** | BLOCKER | Unsafe, incorrect, or irreversible. Work stops until resolved. |
| **P1** | CRITICAL | Significant risk. Deferral requires orchestrator approval + documented rationale. |
| **P2** | IMPORTANT | Quality/robustness gain. Defer to next phase with a tracked ticket and an owner. |
| **P3** | IMPROVEMENT | Non-blocking enhancement. Future work. |

Members *propose* a priority with each finding; the orchestrator assigns the *final* priority in synthesis and must document every downgrade of a proposed P0/P1. P0 has a litmus test — a concrete, named harm that is irreversible, unsafe, or produces incorrect output to users. "Could be bad" is never P0.

---

## The 40-Member Roster

Each agent brings a specific domain, a defined personality, explicit conflict vectors, and a signature challenge question. Phase 0 picks the 5–10 relevant to your audit — you don't need all 40 every time.

### Systems & Engineering
| Agent | Domain | Core Focus |
|---|---|---|
| **Linus Torvalds** | Architecture & Maintainability | Modularity, justified complexity, no premature generalization |
| **John Carmack** | Performance & Optimization | Hot paths, memory layout, O(n) analysis — benchmarks not intuitions |
| **Grace Jansen** | Developer Experience & Tooling | Onboarding, readable code, useful errors, docs without tribal knowledge |
| **Arnauld Lauret** | API Design & Governance | Interface consistency, naming coherence, RFC correctness |
| **Martin Kleppmann** | Distributed Systems & Data | Event sourcing, consistency, idempotency, replication |
| **Eric Evans** | Domain Modeling | Bounded contexts, ubiquitous language, aggregate design |
| **Alex Russell** | Web Performance & Frontend Platform | JS payload, Core Web Vitals, real-device performance discipline |

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
| **Val Head** | Interface Motion Design | Easing, choreography, `prefers-reduced-motion`, functional vs. decorative |
| **John Yunker** | Localization & Global Design | i18n architecture, l10n quality, global gateway, cultural assumptions |
| **Daniele Procida** | Technical Writing & Docs Architecture | Diátaxis: tutorial, how-to, reference, explanation — kept distinct |

### Data, Analytics & AI
| Agent | Domain | Core Focus |
|---|---|---|
| **Joe Celko** | SQL & Data Modeling | Schema correctness, normalization, NULL semantics, query performance |
| **Ralph Kimball** | Dimensional Modeling & Data Warehousing | Fact/dimension tables, grain discipline, SCD strategy, conformed dimensions |
| **Edward Tufte** | Data Visualization | Data-ink ratio, chartjunk, information density, whether viz encodes truth |
| **Hadley Wickham** | Data Science & Analytics | Tidy data, pipeline reproducibility, grammar of graphics |
| **Andrew Gelman** | Statistical Rigor | Metrics validity, A/B test power, false positive rates, overconfident inference |
| **Andrej Karpathy** | AI/ML & LLM Integration | Prompt injection, model evaluation, hallucination failure modes |

### Safety & Governance
| Agent | Domain | Core Focus |
|---|---|---|
| **James Bach** | Testing & QA Strategy | Whether tests find real bugs — not coverage, not CI green |
| **Bruce Schneier** | Security & Threat Modeling | Crypto correctness, auth/authz, secrets management, threat models |
| **Charity Majors** | Infrastructure, Observability & Production Reliability | Deployment pipelines, structured telemetry, SLOs, incident debuggability |
| **John Allspaw** | Resilience & Safety Engineering | Adaptive capacity, near-miss analysis, how systems fail under pressure |
| **Marcy Sutton** | Accessibility | WCAG compliance, keyboard nav, screen reader semantics, focus management |
| **Kat Holmes** | Inclusive Design | Mismatch between human ability and product assumption; "solve for one, extend to many" |
| **Ann Cavoukian** | Privacy & Data Governance | Privacy by Design, data minimization, PII handling, retention policy |
| **Timnit Gebru** | Responsible AI & Algorithmic Harm | Disparate impact, training data provenance, model cards, subgroup performance |
| **Heather Meeker** | Open-Source Licensing & IP | License compatibility, SBOMs, model/dataset terms, trademark use |

### Marketing, Brand & Community
| Agent | Domain | Core Focus |
|---|---|---|
| **David Ogilvy** | Advertising & Brand Copywriting | Headline craft, specific promises, research-led persuasion |
| **Seth Godin** | Marketing Strategy & Permission | Remarkable products, smallest viable audience, permission over interruption |
| **April Dunford** | Positioning & Go-to-Market | Best-at-something-for-somebody, competitive alternatives, sales narrative |
| **Madhavan Ramanujam** | Pricing & Monetization Strategy | Willingness-to-pay before building, value metrics, packaging, monetization failure modes |
| **Ann Handley** | Content Marketing & Business Writing | Reader-first writing, voice consistency, useful-before-promotional |
| **Rory Sutherland** | Behavioral Marketing & Persuasion | Framing, signaling, perception engineering, irrational-but-real drivers |
| **Paula Scher** | Brand Identity Design | Logotype, mark, color system, identity coherence across surfaces |
| **Shawn Wang (Swyx)** | Developer Relations & Community | First-run experience, public signal, DevRel loops into product |

---

## Usage

Luminary is designed to work in any LLM chat or Claude project that supports large context. There are four ways to invoke it, from lowest to highest ceremony.

### 1. Default invocation — full Phase 0 audit

Paste `luminaryPrompt.md` as your system or first message. Then paste the target (codebase, spec, landing page, etc.) with your ask. The orchestrator runs Phase 0 intent classification, selects the relevant 5–10 members, and runs the full protocol.

```
System:  [paste luminaryPrompt.md]
User:    [paste target]
         Audit this feature spec for our new billing engine.
```

### 2. Invocation modes — start with a preset roster

Prefix your first message with a mode. The mode sets the *starting* roster; Phase 0 still runs and can add members based on declared risk surfaces. Modes never silently drop members — they only shape where selection begins.

```
/luminaryReview                  default — full Phase 0 selection
/luminaryReview:architecture     Torvalds, Evans, Kleppmann, Carmack, Lauret, Majors, Allspaw
/luminaryReview:perf             Carmack, Russell, Majors, Bach
/luminaryReview:design           Norman, Zhuo, Butterick, Scher, Head, Morville, Holmes
/luminaryReview:microcopy        Podmajersky, Handley, Ogilvy, Norman
/luminaryReview:ai               Karpathy, Gebru, Schneier, Bach, Gelman
/luminaryReview:global           Yunker, Holmes, Podmajersky, Sutton, Zhuo, Dunford
/luminaryReview:security         Schneier, Cavoukian, Meeker, Bach, Allspaw
/luminaryReview:marketing        Ogilvy, Godin, Dunford, Handley, Sutherland
/luminaryReview:pricing          Ramanujam, Dunford, Torres, Sutherland
/luminaryReview:full             All 40 members, in panels of ≤8
```

Equivalent syntaxes: `/luminaryReview:mode` or `/luminaryReview mode` (start or end of your first message), or `mode: mode` (start only). The space form counts only when the name matches a listed mode or alias. Combine modes with `+` (e.g., `architecture+data`). Aliases: `llm`→`ai`, `l10n`/`i18n`→`global`, `content`→`copy`. See the full mode list in `<invocation_modes>` inside `luminaryPrompt.md`.

```
System:  [paste luminaryPrompt.md]
User:    /luminaryReview:design

         Review our onboarding flow. [paste artifacts]
```

### 3. Single agent — focused one-domain review

Load a specific `agent*.md` file without the orchestrator. Useful when you know the problem domain but want a rigorous single-lens critique. Every agent file carries a standalone rule: loaded without the orchestrator, it runs a complete solo audit at the same evidence bar (quoted citations), skipping only the clash step.

```
System:  [paste agentBruceSchneier.md]
User:    Audit this auth implementation.
```

### 4. Custom roster — hand-picked team

Paste `luminaryPrompt.md` plus the specific `agent*.md` files you want. In your first message, instruct: `use only these members: [names]`. Phase 0 still runs over the constrained roster.

---

### Feeding the target

The audit is only as good as the evidence the members can see, and the protocol refuses to grade what it wasn't shown (Phase 0.7 evidence inventory + the INSUFFICIENT EVIDENCE verdict).

- **Prefer whole artifacts over summaries.** A described feature gets EVIDENCE-LIMITED citations; a pasted one gets real ones.
- **Large codebases:** paste the entry points, the module under review, and its direct dependencies. List the remaining file paths so the inventory can mark them REFERENCED-NOT-PROVIDED instead of members guessing.
- **Very large targets:** the orchestrator will propose a chunk plan in Phase 1 (by module / page / surface) and audit chunk by chunk with one synthesis at the end.

---

### Which should I use?

- **I know broadly what kind of review I want** (architecture, marketing, design, etc.) → **invocation mode**
- **I want the orchestrator to figure it out from the artifact** → **default**
- **I want one specific expert's take** → **single agent**
- **I know exactly who I want** → **custom roster**

---

## Protocol Rules

- **Phase 0 required** — intent classification runs before any audit. Ambiguity triggers a question, not a guess.
- **Cite or retract** — a citation is a direct quote (≤20 words) plus its location; anything less is inadmissible. P0/P1 citations get re-verified at synthesis.
- **Distinct voices enforced** — members stay in character; interchangeable members are an orchestrator failure. The value is the friction between real perspectives.
- **Steelman enforced** — in adversarial clash, you argue the opponent's position before your rebuttal
- **Bounded clash** — two exchanges per conflict, then the orchestrator rules and records the dissent verbatim
- **One red flag maximum** — at most one per member per audit cycle; zero is fine when nothing blocks (forces real prioritization)
- **No silent pass** — "nothing to report" requires active investigation of edge cases
- **No verdicts on unseen material** — domains whose artifacts weren't provided return INSUFFICIENT EVIDENCE, never PASS
- **Positions move on evidence, not pressure** — user pushback never softens a finding; an overruled P0/P1 is recorded as overruled, risk standing as written
- **Output is budgeted** — capped findings per member, batched delivery for big rosters, panels for `full` mode. A truncated audit is a failed audit.
- **Orchestrator stays neutral** — mediates process and resolves deadlock, never takes domain positions
- **Synthesis is actionable** — every recommendation gets an owner and a verification path
- **Excluded members can be pulled in** — if a conflict surfaces a domain the orchestrator didn't select, the relevant member joins the clash

---

## File Structure

```
luminaryProcess/
├── README.md                  # This file
├── CHANGELOG.md               # Version history (the prompt echoes its version in Phase 0)
├── LICENSE
├── index.html                 # GitHub Pages site (ckluis.github.io/luminaryTeam)
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
├── agentJohnYunker.md          # Localization & global design
└── agentMadhavanRamanujam.md   # Pricing & monetization strategy
```

---

## Conflict Map

Some members reliably clash. These tensions are features, not bugs — they surface real trade-offs.

### Classic tensions
- **Carmack vs. Evans** — Performance optimization vs. domain model purity
- **Jobs vs. Bach** — Ship great things fast vs. prove nothing is broken first
- **Kleppmann vs. Torvalds** — Embrace distributed complexity vs. keep it simple and modular
- **Norman vs. Torvalds** — Mental models baked into the architecture vs. interfaces that expose real system complexity
- **Schneier vs. Karpathy** — Deterministic threat models vs. probabilistic LLM failure modes
- **Schneier vs. Carmack** — Validation on every path vs. measured hot-path latency
- **Cavoukian vs. Majors** — Data minimization vs. instrument everything for observability
- **Cavoukian vs. Kleppmann** — Data minimization and retention limits vs. immutable event logs
- **Torvalds vs. Sutton** — "It's a developer tool" vs. developers also have disabilities
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
- **Russell vs. Jansen** — Shipped JS cost vs. developer experience conveniences
- **Head vs. Sutton** — Expressive motion vs. vestibular/`prefers-reduced-motion` safety
- **Head vs. Holmes** — Motion as the comprehension layer vs. motion as an exclusion risk
- **Meeker vs. Torvalds** — License-text compliance vs. pragmatism
- **Scher vs. Zhuo** — Brand identity point of view vs. product UI system neutrality
- **Holmes vs. Sutton** — Inclusive design as practice vs. WCAG as compliance floor
- **Holmes vs. Zhuo** — Accommodating mismatch at the edges vs. design-system consistency in the middle
- **Majors vs. Schneier** — High-cardinality telemetry as visibility vs. telemetry as exfiltration surface
- **Gebru vs. Schneier** — Collecting demographic data to audit fairness vs. the audit dataset as breach blast radius
- **Yunker vs. Dunford** — Per-market positioning vs. US-default GTM translated outward
- **Procida vs. Handley** — Reference docs must not narrate vs. content-first voice
- **Swyx vs. Ogilvy** — Developer community loops vs. classical persuasive advertising
- **Swyx vs. Jansen** — Learn-in-public community momentum vs. the first-run experience actually working
- **Ramanujam vs. Dunford** — Willingness-to-pay evidence leading vs. positioning decided before price
- **Ramanujam vs. Jobs** — Value-metric segmentation vs. one beautiful price

The lists above are the headline pairings, not the whole graph. The complete conflict graph lives in the agent files' Conflict Vectors — every "Will fight X when…" line is a scripted Phase 4 clash, and members respond in-domain even to challenges their own file doesn't list.

---

## What It's Not

Luminary is not a replacement for human judgment. It's a forcing function — a structured way to ensure the right questions get asked before decisions get made. The synthesis is a starting point for your team's conversation, not the end of it.
