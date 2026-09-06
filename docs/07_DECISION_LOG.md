# Decision Log

## D-001 — Multi-user private inventories

Each registered user has a private inventory. Reason: the product should be
publicly usable without exposing household data.

## D-002 — Mobile-first PWA before native apps

Start with a responsive PWA. Reason: one codebase, simple public distribution,
and low initial cost. Native applications remain deferred until actual usage
justifies the extra complexity.

## D-003 — Product and batch separation

Store product identity separately from physical stock batches. Reason: units of
the same product may have different expiry dates, purchase dates, prices, and
locations.

## D-004 — Movement history

Record purchases, use, disposal, transfers, and corrections. Reason: current
quantity alone cannot explain how inventory changed or support later usage
analysis.

## D-005 — Free-tier-first replaceable stack

Start with GitHub, React/TypeScript, Supabase, and a compatible web host. Keep
the product specification tool-independent so an AI builder or design tool can
be replaced.

## D-006 — Unknown is valid

Purchase date and expiry date may be null. Reason: forcing a value for existing
household stock creates false information.

