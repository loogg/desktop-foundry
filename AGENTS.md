# Repository Rules

This repository contains reusable Agent Skills for desktop application development.

## Repository boundary

Public skills live under:

```text
skills/<skill-name>/
```

Beyond that placement rule, this repository does **not** define a fixed internal layout for individual skills.

When creating or restructuring a skill:

- use the appropriate skill-creator capability or the current specification for the target skill ecosystem;
- let that creator/specification decide which files and subdirectories the skill needs;
- do not pre-create optional directories just to match a repository template;
- do not reject a valid skill structure merely because it differs from other skills in this repository.

`SKILL.md` is the skill entry point used for discovery. Any additional structure belongs to the skill itself and may evolve with the relevant tooling and specification.

## Skill boundaries

- Prefer complete reusable capabilities over small component-level micro-skills.
- Avoid unnecessary coupling between unrelated skills.
- Do not tie a generic skill to a single agent, framework, language, or product unless that specialization is intentional.
- Repository-level `docs/` describes Desktop Foundry itself; it must not become an accidental substitute for content that a particular skill creator expects to package with that skill.

## Authoring policy

- Do not duplicate evolving skill-authoring rules in this repository when they are already owned by a dedicated skill-creator or specification.
- Treat the selected skill-creator as authoritative for the internal anatomy of a skill.
- Keep repository-level rules focused on repository organization, contribution boundaries, and compatibility goals.
- Avoid placeholder behavior in published skills.

## Repository-level files

- `docs/` documents this repository itself.
- Do not add top-level directories preemptively. Add them only when they have a real repository-wide use case.
- Do not add agent-specific mirrors such as `.claude/skills/` or `.agents/skills/` unless a demonstrated compatibility requirement calls for them.

## Current state

The repository structure is initialized, but no skill is implemented yet. Do not create a `SKILL.md` unless the task explicitly requires implementing a skill.
