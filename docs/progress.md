# Progress

## Current state
- Reusable instruction template updated with configuration ownership and initialization guidance.
- project.config.yaml version 2 includes application shape, tooling, testing, and CI selections, with explicit exclusion conventions.
- README documents initialization, scaffolding, and verification.
- Brief and design placeholders expanded; architecture is ready to record implementation facts.
- No application code, dependencies, database, or deployment has been created.

## Next steps
1. Review the template changes.
2. Exercise the workflow in a throwaway repository with a small first milestone.
3. For each new application, complete its brief and resolve choices needed for that milestone.
4. Scaffold the application and document actual structure and verified commands.

## Known issues and open decisions
- Project-specific choices remain unresolved in project.config.yaml and the brief/design placeholders.
- Dependency versions will be resolved and pinned when scaffolding.
- The end-to-end template workflow has not yet been exercised with a generated application.
- Custom consumers of configuration version 1 must adapt to the nested database fields in version 2.
