# Desktop Foundry

Reusable agent workflows and skills for designing, building, reviewing, and testing desktop applications.

> Repository structure is initialized. No public skills are implemented yet.

## Scope

Desktop Foundry is intended for reusable, implementation-oriented guidance for desktop GUI applications. It is not tied to a single domain, UI framework, programming language, or agent.

Potential future areas include product design, UI/UX, architecture, implementation, testing, release workflows, device tools, engineering utilities, and framework-specific development.

## Repository layout

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

- `skills/` — installable Agent Skills. Each future skill will live in its own directory.
- `docs/` — repository-level documentation and design decisions. It is not a runtime dependency for installed skills.
- `AGENTS.md` — repository rules for agents and contributors working on this repository.
- `CONTRIBUTING.md` — conventions for adding or changing skills.

## Future installation

Once skills are published, the repository can be used with the Skills CLI:

```bash
npx skills add loogg/desktop-foundry
```

Individual skills will follow this shape:

```text
skills/<skill-name>/
├── SKILL.md
├── references/   # optional
├── scripts/      # optional
└── assets/       # optional
```

## Status

The repository currently contains infrastructure only. No skill is available yet.
