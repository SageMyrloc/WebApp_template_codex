# Architecture

Status: Planning only; no application has been scaffolded.

## Technology selections
Read [project.config.yaml](../project.config.yaml) for the agreed defaults.
Record rationale and implementation details here without duplicating the full configuration.

## Planned boundaries
- apps/web/: frontend interface.
- apps/api/: server routes, authorization, and business operations.
- packages/shared/: shared types and validation when needed.
- docs/: project requirements and decisions.

These application directories do not exist yet.

## Setup and commands
No commands are implemented or verified yet.
When scaffolding, document prerequisites and exact commands for installation, local services, development, linting, type checking, tests, database migrations, and production builds.

## Runtime configuration
No runtime environment variables are required yet.
Add a secret-free .env.example and document each variable when the application needs it.

## Data and integrations
Undecided. Record the data model, external services, and authentication approach as they are agreed.

## Deployment
Docker on Hetzner is the configured default. Deployment files and procedures are not implemented yet.

## Decision log
Record consequential decisions with their date, rationale, and implications.
Changing a selected technology after implementation requires assessing migration work.
