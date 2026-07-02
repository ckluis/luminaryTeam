# Changelog

The orchestrator echoes its version at the top of every Phase 0 output (`Luminary v2.1 — mode: …`), so any transcript can be traced back to the protocol that produced it. Bump the version on any protocol or roster change.

## v2.1 — 2026-07-02

Hardening release. Protocol enforcement against the failure modes of single-context multi-persona runs, plus one roster addition.

**Protocol**
- Phase 0.7 EVIDENCE INVENTORY + coverage statement; new INSUFFICIENT EVIDENCE verdict; rule 14: never PASS on unseen material.
- Persona fallback: when agent files aren't loaded, the orchestrator writes binding persona cards for the selected roster (fixes voice convergence in prompt-only runs).
- Citation format (direct quote ≤20 words + location) and a Phase 5 citation-verification pass; fabricated citations downgrade findings to UNVERIFIED.
- Phase 3.5 CONVERGENCE AUDIT (anti-groupthink gate); Phase 2 independence made literal.
- Phase 4 clash bounded to two exchanges, then orchestrator ruling with dissent recorded; conflict vectors declared triggers, not permission lists.
- Verdicts (PASS/CONCERNS/FAIL) defined mechanically from findings; members propose P0–P3 priorities, orchestrator assigns finals with documented downgrades; red flags formally linked to P0.
- Phase 5 opens with a per-member scoreboard; OPEN RED FLAGS section added; Phase 5b PLAN ASSEMBLY produces a sequenced plan when one was asked for.
- Phase 6 re-audit delta contract (scope, transitions, red-flag clearance).
- Phase gates + resume protocol (no silent phase skipping; truncated runs continue, never restart).
- `<target_intake>`, `<output_budget>` (batching, `full`-mode panels, chunk plans), `<minimum_viable_run>` blocks.
- Rule 13 (positions move on evidence, not user pressure) and BUSINESS IMPACT red-flag category with definitions for all six categories.
- Invocation detection rule fixed (start-or-end token, space form covered); `perf` and `pricing` modes; `llm`/`l10n`/`i18n`/`content` aliases; tag map declared the single source of truth for Phase 0.5 pulls; Majors added to the `safety` tag.

**Roster**
- \#40 Madhavan Ramanujam — Pricing & Monetization Strategy (`pricing`, `monetization`, `gtm`), with a pricing hard pull and reciprocal conflict vectors (Dunford, Jobs, Godin).
- Agent files: broadened Protocol boilerplate (any product artifact + standalone mode), verdict/priority/citation upgrades in Audit Output, reciprocal conflict vectors back-filled (Carmack↔Evans, Jobs↔Bach fight lines, inbound edges for the eight previously unreachable members, Holmes↔Zhuo, Head↔Holmes, Schneier↔Gebru, Majors↔Schneier), Handley's generic vector retargeted, Zhuo/Sutton duplicate trigger resolved, Jansen naming convention (was bare "Grace").

**Docs/site**
- README and index.html synced: 40 members, shared roster grouping, full mode list, corrected conflict map, "Feeding the target" guide, file tree completed, version stamps.

## v2.0 — 2025-04

- Roster expanded to 39 agents; Phase 0 intent classification; invocation modes as universal text conventions.

## v1.0 — 2025-04

- Initial release: 19-expert review framework with independent audit, red flags, adversarial clash, and synthesis.
