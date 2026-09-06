# AI Handoff Contract

Give this file and all preceding documents to any AI tool before asking it to
build or change the product.

## Instruction to the AI

You are working on a multi-user home inventory application. Treat the repository
documentation as the product source of truth. Before editing code:

1. Read `README.md` and every file in `docs/`.
2. State which requirement or user flow the requested change implements.
3. Do not add speculative features outside `02_MVP_SCOPE.md`.
4. Preserve the distinction between products, batches, and movements.
5. Enforce ownership in the database, not only in the interface.
6. Never place secrets or real user data in the repository.
7. Keep the interface mobile-first and accessible.
8. Update relevant documentation and the decision log when a product or
   architecture decision changes.
9. Make the smallest coherent change and test its success, failure, empty, and
   permission states.
10. Explain what changed in plain language and list any user action required.

## Change request template

Goal:

User story:

Current behavior:

Required behavior:

Acceptance criteria:

Out of scope:

Files or flows likely affected:

Security and privacy considerations:

How to verify:

