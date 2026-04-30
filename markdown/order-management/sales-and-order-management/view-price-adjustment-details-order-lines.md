---
title: Price adjustment breakdown on order lines
description: Order agents can view the price adjustments that were applied to the base price in the price list to reflect attribute adjustments and any custom adjustments that you added through the pricing plan, and see how the net price was calculated while processing orders.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-04-28"
reading_time_minutes: 2
breadcrumb: [Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Price adjustment breakdown on order lines

Order agents can view the price adjustments that were applied to the base price in the price list to reflect attribute adjustments and any custom adjustments that you added through the pricing plan, and see how the net price was calculated while processing orders.

## Where to find the price adjustment details

The unit base price, unit list price, and unit adjustment details are listed on the Pricing section of the Order Line Item Details page.![Pricing section on the Order Line Item Details page](../image/pricing-order-line-item.png)

The Price Adjustments tab on the order line item provides the following information.

<table id="table_d1l_hnq_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

ID of the price adjustment record.

</td></tr><tr><td>

Name

</td><td>

Name specified while creating the price adjustment.

</td></tr><tr><td>

Sequence

</td><td>

The number of the pricing plan step used to generate the adjustment. It helps the agent identify the order of operations for the pricing adjustments.

</td></tr><tr><td>

Adjustment source

</td><td>

Origin of the price adjustment.-   Auto: Adjustment applied automatically by pricing plan, and can be defined using standard adjustment matrices or via extension points, such as, PricingAdjustmentExtensionPoint.
-   Manual: Manual adjustment made by agent.

</td></tr><tr><td>

Adjustment type

</td><td>

-   Markdown %
-   Markdown amount
-   Markup %
-   Markup amount
-   Price override

</td></tr><tr><td>

Price point

</td><td>

Setup by the admin in the Pricing Plan for the adjustment step. This could be the List Price or Net Price.

</td></tr><tr><td>

Adjustment value

</td><td>

Percentage or absolute amount of adjustment that is applied to the price.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of items in the order line.

</td></tr><tr><td>

Amount

</td><td>

Price adjustment amount.

</td></tr><tr><td>

Total amount

</td><td>

Quantity multiplied by the amount.

</td></tr><tr><td>

Unit running price

</td><td>

Price calculated with the adjustment amount from the specific pricing plan step.

</td></tr></tbody>
</table>![List view of the Price adjustments tab for an order line item](../image/price-adjustment-order-line.png)

## Price adjustment example

To understand price adjustment and the terms used, let's consider a scenario where a customer is purchasing an API Edition license from a provider.

-   Unit Base Price: The price defined in the Price List, say $1000.
-   Attribute Adjustment: The customer opts for the "Professional Plus Edition" version of the product with Price Point as List Price which costs them additional $200.
-   Volume adjustment: The customer receives a discount of $50 when they purchase 100 licenses. Here as well, the Price Point is the List Price.
-   Price Point: The Price point is the entity on which the price adjustments were applied. It could be the List Price or Net Price.
-   Unit List Price: The Unit List Price is calculated as $1000 + $200 - $50 = $1150.
-   Customer also receives a premier account discount of $100 with Price Point as Net Price.
-   Unit Net Price: The Unit Net Price is the final price after all adjustments have been applied. This is calculated as $1150 - $100 = $1050.

**Parent Topic:**[Create an order in Order Management](som-create-product-order.md)

**Related topics**  


[Configurable pricing plans](../concept/configuring-pricing-plan.md)

