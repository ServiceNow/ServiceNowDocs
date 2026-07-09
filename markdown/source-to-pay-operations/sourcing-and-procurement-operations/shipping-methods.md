---
title: Shipping methods
description: Shipping methods define how goods are transported from suppliers to delivery destinations. Administrators can create shipping methods and associate them with suppliers and delivery locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/shipping-methods.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-06-26"
reading_time_minutes: 1
breadcrumb: [Complete your checkout, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Shipping methods

Shipping methods define how goods are transported from suppliers to delivery destinations. Administrators can create shipping methods and associate them with suppliers and delivery locations.

## About shipping methods

Shipping methods are applicable only for product type goods. Shipping method records store the details of the carrier, the applicable suppliers, and the valid delivery location countries for those suppliers. If no countries are defined for a supplier to deliver, the shipper delivers to all countries.

If a shipping method is defined by the administrator for a specific supplier and a specific delivery location, it displays to the shopper during checkout. When multiple shipping methods are available, the shopper can select any one for the purchase.

## Shipping method requirements during checkout

The shopper must select the shipping method, if applicable, during quick and full checkout to proceed. In full checkout, it is a required field on the Delivery date page.

A shipping method is available for selection during checkout if both of the following conditions are met:

-   The supplier in the given shipping method is listed in that shipping method's **Supplier** field.
-   The delivery location country in the given shipping method is listed in the shipping method's **Supplier delivers to** field.

## Shipping method storage and references

Shipping method is stored in each cart line and purchase line. It is also stored on each purchase requisition generated during full checkout, and is referenced in the purchase order and purchase order lines.

Shipping method is one criterion for grouping purchase requisitions, along with supplier, business owner, and blanket requisition. All purchase lines with the same shipping method are grouped together.

**Parent Topic:**[Complete your checkout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/complete-your-checkout.md)

