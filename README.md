# WebApp template for Codex

A reusable starting point for building web applications with Codex/ChatGPT.
This repository contains instructions and planning documents. Application code and tooling are added when a project begins.

## Start a new application

1. Create a separate repository from this template or copy its contents.
2. Edit [project.config.yaml](project.config.yaml): set the project identity and type, application shape, technologies, and planned paths.
3. Fill in [the project brief](docs/project-brief.md), especially the first user journey, acceptance criteria, and exclusions.
4. Add visual direction, assets, and references to [the design guide](docs/design.md), or mark UI sections not applicable for an API-only project.
5. Ask Codex for the initialization plan below. Resolve choices that materially block the first milestone; unrelated choices can remain undecided.
6. Ask Codex to scaffold the agreed milestone using the second prompt.
7. Have Codex verify the implementation and record actual structure and commands in [architecture](docs/architecture.md), and current state in [progress](docs/progress.md).
8. Begin feature work against the brief and acceptance criteria.

If using ChatGPT without automatic repository instruction loading, explicitly ask it to read AGENTS.md first.

### Initialization prompt

> Read AGENTS.md, project.config.yaml, and all project documentation. This repository has just been created from the template. Check that the project shape, technology choices, and planned paths agree. Identify unresolved decisions that materially block scaffolding the first milestone. Do not implement anything yet. Give me a concise project initialization plan.

### Scaffolding prompt

> Scaffold the first agreed milestone according to AGENTS.md, project.config.yaml, and the project documentation. Respect components marked "none". Verify the relevant checks and production build once tooling exists. Update docs/architecture.md with the actual structure and commands you verified, and docs/progress.md with completed work, next steps, and outstanding issues. Report any checks you could not perform.

## Files

| File | Purpose |
| --- | --- |
| AGENTS.md | Stable working instructions for Codex/ChatGPT |
| project.config.yaml | Per-project technology choices, application shape, and planned paths |
| docs/project-brief.md | Audience, scope, user journeys, and success criteria |
| docs/design.md | Visual direction and interface expectations |
| docs/architecture.md | Observed implementation facts, decisions, and verified commands |
| docs/progress.md | Current state and next steps |

## Configuration conventions

Current technology defaults and planned directories are defined only in [project.config.yaml](project.config.yaml). Change them for each new project; AGENTS.md stays technology-neutral.

- `undecided` means unresolved. Resolve it when it materially blocks the current milestone.
- `none` means deliberately excluded. Do not install tooling or create directories for that component.
- Keep component choices and paths consistent with the application shape. Frontend-only projects omit the separate backend; API-only projects omit the frontend. Integrated applications may share a frontend/backend path.
- When there is no database, set both its engine and ORM to `none`.
- Testing, formatting, linting, CI, authentication, and deployment choices are editable per project.

The YAML guides development; it does not generate an app, configure its runtime, or migrate existing code. If configuration changes after implementation, assess the migration and document discrepancies.

Configuration version 2 adds project shape and tooling selections and moves the former `stack.database` string and `stack.orm` value into `stack.database.engine` and `stack.database.orm`. Update any custom consumers when adopting this version.

Keep configuration free of secrets. Runtime environment values belong in local environment files or the deployment secret store.

No application directories or install, development, or test commands exist yet. Record commands only after implementing and verifying them.

## Validate the template workflow

After reviewing these template changes, create a throwaway repository from the template and exercise initialization, scaffolding, and verification for one small milestone. Record any friction before expanding the template further.
