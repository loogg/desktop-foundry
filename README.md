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

- `skills/` — source directory for installable Agent Skills. Each future skill lives in its own directory.
- `docs/` — repository-level documentation and design decisions.
- `AGENTS.md` — repository rules for agents and contributors working on this repository.
- `CONTRIBUTING.md` — repository-level contribution guidance.

Desktop Foundry intentionally does not prescribe a universal internal file structure for individual skills. When a skill is created, its structure should follow the appropriate skill-creator capability or the current specification for that target ecosystem.

## Future installation

Once skills are published, the repository can be used with the Skills CLI:

```bash
npx skills add loogg/desktop-foundry
```

## Status

The repository currently contains infrastructure only. No skill is available yet.
