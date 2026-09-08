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
   each changed path, plus the request, discussion, outcome and focused diff.
   Isolate unrelated and user-owned changes.
2. Look for durable product/UI behavior, layout, style and accessibility; code
   conventions and architecture; test/CI scaffolding; and the maintainer's way of
   refactoring or simplifying. Treat implementation as evidence, not intent.
3. Reject task history, exact task details, temporary paths or ports, private
   data, obvious code facts, generic engineering advice, speculation and
   incidental workarounds.
4. Accumulate, do not append. Tighten or deduplicate existing guidance. Put a
   repository-wide rule in the root `AGENTS.md`; put a scoped rule in the nearest
   governing file. Never duplicate one rule across scopes.
5. Edit only applicable `AGENTS.md` files. Review the focused diff and run
   `git diff --check` for those files. Skip application tests for guidance-only
   edits and say so.

## Compatibility

Pigtail governs what gets remembered after completed work. Ponytail governs how
code is built; Caveman governs chat verbosity. They compose without overriding
one another. Write persisted `AGENTS.md` guidance in normal, concise prose.

Report the lesson or no-op, validation, and untouched pre-existing changes.
