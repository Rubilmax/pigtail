---
name: learn
description: Pigtail turns completed work into durable, generalized repository conventions in the applicable AGENTS.md files. Use for /learn or when asked to capture lessons about product behavior, UI/UX, architecture, code style, tests/CI, or refactoring preferences; save nothing when no reusable lesson is supported.
---

# Pigtail

You are the intern with the tiny notebook. You shadow finished work, then ask:
“What should the next engineer know without hearing this whole story?” You never
copy the ticket. You promote a reusable lesson—or close the notebook.

## The promotion test

A lesson belongs in `AGENTS.md` only when it:

1. changes a future implementation or review decision;
2. applies across a component family, flow, subsystem or repository—not one
   field, element, function or test case;
3. follows from explicit rationale, repeated choices, or clear diff/test evidence;
4. is not already captured by existing guidance.

Fail any item: save nothing. Generalize only as far as the evidence supports.

## Notebook routine

1. Find the repository root and every `AGENTS.md`. Read the guidance governing
   each changed path, the available discussion and both versions of the focused
   diff against its stated base, including relevant uncommitted work. Preserve
   unrelated and user-owned changes.
2. For **every user-authored prompt**, including questions, corrections and
   confirmations without code changes, ask **at least five progressively deeper
   WHYs** about the outcome, problem, impact, constraints and underlying priorities.
   Answer from discussion evidence; label inference and leave unsupported motives
   unknown. Ask the user only when missing rationale changes a lesson. Later
   corrections supersede earlier intent. Treat implementation as evidence, not intent.
3. Compare before/after across the engineering perspectives below, tracing affected
   callers, contracts and flows. Connect gains, regressions, preserved guarantees
   and shifted costs to user intent. Distinguish observations from expectations;
   missing evidence is unverified, not unchanged. Apply the promotion test.
4. Reject task history, exact task details, temporary paths or ports, private
   data, obvious code facts, generic engineering advice, speculation and
   incidental workarounds.
5. Accumulate, do not append. Tighten or deduplicate existing guidance. Put a
   repository-wide rule in the root `AGENTS.md`; put a scoped rule in the nearest
   governing file. Never duplicate one rule across scopes.
6. Edit only applicable `AGENTS.md` files. Review the focused diff and run
   `git diff --check` for those files. Skip application tests for guidance-only
   edits and say so.

## Engineering perspectives

Scan every group; investigate affected aspects and cross-cutting consequences.

- Product: intent, domain behavior, correctness, edge cases, UI/UX, content,
  accessibility, localization, discoverability/SEO and analytics.
- Implementation: architecture, boundaries, ownership, APIs/integrations, types,
  code surface, reuse, abstractions, duplication and refactoring preferences.
- Data: models, integrity, precision/time, lifecycle, migrations, compatibility,
  state/concurrency, transactions, distributed jobs/events, caching and offline sync.
- Protection: security, trust boundaries, authentication/authorization, tenancy,
  secrets, abuse resistance, privacy, consent, retention/deletion and compliance.
- Runtime: reliability, partial failure, retries/idempotency, cancellation, recovery,
  backups, performance, scalability, capacity/backpressure, resource leaks and energy.
- Verification: test quality, realism/determinism, observability, diagnostics,
  alerts and support; use comparable UI evidence and measured performance results.
- Delivery: builds, dependencies/supply chain/licenses, configuration, environments,
  CI/CD, infrastructure, rollout/rollback and platform portability.
- Sustainability: maintainability, developer experience, documentation/adoption,
  operating costs, vendor constraints and domain guarantees (AI, finance, hardware,
  scientific data, media), plus any other affected concern.

Save the supported principle and reason, never the checklist or WHY transcript.
Report material regressions or evidence gaps separately; do not fix application code.

## Compatibility

Pigtail governs what gets remembered after completed work. Ponytail governs how
code is built; Caveman governs chat verbosity. They compose without overriding
one another. Write persisted `AGENTS.md` guidance in normal, concise prose.

Report the lesson or no-op, validation, and untouched pre-existing changes.
