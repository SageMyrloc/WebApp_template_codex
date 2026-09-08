# Architecture

Status: Planning only; no application has been scaffolded.

## Configuration and system overview

Read [project.config.yaml](../project.config.yaml) for selected technologies, application shape, and planned paths.
This document records observed implementation facts and rationale, not a second set of authoritative defaults.
No application system exists yet. After scaffolding, describe its actual components and boundaries.
Flag differences from configuration and assess migration work before changing implementations.

## Repository layout

Planned paths are defined in project.config.yaml. Application directories do not exist yet.
After scaffolding, record the actual layout and explain component responsibilities.

## Frontend

Not implemented. Record routing, state management, and UI boundaries if applicable.

## Backend

Not implemented. Record service boundaries, input validation, and error handling if applicable.

## Data model

Not implemented. Record entities, persistence, and migration procedures if applicable.

## Authentication and authorization

Not implemented. Record identity flows, roles, and enforcement boundaries if applicable.

## External integrations

Not implemented. Record service responsibilities and failure handling if applicable.

## Runtime configuration

No runtime environment variables are required yet.
When needed, add a secret-free .env.example and document variable names, purpose, required/optional status, and safe defaults. Never record secrets here.

## Verified commands

No commands are implemented or verified yet.
After scaffolding, record prerequisites, working directory, exact command, and verification result for applicable operations:

- Installation and local services
- Development
- Linting and formatting checks
- Type checking
- Unit, component, and end-to-end tests
- Database migrations
- Production build

Do not present example or anticipated commands as verified. Mark unavailable checks explicitly.

## Deployment

Selections are defined in project.config.yaml. No deployment files or procedures exist yet.
Record actual build, release, migration, and rollback procedures when implemented.

## Decision log

Record consequential decisions with their date, rationale, and implications.
Distinguish proposed decisions from implemented facts.
