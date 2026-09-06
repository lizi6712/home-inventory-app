# Data Model

## Central distinction

`products` describes what an item is. `inventory_batches` describes physical
units currently owned. A single product may have several batches with different
purchase dates, expiry dates, prices, or locations.

## Tables

### profiles

- `id` — UUID, same identity as the authenticated user
- `display_name`
- `created_at`
- `updated_at`

### categories

- `id` — UUID
- `owner_id` — UUID
- `name`
- `parent_id` — nullable UUID for subcategories
- `created_at`

### locations

- `id` — UUID
- `owner_id` — UUID
- `name`
- `parent_id` — nullable UUID for future nested locations
- `created_at`

### products

- `id` — UUID
- `owner_id` — UUID
- `name`
- `brand` — nullable
- `barcode` — nullable string; never numeric because leading zeros matter
- `category_id` — nullable UUID
- `default_location_id` — nullable UUID
- `unit` — e.g. unit, pack, bottle, kg
- `minimum_stock` — nullable decimal
- `photo_path` — nullable
- `notes` — nullable
- `is_active` — boolean
- `created_at`
- `updated_at`

### inventory_batches

- `id` — UUID
- `owner_id` — UUID
- `product_id` — UUID
- `location_id` — UUID
- `quantity` — decimal greater than or equal to zero
- `purchase_date` — nullable date
- `expiry_date` — nullable date
- `unit_price` — nullable decimal
- `currency_code` — nullable ISO currency code
- `created_at`
- `updated_at`

### inventory_movements

- `id` — UUID
- `owner_id` — UUID
- `product_id` — UUID
- `batch_id` — nullable UUID
- `movement_type` — purchase, use, disposal, correction, transfer
- `quantity_delta` — signed decimal
- `from_location_id` — nullable UUID
- `to_location_id` — nullable UUID
- `note` — nullable
- `occurred_at`
- `created_at`

### shopping_list_items

- `id` — UUID
- `owner_id` — UUID
- `product_id` — nullable UUID
- `custom_name` — nullable; used when no product exists yet
- `desired_quantity` — nullable decimal
- `status` — needed, purchased, dismissed
- `source` — manual or low_stock
- `created_at`
- `updated_at`

## Required ownership rule

Every user-owned table contains `owner_id`. Every read, insert, update, and
delete must be checked against the authenticated user's ID in the database, not
only hidden in the user interface.

## Derived values

- Current product quantity = sum of active batch quantities.
- Low stock = current quantity < product minimum stock.
- Expiring soon = expiry date is known and falls within the user's selected
  warning window.

Do not store derived totals in the MVP unless performance evidence shows that
calculation is insufficient.

