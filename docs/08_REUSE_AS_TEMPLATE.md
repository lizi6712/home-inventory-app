# Reuse This Method for Another AI Project

## Portable project layers

1. Problem and audience — `01_PROJECT_BRIEF.md`
2. Boundaries — `02_MVP_SCOPE.md`
3. Information structure — `03_DATA_MODEL.md`
4. User behavior — `04_USER_FLOWS.md`
5. Technology and safeguards — `05_ARCHITECTURE_AND_SECURITY.md`
6. Instructions to future AI tools — `06_AI_HANDOFF.md`
7. Reasons behind decisions — `07_DECISION_LOG.md`

## Reuse process

1. Copy the repository into a new repository.
2. Replace the problem, user, and success criteria.
3. Define what the first version includes and explicitly excludes.
4. Model the underlying records before designing screens.
5. Write the three most important user flows.
6. Identify private data, permissions, and failure scenarios.
7. Record tool choices as replaceable decisions, not permanent facts.
8. Give the complete repository to the selected AI tool.
9. Ask the AI to implement one vertical user flow at a time.
10. Commit only after the flow is verified.

## Quality questions

- Can another AI understand the product without reading the old chat?
- Can the interface tool be replaced without losing the data model?
- Are unknown values allowed instead of invented?
- Is every private record protected server-side or in the database?
- Is the MVP small enough to finish and useful enough to test?
- Does every added feature solve an observed problem?

