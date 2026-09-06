# MVP Scope

## Included

### Account

- Register, sign in, sign out, and reset password.
- User profile with display name and basic preferences.

### Product catalog

- Product name, brand, barcode, category, subcategory, default location, unit,
  minimum stock, notes, and optional photo.
- Search by product name, brand, or barcode.

### Physical inventory

- Add a batch with quantity, purchase date, expiry date, location, and optional
  price.
- Allow unknown purchase and expiry dates.
- Edit or remove a batch through a recorded inventory movement.

### Inventory activity

- Movement types: purchase, use, disposal, correction, and transfer.
- Movement history per product.

### Dashboard

- Total products and total units.
- Expiring soon.
- Low stock.
- Category and location filters.

### Shopping list

- Manually add and remove items.
- Suggest items whose current quantity is below their minimum stock.

## Explicitly excluded from the MVP

- Automatic product identification from external barcode databases.
- OCR reading of expiry dates.
- Consumption forecasting.
- Push notifications.
- Social sharing of private inventory.
- Multiple households per user or household invitations.
- Native iOS and Android applications.
- Payments or subscriptions.

Exclusion does not mean rejection. These features remain candidates only after
the MVP proves that users consistently maintain their inventory.

## MVP release gate

Do not add a deferred feature until the complete add-stock, use-stock,
expiring, and low-stock flows work with real test data on mobile.

