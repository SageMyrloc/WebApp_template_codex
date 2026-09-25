---
name: security-review
description: Review a web application change for concrete security risks before merge or release.
---

Prioritize real exploit paths over generic checklist output.

Check when relevant:
- authentication and session/cookie handling;
- server-side authorization and ownership checks;
- input validation, output encoding, injection, and unsafe query construction;
- sensitive-data exposure in APIs, logs, errors, client bundles, and repository files;
- CSRF/CORS assumptions;
- file upload/download validation and path handling;
- SSRF or untrusted URL fetching;
- abuse/rate-limit concerns on sensitive endpoints;
- security-sensitive dependency/framework behaviour;
- destructive actions and auditability.

Use Context7 when current framework/library behaviour matters.

Return findings ordered by severity with location, impact, evidence, and remediation. Distinguish confirmed vulnerabilities from hardening suggestions.
