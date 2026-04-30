---
title: Price adjustment breakdown on order lines
description: Order agents can view the price adjustments that were applied to the base price in the price list to reflect attribute adjustments and any custom adjustments that you added through the pricing plan, and see how the net price was calculated while processing orders.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Price adjustment breakdown on order lines

Order agents can view the price adjustments that were applied to the base price in the price list to reflect attribute adjustments and any custom adjustments that you added through the pricing plan, and see how the net price was calculated while processing orders.

## Where to find the price adjustment details

The unit base price, unit list price, and unit adjustment details are listed on the Pricing section of the Order Line Item Details page.

The Price Adjustments tab on the Order Line Item page displays the manual price adjustments that were applied to an order line item. For information about the fields on the list view, see [Price adjustment fields](../reference/field-descriptions-customer-order-line-items.md#).

## Price adjustment example

To understand price adjustment and the terms used, let's consider a scenario where a customer is purchasing an API Edition license from a provider.

-   Unit Base Price: The price defined in the Price List, say $1000.
-   Attribute Adjustment: The customer opts for the "Professional Plus Edition" version of the product with Price Point as List Price which costs them additional $200.
-   Volume adjustment: The customer receives a discount of $50 when they purchase 100 licenses. Here as well, the Price Point is the List Price.
-   Price Point: The Price point is the entity on which the price adjustments were applied. It could be the List Price or Net Price.
-   Unit List Price: The Unit List Price is calculated as $1000 + $200 - $50 = $1150.
-   Customer also receives a premier account discount of $100 with Price Point as Net Price.
-   Unit Net Price: The Unit Net Price is the final price after all adjustments have been applied. This is calculated as $1150 - $100 = $1050.

**Related topics**  


[Configurable pricing plans](../concept/configuring-pricing-plan.md)

