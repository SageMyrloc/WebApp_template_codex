---
name: implement-feature
description: Implement a feature end to end across the project layers selected in project.config.yaml.
---

1. Read AGENTS.md, project.config.yaml, docs/project-brief.md, docs/progress.md, and relevant architecture/design notes.
2. Trace the current implementation before editing and reuse existing patterns.
3. Identify affected layers from the configured application shape: data model, backend, shared contracts, frontend, tests, docs, and deployment/config.
4. Implement the smallest coherent vertical slice that satisfies the requirement.
5. Keep business rules out of UI components; validate inputs at boundaries and enforce authorization server-side where applicable.
6. Use Context7 when framework/library behaviour is current-version-sensitive or uncertain.
7. Add tests appropriate to the configured stack. For user-visible changes, add/update E2E coverage when E2E tooling is configured.
8. Use Playwright MCP for interactive browser verification when the project has a runnable UI.
9. Run the real verification commands recorded in docs/architecture.md.
10. Update docs/progress.md and any affected architecture/design notes.
11. Report what changed, what ran successfully, and what remains unverified.

Never claim a check passed unless it actually ran.
