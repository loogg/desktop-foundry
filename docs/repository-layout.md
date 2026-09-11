# Repository Layout

This document defines only the repository-level structure for Desktop Foundry before individual skills are introduced.

## Current layout

```text
desktop-foundry/
├── README.md
├── AGENTS.md
├── CONTRIBUTING.md
├── skills/
│   └── .gitkeep
└── docs/
    └── repository-layout.md
```

## Directory responsibilities

### `skills/`

The source directory for public installable skills.

A future skill is placed under:

```text
skills/<skill-name>/
```

Its internal structure is intentionally **not** defined here. Skill anatomy belongs to the skill-creator capability or current specification used when that skill is authored.

This repository should not freeze optional directories, metadata files, templates, assets, scripts, references, or agent-specific files into a universal layout. Different skills may legitimately require different structures.

### `docs/`

Repository-level documentation only: architecture decisions, contribution rules, maintenance notes, and other material about Desktop Foundry itself.

Do not use this directory to predefine the internal anatomy of individual skills.

## Deliberately omitted for now

The following repository-level directories are not created until a real repository-wide use case exists:

- `scripts/` — repository maintenance or validation scripts;
- `examples/` — cross-skill examples;
- `templates/` — repository-wide templates;
- `.github/workflows/` — CI after there is content worth validating;
- shared resource directories — only if a concrete cross-skill need justifies them.

The goal is to keep Desktop Foundry's repository contract small and leave skill-specific structure to the tooling designed to create each skill.
