---
name: release-check
description: Run a final release-readiness pass using the actual tooling selected and documented for the project.
---

1. Inspect the current diff/status and confirm only intended files are included.
2. Run the verification commands documented in docs/architecture.md for formatting, linting, type checks, tests, and build when those tools are configured.
3. Run configured E2E tests. For important UI changes, exercise the critical path with Playwright MCP when possible.
4. Confirm database migrations are present and appropriate when a database is configured.
5. Check environment/deployment documentation for new requirements.
6. Confirm no credentials, private data, debug artefacts, temporary files, or generated test output were accidentally added.
7. Confirm docs/progress.md and affected architecture/design/readme content are current.
8. Summarize pass/fail results and blockers. Never mark an unrun check as passed.
