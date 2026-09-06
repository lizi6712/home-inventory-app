# Architecture and Security

## Logical architecture

1. Mobile-first web interface.
2. Authentication service identifies the user.
3. API or database client submits requests with the user session.
4. Database-level policies restrict every row to its owner.
5. Object-storage policies restrict product images to their owner.

## Public does not mean public data

The application URL and registration screen may be public. Inventory records,
movement history, shopping lists, and private images are never public.

## Minimum security requirements

- Enable Row Level Security on every user-owned table.
- Create explicit owner-only policies for select, insert, update, and delete.
- Validate that referenced category, location, product, and batch records belong
  to the same user.
- Never trust `owner_id` supplied by the browser; derive or verify it from the
  authenticated session.
- Keep service-role keys and other secrets out of browser code and GitHub.
- Commit only `.env.example`, never `.env`.
- Restrict accepted image types and sizes.
- Use database constraints for quantities, permitted statuses, and movement
  types.
- Record timestamps and retain movement history for traceability.

## Critical security test

Create two test users. While signed in as User B, attempt to read, update, and
delete records belonging to User A by calling their known IDs directly. The
release fails if any operation succeeds.

## Replaceable layers

- Figma can be replaced by another design tool.
- The AI coding assistant can be replaced without changing the specification.
- Vercel can be replaced by another compatible host.
- The React interface can be replaced while the data contracts remain stable.

Replacing Supabase is possible but more expensive because it currently combines
authentication, relational data, access policies, and file storage. Therefore
the database schema and security rules must remain documented and versioned.

