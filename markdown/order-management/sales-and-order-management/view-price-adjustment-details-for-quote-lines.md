---
title: View price adjustment breakdown on a quote line item
description: Sales agents can view the price adjustments that were applied to the base price in the price list to reflect discounts, surcharges, or other pricing strategies, and see how the net price was calculated while processing a quote.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-04-28"
reading_time_minutes: 2
breadcrumb: [Using Quote Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# View price adjustment breakdown on a quote line item

Sales agents can view the price adjustments that were applied to the base price in the price list to reflect discounts, surcharges, or other pricing strategies, and see how the net price was calculated while processing a quote.

## Where to find the price adjustment details

The unit base price, unit list price, and unit adjustment details are listed on the **Pricing** section of the Quote Line Item Details page.

The Price Adjustments tab on the quote line item provides the following information.

<table id="table_u45_jmr_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

ID of the price adjustment record.

</td></tr><tr><td>

Short description

</td><td>

Description of the price adjustment.

</td></tr><tr><td>

Sequence

</td><td>

Number of the pricing plan step used to generate the adjustment.

</td></tr><tr><td>

Adjustment source

</td><td>

Origin of the price adjustment.-   Auto: Adjustment applied automatically by pricing plan, and can be defined using standard adjustment matrices or via extension points, such as PricingAdjustmentExtensionPoint.
-   Manual: Adjustment made by agent.

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

Price that is calculated after the adjustment is applied. This could be the List Price or Net Price.

</td></tr><tr><td>

Adjustment value

</td><td>

Percentage or absolute amount of adjustment that is applied to the price.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of items in the quote line.

</td></tr><tr><td>

Amount

</td><td>

Adjustment applied to the original price in currency format.

</td></tr><tr><td>

Total amount

</td><td>

Quantity multiplied by the amount.

</td></tr><tr><td>

Unit running price

</td><td>

Unit price after applying the adjustment to the quote line.

</td></tr></tbody>
</table>## Price adjustment example

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

