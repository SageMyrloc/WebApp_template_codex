---
name: database-change
description: Make a safe database/schema/persistence change when a database and ORM are configured in project.config.yaml.
---

1. Read project.config.yaml, the current schema/migration history, affected services/routes, and project instructions.
2. If database or ORM is set to none, stop and follow the configured architecture instead.
3. Identify compatibility risks including nullability, defaults, uniqueness, indexes, foreign keys, cascades, and existing rows.
4. Prefer additive/backward-compatible changes where practical.
5. Create a real migration using the configured ORM/tooling and review generated SQL when available.
6. Update fixtures, seeds, contracts, APIs, and tests as required.
7. Run generation/migration commands and relevant tests using the project's documented workflow.
8. Never commit credentials or connection strings.
9. Document staged rollout or backfill requirements when a production migration needs them.
