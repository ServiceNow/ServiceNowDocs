---
title: Handling fees
description: As an administrator, you can configure the conditions of a purchase request, which when met, adds a handling fee to that purchase request. Any field on the Purchase Request table can be used as part of the conditions to determine if a handling fee is to be applied for a purchase.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Purchase requisition, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Handling fees

As an administrator, you can configure the conditions of a purchase request, which when met, adds a handling fee to that purchase request. Any field on the Purchase Request table can be used as part of the conditions to determine if a handling fee is to be applied for a purchase.

If multiple handling fees are generated based on the configurable conditions, the handling fee with the lowest rank is applied. A Procurement Administrator can leverage the Pricing table to apply handling fee pricing. In the Pricing table, handling fees can be set as a fixed price or as a percentage-based price. When percentage-based pricing is not applied, the handling fee line amount is a percentage of the total amount of all the lines on the purchase request.

If there is a handling fee rule associated with a purchase requisition, a new purchase line is created with product type as handling fee. You can also view the details of this view-only handling fee purchase line from the **My purchases** tab.

## Shipping method

As an administrator, you can create shipping methods and associate them with various suppliers and delivery locations. If a shipping method is defined by the admin for a specific supplier and a specific delivery location, it is prompted to the shopper during checkout. When multiple shipping methods are available, the user can select any one for the purchase. Shipping method is only applicable for product type goods. Shipping method records store the details of the carrier, the applicable suppliers, and the valid delivery location countries for those suppliers. If no countries are defined for a supplier to deliver, the shipper delivers to all countries.

The shopper is required to select the shipping method, if applicable, during both quick and full checkout to proceed. In full checkout, it is a mandatory field on the Delivery date page. During checkout, a shipping method is available for selection if both these conditions are met:

-   If the supplier in a given shipping method is listed in that shipping method's **Supplier** field.
-   If the delivery location country in a given shipping method is listed in the **Supplier delivers to** field.

Shipping method is stored in each cart line and purchase line. It is also stored on each purchase requisition generated during full checkout, and is referenced in the purchase order and purchase order lines.

Shipping method is one of the criteria for grouping purchase requisitions, along with supplier, business owner, and blanket requisition. All purchase lines with the same shipping method are grouped together.

**Parent Topic:**[Purchase requisition](../reference/purchase-requisition.md)

