# Repository Layout

This document defines the repository-level structure for Desktop Foundry before individual skills are introduced.

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

The only source directory for public installable skills.

Future skills should use:

```text
skills/<skill-name>/
├── SKILL.md
├── references/   # optional
├── scripts/      # optional
└── assets/       # optional
```

A skill should carry everything it needs at runtime inside its own directory so that installation remains portable.

### `docs/`

Repository-level documentation only: architecture decisions, contribution rules, maintenance notes, and other material about Desktop Foundry itself.

Files here should not be required by an installed skill at runtime.

## Deliberately omitted for now

The following directories are not created until a real use case exists:

- `scripts/` — repository-wide maintenance or validation scripts;
- `examples/` — end-to-end examples that are useful across skills;
- `templates/` — repository-wide authoring templates;
- `.github/workflows/` — CI validation after there is content to validate;
- shared `references/` or `assets/` — avoided to keep skills independently portable.

This keeps the repository small while preserving a clean path for growth.
