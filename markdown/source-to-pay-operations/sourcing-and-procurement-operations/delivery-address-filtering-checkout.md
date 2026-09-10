---
title: Delivery address filtering at checkout
description: When a shopper removes a saved delivery address, the Deleted column in the Delivery locations table is set to true for that address record. The Shopping Hub checkout flow automatically filters out all addresses where the Deleted column is true, so those addresses do not appear as options during checkout.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/delivery-address-filtering-checkout.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [address suppression, checkout, deleted addresses]
breadcrumb: [Saved delivery addresses, Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Delivery address filtering at checkout

When a shopper removes a saved delivery address, the Deleted column in the Delivery locations table is set to **true** for that address record. The Shopping Hub checkout flow automatically filters out all addresses where the Deleted column is **true**, so those addresses do not appear as options during checkout.

## How address filtering works

When you remove a delivery address, it is no longer available at checkout. The checkout address picker shows only active delivery addresses \(addresses you have not removed\).

-   Removed addresses do not appear in the checkout address picker
-   Active saved addresses continue to appear without disruption
-   Filtering happens automatically

## Checkout address visibility

-   Deleted addresses do not appear: When shopping at checkout, deleted addresses do not appear to the user.
-   Non-deleted addresses display normally: All active saved addresses appear in the delivery location picker.
-   Work address directory is unaffected: When adding a new work address from the org directory, previously deleted addresses are visible and can be re-added to the saved list.
-   Re-addition restores functionality: If a user re-adds a previously removed address from the work picker, the Deleted column is set to **false** and the address reappears as an available option.

## Cart line address reassignment

If a cart line is assigned to a delivery address that is deleted, Shopping Hub automatically reassigns the line to a fallback address:

-   Preferred fallback: The user's session deliver-to location \(if still active\)
-   Secondary fallback: The user's account default delivery location
-   Scope: Only applied to cart lines in draft or active status; lines in other states or tied to completed orders are left untouched

No cart line references an invalid or deleted address when the shopper proceeds to checkout.

**Parent Topic:**[Managing saved delivery addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-overview.md)

