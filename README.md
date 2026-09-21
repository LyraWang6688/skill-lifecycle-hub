# Skill Lifecycle Hub

Central repository for managing the full lifecycle of AI skills across projects.

## Purpose

This repository is the source of truth for reusable AI skills owned or maintained by Lyra.

- Organize skills by project.
- Keep cross-project skills in `shared/`.
- Track lifecycle status and version information in `registry.yaml`.
- Require AI contributors to follow `CONTRIBUTING_AI.md`.

## Repository Structure

```text
skill-lifecycle-hub/
├── README.md
├── CONTRIBUTING_AI.md
├── LIFECYCLE.md
├── registry.yaml
├── projects/
│   └── <project-name>/
│       ├── README.md
│       └── <skill-name>/
│           ├── SKILL.md
│           ├── agents/
│           │   └── openai.yaml
│           ├── scripts/
│           ├── references/
│           └── assets/
└── shared/
    └── <skill-name>/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        ├── scripts/
        ├── references/
        └── assets/
```

## Lifecycle

`draft -> testing -> active -> deprecated -> archived`

See [LIFECYCLE.md](./LIFECYCLE.md) for transition rules.

## Registry

`registry.yaml` is the machine-readable index of projects and skills. It should be updated whenever a skill is added, moved, renamed, versioned, deprecated, or archived.

## AI Contributors

Before changing this repository, read:

1. [CONTRIBUTING_AI.md](./CONTRIBUTING_AI.md)
2. [registry.yaml](./registry.yaml)
3. [LIFECYCLE.md](./LIFECYCLE.md)
