---
title: Shipping cost calculations
description: A framework to integrate shipping cost calculations into Sourcing and Purchasing Automation is implemented such that approvals can be done on the full value of purchases.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Shipping cost calculations

A framework to integrate shipping cost calculations into Sourcing and Purchasing Automation is implemented such that approvals can be done on the full value of purchases.

Shipping estimates can be provided by both the ShoppingHub administrator and the buyer.

## Shipping estimates from ShoppingHub administrator

A ShoppingHub administrator can set a default system-wide shipping estimate as a percentage. This can then be applied to all purchases that require shipping, when no other shipping estimates or data exist. This is enabled through a system property sn\_shop.default.shipping.estimate. Organizations that have a policy around an acceptable threshold shipping cost might want to enter the threshold in the sn\_shop.default.shipping.estimate.

A ShoppingHub administrator can also configure shipping estimates to be included in purchase requests for the approval process. This is enabled through a system property sn\_shop.shipping.estimate.inclusion, which is included in purchase request approvals. If this inclusion is marked as true, the shipping estimate from the cart line or checkout is included as a field in the purchase line and in the total amount in the purchase request, while the estimate in cost allocation is not considered. However, if this inclusion is marked as false, not only would shipping be excluded in the purchase request approval process, but also not calculated at checkout, even if data is included at the product, supplier, or system levels.

**Note:** When a purchase request becomes a purchase order, the shipping estimate is not included in the total amount.

## Shipping estimates from buyer

A buyer can set shipping estimates at the following levels:

-   Supplier:

    Set a standard percentage estimate for shipping costs from a specific supplier. This estimate is then applied to all the orders that require shipping from that supplier, which do not have any estimate at the product level. In the **Purchasing Automation** tab of the supplier record, enter a shipping estimate value in decimal in the **Default shipping estimate for products from this supplier \(calculated as percentage of negotiated unit price\)** field.

-   Product:

    Set a default shipping estimate for a supplier product record. This is then prioritized in estimating the shipping cost of a purchase over any supplier level estimate or default shipping estimate. In the **Purchasing Automation** tab of the supplier product record, enter a shipping estimate value in decimal in the **Default shipping estimate for this supplier product \(calculated as percentage of negotiated unit price\)** field.


**Note:** The entered decimal values are stored in percentage. For example, a shipping estimate value of 10.5 is stored as 10.5%.

-   **[Shipping cost calculation in cart line table](shipping-cost-calculation-cart-line.md)**  
If the item in your cart is a good, a cart line shipping estimate prioritization logic is used to calculate the estimated shipping cost. If the item in your cart is a service, the estimated shipping cost shows as 0.0 in your currency.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

