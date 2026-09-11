# Repository Rules

This repository contains reusable Agent Skills for desktop application development.

## Structure

Public skills must live under:

```text
skills/<skill-name>/
```

A skill may contain:

```text
skills/<skill-name>/
├── SKILL.md
├── references/   # optional detailed guidance
├── scripts/      # optional deterministic helpers
└── assets/       # optional templates or static resources
```

## Skill boundaries

- Each skill must be independently understandable and installable.
- Do not create runtime dependencies from a skill to repository-level `docs/` files.
- Keep references, scripts, and assets required by a skill inside that skill directory.
- Avoid shared runtime files between skills unless a concrete need proves that duplication is worse than coupling.
- Prefer complete reusable capabilities over small component-level micro-skills.
- Do not tie generic skills to a single agent, framework, language, or product unless the skill is explicitly technology-specific.

## Naming

- Skill directory names use lowercase kebab-case.
- The `name` in `SKILL.md` frontmatter must match the skill directory name.
- Names should describe a capability, not an implementation detail.

## Authoring

- Keep `SKILL.md` focused on trigger conditions, workflow, decisions, and completion criteria.
- Put detailed knowledge, checklists, examples, and background material in `references/` when needed.
- Use `scripts/` only when deterministic automation provides clear value.
- Use `assets/` for reusable templates or static files, not general documentation.
- Avoid placeholder behavior in a published skill.
- Define observable completion gates for workflows that produce or modify artifacts.

## Repository-level files

- `docs/` documents this repository itself; it is not part of an installed skill's runtime contract.
- Do not add top-level directories preemptively. Add them only when they have a real use case.
- Do not add agent-specific mirrors such as `.claude/skills/` or `.agents/skills/` to this source repository unless there is a demonstrated compatibility requirement.

## Current state

The repository structure is initialized, but no skill is implemented yet. Do not create a `SKILL.md` unless the task explicitly requires implementing a skill.
