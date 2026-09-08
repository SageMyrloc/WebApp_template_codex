# Project working guide

## Start here
- Read [project.config.yaml](project.config.yaml), [the brief](docs/project-brief.md), and [progress](docs/progress.md) before starting work.
- Consult [architecture](docs/architecture.md) and [design](docs/design.md) for relevant implementation decisions.
- This repository starts as an instruction template. Do not assume an application, dependencies, or runnable commands already exist.
- Follow the user's current instructions. If they change an agreed choice, update the affected configuration and documentation.

## Technology choices
- Use project.config.yaml as the source of truth for selected technologies and planned paths. Do not silently substitute another stack.
- Keep authoritative technology selections and planned paths only in project.config.yaml. Other documents should link to it; architecture records observed implementation facts and rationale. Flag discrepancies rather than treating stale documentation as configuration.
- Treat "undecided" as unresolved and "none" as intentionally excluded. Ask only when an unresolved choice materially blocks the current task.
- The YAML does not switch frameworks or configure the running application. If it differs from existing code, explain the discrepancy and assess migration work before changing implementations.
- When scaffolding, verify compatible supported dependency versions and pin them in the appropriate manifests, lockfile, runtime files, and container definitions.
- Keep runtime settings in environment variables; document required names using a secret-free .env.example when needed.

## Project initialization
- Before scaffolding a new project, review its shape, configuration, brief, and design references. Identify only unresolved decisions that materially block the first milestone.
- Check that architecture, selected technologies, and planned paths agree. Do not create components or directories marked "none".
- A frontend-only project needs no separate backend; an API-only project needs no frontend; an integrated application may share one frontend/backend path. A database engine of "none" requires an ORM of "none".
- During a planning-only task, provide a concise initialization plan without scaffolding. Once the user authorizes scaffolding, implement the agreed configuration and record actual structure and verified commands.

## Implementation
- Make routine implementation decisions independently within the agreed scope.
- Reuse existing components and utilities; keep changes focused.
- Keep business rules separate from UI components and validate inputs at application boundaries.
- Enforce authentication and authorization on the server when applicable.
- Never commit credentials or private user data.
- Document consequential decisions and unresolved questions without inventing requirements.

## Design
- Follow the design document and agreed references.
- Establish a representative page before extending the visual system across the app.
- Reuse design tokens and components. Support keyboard use, labelled controls, and responsive layouts.
- Account for relevant loading, empty, error, and validation states.

## Verification
- Use the real commands documented in docs/architecture.md. Add commands there when tooling is implemented and verified.
- Run checks relevant to the change; add meaningful tests for business rules and bug fixes.
- Inspect UI changes at mobile and desktop sizes and exercise affected interactions when browser tooling is available.
- Check the production build after build configuration or dependency changes.
- For documentation-only work, check syntax, links, and consistency; do not invent application test results.
- Report what was verified and any checks that could not be performed.

## Handoff
- Update docs/progress.md after meaningful work with current state, next steps, and outstanding issues.
- Keep the brief, configuration, design, and architecture aligned with agreed decisions.
- Give a concise completion report with links to changes and verification results.
