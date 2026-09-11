# Contributing

Desktop Foundry is a collection of reusable Agent Skills for desktop application development.

## Adding a skill

Do not add a skill until its responsibility and boundary are clear.

When a new skill is justified, create:

```text
skills/<skill-name>/
├── SKILL.md
├── references/   # optional
├── scripts/      # optional
└── assets/       # optional
```

## Requirements

A contributed skill should:

- solve one coherent, reusable task;
- have clear activation conditions;
- be self-contained inside its own directory;
- avoid unnecessary coupling to other skills;
- separate core workflow from detailed reference material;
- define completion criteria when the task has a verifiable end state;
- avoid placeholders in published workflows;
- remain agent-neutral unless agent-specific behavior is intentional.

## Naming

- Use lowercase kebab-case for skill directory names.
- Keep the frontmatter `name` identical to the directory name.
- Prefer capability-oriented names.

## Validation

After at least one skill exists, repository-level validation should include discovery through the Skills CLI, for example:

```bash
npx skills add loogg/desktop-foundry --list
```

Validation scripts and CI should be added only when there is real content to validate.

## Repository changes

Keep repository-level additions minimal. New top-level directories, shared resources, build systems, or CI workflows should have a concrete purpose before being introduced.
