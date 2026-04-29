---
title: Add or change a pricing plan step
description: Add a pricing plan step to a configurable pricing plan that applies either a pricing matrix or a custom adjustment using the pricing extension point. You can also change certain items in an existing step, such as the sequence or type of matrix used, as well as specify conditions for running the step.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configurable pricing plans, Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Add or change a pricing plan step

Add a pricing plan step to a configurable pricing plan that applies either a pricing matrix or a custom adjustment using the pricing extension point. You can also change certain items in an existing step, such as the sequence or type of matrix used, as well as specify conditions for running the step.

## Before you begin

[Create a configurable pricing plan](create-custom-pricing-plan.md).

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## About this task

You can add or change a pricing plan step only when the configurable pricing plan is in the Draft state.

**Note:** The following steps in all pricing plans are fixed and can't be changed:

-   Initialize Pricing Context
-   Fetch Base Cost
-   Fetch Base List Price
-   Apply Attribute Adjustments

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Pricing Plans**.

3.  Select the configurable pricing plan to which steps are being added or changed.

4.  In the pricing plan, select the Pricing Plan Steps tab.

    -   To add a step, select **New**.
    -   To change a step, select the step number to be updated. If you need to delete a pricing adjustment step, see [Delete a pricing plan step](delete-pricing-plan-step.md).
5.  Fill in or change certain fields in the form.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System assigned number for the pricing plan step.

</td></tr><tr><td>

Name

</td><td>

Name of the step to be added.

</td></tr><tr><td>

Description

</td><td>

Brief description of the step.

</td></tr><tr><td>

Price point

</td><td>

Selling price for a product or service. Select one of the following:-   List Price: Standard selling price to be applied before any pricing adjustments.
-   Net Price: Final price to customer after predefined or negotiated adjustments have been subtracted.


</td></tr><tr><td>

Calculation type

</td><td>

Option for evaluating the result of the adjustment at each step. Select one of the following:-   Previous price point: When the Price Point is Net Price, the previous price point is List Price. The adjustment is applied to the List Price.
-   Rolling: When multiple adjustments exist, apply the subsequent adjustment to the price resulting from the previous adjustment to calculate the final net price.


</td></tr><tr><td>

Sequence

</td><td>

Number value indicating the order in which the step is to be applied.For example, if you're adding a step between two existing steps with sequence numbers 40 and 50 respectively, you could enter the sequence number 45 for the step.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the pricing plan step name.

</td></tr><tr><td>

Action

</td><td>

Option indicating the type of pricing adjustment to be run in the step. Select one of the following:-   Apply Matrix Adjustments: Run a pricing matrix.
-   Apply Custom Adjustments: Run a custom pricing adjustment using the PricingAdjustmentsExtensionPoint.


</td></tr><tr><td>

Rule matrix

</td><td>

Option that displays if you selected the Apply Matrix Adjustments action. Select the pricing matrix to be applied:-   [Configuration Component Price Adjustment Matrix](som-create-bundle-adjustment.md): Use this matrix to set the price adjustments for child product offerings that are bundled under a parent product offering.
-   [Standard Price Adjustment Matrix](som-create-nonprod-attrib-adjustment.md): Use this matrix to set a pricing adjustment for a product offering based on non-product characteristics, such as billing state or shipping zip code.
You can select the rule matrix link in the step to define the matrix.

</td></tr><tr><td>

Pricing plan

</td><td>

Name of the configurable pricing plan.

</td></tr><tr><td>

Extension point

</td><td>

Option that displays the PricingAdjustmentsExtensionPoint if you selected the Apply Custom Adjustments action.

</td></tr></tbody>
</table>6.  Specify certain conditions for running the step, if applicable.

    **Note:** Any conditions that aren't met, are ignored.

    |Type of condition|Description|
    |-----------------|-----------|
    |**Header condition**|Use the condition builder to add or change conditions that control when the step is run, based on the transaction header \(for example the header for an opportunity, quote, or order\). Specify the condition fields to be used, for example a context variable for transaction headers, product characteristics, or other objects such as account or product offering.|
    |**Line condition**|Use the condition filter to add or change conditions that control when the step is run, based on the transaction line \(for example an opportunity, quote, or order line\). Specify the condition fields to be use, such as a context variable for transaction lines, product characteristics, or other objects, such as account or product offering.|

7.  Select **Save**.

8.  To continue adding or changing steps, repeat steps 4 through 7.

    If you need to remove a step, see [Delete a pricing plan step](delete-pricing-plan-step.md).

9.  When you're finished adding or changing steps, select **Publish**.

    The configurable plan becomes the active pricing plan, and the former active plan is retired.


