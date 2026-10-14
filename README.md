# Desktop Foundry

Reusable agent workflows and skills for designing, building, reviewing, and testing desktop applications.

Local skill sources are available under `skills/`. Local availability does not imply a published or installed release.

## Scope

Desktop Foundry is intended for reusable, implementation-oriented guidance for desktop GUI applications. It is not tied to a single domain, UI framework, programming language, or agent.

Potential future areas include product design, UI/UX, architecture, implementation, testing, release workflows, device tools, engineering utilities, and framework-specific development.

## Repository layout

```text
desktop-foundry/
├── README.md
├── CONTRIBUTING.md
├── skills/
│   ├── gui-development/
│   ├── design-prototyping/
│   └── web-prototyping/
└── docs/
    └── repository-layout.md
```

- `skills/` — source directory for installable Agent Skills. Each skill lives in its own directory.
- `docs/` — repository-level documentation and design decisions.
- `CONTRIBUTING.md` — repository-level contribution guidance.

Desktop Foundry intentionally does not prescribe a universal internal file structure for individual skills. When a skill is created, its structure should follow the appropriate skill-creator capability or the current specification for that target ecosystem.

## Future installation

Once skills are published, the repository can be used with the Skills CLI:

```bash
npx skills add loogg/desktop-foundry
```

## Available local skills

| Skill | Purpose |
|---|---|
| [gui-development](skills/gui-development/README.md) | GUI implementation workflow with project-aware architecture references, task acceptance, real interaction, visual review and repair/retest. Covers Web and desktop GUI increments. |
| [design-prototyping](skills/design-prototyping/README.md) | Organize UI prototypes, component examples and design annotations. |
| [web-prototyping](skills/web-prototyping/README.md) | Guide product UI and interaction expression in Web prototypes: interface states, mock data, component placeholders and source comments. Includes a TSX structure example adaptable to the current platform. |

To inspect local discovery without installing, run `npx skills add . --list` from this repository. See each skill's README for usage and validation limits.
