---
title: Price and quantity ramps
description: Price and quantity ramps enable sales agents to set incremental increases in product pricing and quantity deals over the duration of a customer contract or subscription period.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-09"
reading_time_minutes: 4
breadcrumb: [Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Price and quantity ramps

Price and quantity ramps enable sales agents to set incremental increases in product pricing and quantity deals over the duration of a customer contract or subscription period.

## How ramps work

Different product adoption scenarios by customers can affect product pricing and quantities for subscription products or products under contract. For example, customers might want to scale their purchases over time, based on product use that increases annually as the company grows. Changes to products in subscriptions or contracts, such as changes to product characteristics or quantity, can cause pricing or quantity increases that must be applied.

Ramps provide a flexible pricing structure for sales agents to schedule pricing and quantity increases over specific time periods, called ramp segments. During the quote process, sales agents can create ramps for configurable products.

**Note:** Products that can have ramps must have the **Price method** set to Recurring and the **Enable ramps** option selected. Your product catalog admin sets these options when [creating a product offering](../task/som-create-product-offering.md).

The following example shows the ramp settings used to create ramps for a configurable product offering. The Price ramp details section displays the ramp segments that are generated automatically for the configurable product and its child lines.

![Ramp settings for a quote line of a parent product offerings that are used to generate the ramp segments and associated pricing for the parent and child quote lines.](../image/price-ramps-quote-details.png "Ramps for a configurable product offering")

Sales agents provide the following items to generate the ramps for a quote line:

-   **Start date** and **End date**. The default dates come from the quote line. The agent can enter a different start or end date, which the system uses to update the settings accordingly. These dates are used with the **Term** to calculate the ramp segments. The start date is used as the starting date for the first ramp segment.
-   **Ramp type**: Yearly or quarterly.
-   **Term**: Length of time, in months, for the ramps. The maximum term is 60 months. The Term is used with the Ramp type \(Start date and End date\) to determine the segments created.
-   **Annual % increase**: The percentage increase to be applied annually. The annual percentage increase is applied after the completion of the first year and is cascaded to all quote lines.
-   **Segment**: The number of time periods in the ramp to be created. Segments are determined as follows:
    -   Yearly ramp type: If the **Term** is a multiple of 12, the number of segments created is equal to the term/12. Each segment term is 12 months. If the **Term** isn’t a multiple of 12, the number of segments is term/12 +1, where the first segment is less than 12 months, but the other segments are 12 months each. Also, the first segment can be partial months.
    -   Quarterly ramp type: If the **Term** is a multiple of 3, the number of segments isn’t equal to term/3. Each individual segment term is 3 months. If the term isn’t a multiple of 3, the number of segments is equal to \(Term/3+1\) with the first segment less than 3 months while the rest of the segments are 3 months each. The first segment can be partial months, such as 8 months, 5 days based on the **Start date** and **End date**.

## Ramp generation and validation

For bundled products, the ramps generated for the parent line and its child lines have segments with the same ramp type \(yearly or quarterly\) and term.

-   If the parent line has a ramp, ramps are created automatically for all the child lines.
-   If the parent line isn’t ramped, all the child offers can be ramped independently.

## Ramp benefits

Ramps provide the following benefits:

-   Flexible pricing structures for customers, to align with their product adoption phases. For example, you can start with lower product pricing in the first ramp segment, to reduce initial costs and overcome buyer hesitancy.
-   Scaled revenue optimized over time as product usage grows.
-   Automatic calculations of ramp segments and pricing, minimizing errors in manual calculations made by sales agents.

## Ramp limitations

Ramps have certain limitations.

-   Ramps aren't supported for these features:
    -   Quotes of types sale agreement
    -   Multiple configurations
    -   Product inventory \(not applicable\)
-   Ramps for order lines are displayed, but order changes to ramps by order agents aren't supported.
-   Sold products that have ramps are supported, but Modify, Add, Change, Delete \(MACD\) operations for sold product aren't supported.

## Setting up ramps

Configuring ramps involves the following tasks:

<table id="table_xrz_tzj_dcc"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

[Enable ramps in product offerings](../task/som-create-product-offering.md)

</td><td>

When creating a configurable product offering: -   Set the **Pricing method** to Recurring, which makes the **Enable ramps** option available.
-   Select the **Enable ramps** option, which lets sales agents create ramps for the offering in a quote line.

</td><td>

Product catalog admin

</td></tr><tr><td>

[Add price ramps on a quote line item](../task/add-price-ramps-on-a-quote-line-item.md)

</td><td>

Define the ramp settings for the quote line and generate the ramps. After creating the ramps, agents can update the settings, such as the **Ramp type** or **Annual % increase** to recalculate the ramp segments automatically.

</td><td>

Sales agent

</td></tr></tbody>
</table>