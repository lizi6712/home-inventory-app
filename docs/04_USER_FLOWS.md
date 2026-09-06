# User Flows

## First use

1. User registers.
2. User confirms access and signs in.
3. User sees an empty dashboard with one primary action: Add product.
4. User creates their first product and stock batch.
5. Dashboard displays the new inventory.

## Add an existing product to stock

1. Tap Add stock.
2. Search or scan barcode.
3. Select product.
4. Enter quantity.
5. Optionally enter purchase date, expiry, price, and location.
6. Confirm.
7. System creates or updates a batch and records a purchase movement.

## Add an unknown product

1. Search or scan returns no result.
2. Tap Create product.
3. Enter name; other fields are optional unless technically required.
4. Save the product.
5. Continue directly to Add stock without searching again.

## Use or discard stock

1. Open product.
2. Tap Use or Discard.
3. Enter quantity.
4. When several batches exist, default to the earliest expiry date but allow
   the user to choose another batch.
5. Confirm.
6. System records the movement and reduces the selected batch.

## Check expiring items

1. Open Expiring soon from the dashboard.
2. Items are ordered by earliest expiry.
3. User can use, discard, or open the product.

## Shopping list

1. Open Shopping list.
2. See manual items and low-stock suggestions.
3. Mark an item purchased.
4. Continue to Add stock with product and desired quantity prefilled.

## Required interface states

Every flow must define loading, empty, validation error, network error,
permission error, and successful completion states.

