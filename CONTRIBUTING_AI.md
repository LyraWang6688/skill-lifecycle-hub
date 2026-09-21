# AI Contribution Protocol

This file defines the required operating rules for any AI system modifying this repository.

## Mandatory Read Order

Before making changes:

1. Read `CONTRIBUTING_AI.md`.
2. Read `registry.yaml`.
3. Read `LIFECYCLE.md`.
4. Inspect the target project or skill before editing it.

Do not create, move, rename, deprecate, or archive a skill without checking the registry first.

## Placement Rules

### Project-specific skill

Place a skill under:

```text
projects/<project-name>/<skill-name>/
```

### Cross-project reusable skill

Place a reusable skill under:

```text
shared/<skill-name>/
```

Do not duplicate the same skill across multiple projects. Move genuinely reusable skills to `shared/`.

## Naming Rules

Use lowercase kebab-case for:

- project directories
- skill directories
- machine-readable identifiers

Examples:

```text
meeting-agent
meeting-analysis
web-research
```

## Skill Structure

Each skill must contain at least:

```text
<skill-name>/
├── SKILL.md
└── agents/
    └── openai.yaml
```

Add these only when needed:

- `scripts/` for deterministic executable logic
- `references/` for documentation or knowledge loaded on demand
- `assets/` for templates, icons, images, or other output resources

Keep `SKILL.md` focused. Do not use it as a project knowledge dump.

## Add or Update Workflow

For every contribution:

1. Determine whether the requested capability already exists.
2. Determine whether it is project-specific or shared.
3. Read the existing skill before changing it.
4. Make the smallest coherent change.
5. Update `registry.yaml`.
6. Update the project `README.md` when project membership changes.
7. Preserve Git history; do not silently overwrite or replace unrelated work.
8. Use a clear commit message.

## Registry Requirements

Every registered skill should include:

- `name`
- `path`
- `status`
- `version`
- `updated`

Project-specific skills should also be associated with a project.

## Lifecycle Rules

Only use these statuses:

- `draft`
- `testing`
- `active`
- `deprecated`
- `archived`

Follow transition rules in `LIFECYCLE.md`.

## Commit Message Convention

Use one of these patterns:

```text
feat(skill): add <skill-name>
update(skill): refine <skill-name>
fix(skill): fix <skill-name>
move(skill): move <skill-name>
deprecate(skill): deprecate <skill-name>
archive(skill): archive <skill-name>
chore(registry): update skill registry
```

## Safety Rules

Do not:

- create duplicate skills without checking the registry
- mix unrelated capabilities into one skill
- store secrets, tokens, passwords, or credentials
- change unrelated files
- invent project ownership or lifecycle status when it is unknown

When required information is missing, stop and ask for clarification instead of guessing.
