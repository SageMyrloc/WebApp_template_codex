# WebApp template for Codex

A reusable starting point for building web applications with Codex/ChatGPT.
This repository currently contains instructions and planning documents; application code and tooling are added when a project begins.

## Start a new application
1. Create a separate repository from this template or copy its contents.
2. Edit [project.config.yaml](project.config.yaml) for the new project's name and technology choices.
3. Fill in [the project brief](docs/project-brief.md) and add design references to [the design guide](docs/design.md).
4. Ask Codex to read [AGENTS.md](AGENTS.md) and scaffold the first agreed milestone.
5. Record actual setup and verification commands in [architecture](docs/architecture.md) as they become available.

If using ChatGPT without automatic repository instruction loading, explicitly ask it to read AGENTS.md first.

## Files
| File | Purpose |
| --- | --- |
| AGENTS.md | Working instructions for Codex/ChatGPT |
| project.config.yaml | Editable default technology selections |
| docs/project-brief.md | Audience, scope, user journeys, and success criteria |
| docs/design.md | Visual direction and interface expectations |
| docs/architecture.md | Implementation decisions and verified commands |
| docs/progress.md | Current state and next steps |

## Default stack
TypeScript, React with Vite, Fastify, PostgreSQL, Prisma, and pnpm.
Deployment defaults to Docker on Hetzner. Authentication and visual styling remain undecided.

The YAML guides development; it does not automatically generate an app or migrate existing code.
Keep it free of secrets. Runtime environment values belong in local environment files or the deployment secret store.

## Planned application layout
- apps/web/ — frontend
- apps/api/ — backend
- packages/shared/ — shared contracts and validation where needed
- docs/ — project documentation

Application directories will be created when scaffolding starts. There are no install, development, or test commands yet.
