# Contributing

Desktop Foundry is a collection of reusable Agent Skills for desktop application development.

## Adding a skill

Do not add a skill until its responsibility and boundary are clear.

Public skills belong under:

```text
skills/<skill-name>/
```

This repository intentionally does not prescribe the rest of a skill's file structure.

When creating a new skill, use the appropriate skill-creator capability or the current specification for the target ecosystem. The creator/specification should decide what additional files or directories are needed for that skill.

Do not create placeholder directories merely for consistency with another skill.

## Requirements

A contributed skill should:

- solve one coherent, reusable task;
- have clear activation conditions;
- avoid unnecessary coupling to unrelated skills;
- avoid placeholders in published workflows;
- remain agent-neutral unless agent-specific behavior is intentional;
- follow the current rules of the skill-creator or specification used to author it.

Repository-level contribution rules should not duplicate or freeze details that belong to evolving skill-authoring tooling.

## Validation

After at least one skill exists, repository-level validation should include discovery through the Skills CLI, for example:

```bash
npx skills add loogg/desktop-foundry --list
```

Additional validation should follow the creator/specification used by each skill. Repository-wide validation scripts and CI should be added only when there is real content to validate.

## Repository changes

Keep repository-level additions minimal. New top-level directories, shared resources, build systems, or CI workflows should have a concrete purpose before being introduced.
