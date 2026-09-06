# Home Inventory App

A tool-independent blueprint for a multi-user home inventory application.

## Product principle

The data, rules, and documentation are the durable product. The UI builder, AI
assistant, hosting provider, and design tool may be replaced without redefining
the application.

## Current decisions

- Publicly reachable web application with user registration.
- Every user has a private inventory.
- Mobile-first Progressive Web App (PWA).
- Free-tier-first architecture.
- GitHub is the source of truth for code and project documentation.
- No production data, passwords, API secrets, or private images belong in Git.

## Recommended starting stack

- Frontend: React + TypeScript + Vite
- Styling: Tailwind CSS
- Data, authentication, and image storage: Supabase
- Hosting: Vercel or another compatible static/web host
- Design: Figma
- Source control: GitHub

These are replaceable implementation choices. The files in `docs/` define the
product independently of this stack.

## Documentation order

1. `docs/01_PROJECT_BRIEF.md`
2. `docs/02_MVP_SCOPE.md`
3. `docs/03_DATA_MODEL.md`
4. `docs/04_USER_FLOWS.md`
5. `docs/05_ARCHITECTURE_AND_SECURITY.md`
6. `docs/06_AI_HANDOFF.md`
7. `docs/07_DECISION_LOG.md`
8. `docs/08_REUSE_AS_TEMPLATE.md`

## Status

Phase 1 — product foundation and portable specification.

