# Pigtail

> The intern with the tiny notebook: learn the pattern, not the ticket.

Pigtail is a portable Codex skill that reviews completed work and promotes only
durable, generalized lessons into the current repository's applicable
`AGENTS.md` files. It can learn product and UI conventions, architecture and code
style, test/CI scaffolding, and a maintainer's refactoring or simplification
preferences. When no lesson clears that bar, it writes nothing.

The skill is branded **Pigtail** but named `learn`, so its command remains
`/learn` (or `$learn`).

## Install

Link `skills/learn` into the Codex skills directory as `learn`:

```sh
ln -s /path/to/pigtail/skills/learn ~/.codex/skills/learn
```

## Compatibility

Pigtail works alone or beside Ponytail and Caveman. Ponytail governs how code is
built, Caveman governs chat brevity, and Pigtail governs what is remembered after
the work. It does not activate, disable, or override either mode, and it keeps
persisted `AGENTS.md` guidance in normal prose.

## Layout

```text
skills/learn/SKILL.md
skills/learn/agents/openai.yaml
```
