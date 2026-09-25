---
name: review-feature
description: Perform an independent pre-merge review for requirement coverage, correctness, maintainability, tests, UX, accessibility, security, and regressions.
---

1. Re-read the requirement and relevant project documentation.
2. Inspect the complete diff and surrounding code.
3. Check requirement coverage before style issues.
4. Review architecture fit, business-rule placement, contracts, error handling, typing, persistence, and authorization where applicable.
5. Review tests for meaningful behavioural coverage.
6. For user-visible changes, use Playwright MCP to exercise the important path when runnable.
7. Check keyboard access, labels, responsive behaviour, and loading/empty/error states where relevant.
8. Apply the security-review skill's principles to security-sensitive changes.
9. Use Context7 where correctness depends on current library/framework semantics.
10. Report findings by severity with concrete locations and recommended fixes.

Do not approve solely because tests pass.
