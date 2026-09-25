---
name: bug-investigation
description: Diagnose and fix a defect or regression with evidence-first debugging and a regression test where practical.
---

1. Read the relevant project instructions and implementation before editing.
2. Reproduce the problem when possible and capture the failing behaviour, error, log, test, or browser state.
3. Form a small number of evidence-based hypotheses and inspect the involved code paths.
4. Avoid broad refactors before identifying the likely root cause.
5. Add a regression test when practical.
6. Implement the smallest fix that addresses the root cause.
7. Run the focused test first, then the broader affected checks.
8. For UI defects, use Playwright MCP to reproduce and verify when the app is runnable.
9. Use Context7 for version-sensitive framework/library behaviour.
10. Report the root cause, fix, verification, and any remaining uncertainty.
