---
title: Create and publish a product attribute-based pricing adjustment
description: Create a pricing adjustment for a product offering based on its product characteristics, such as the product size or color. A pricing adjustment can be a markup or markdown percentage, amount, or a pricing override.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create and publish a product attribute-based pricing adjustment

Create a pricing adjustment for a product offering based on its product characteristics, such as the product size or color. A pricing adjustment can be a markup or markdown percentage, amount, or a pricing override.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## About this task

In this task, you specify the product characteristics to which the pricing adjustment applies. Then you use a decision table to set the attribute adjustment rule, which defines the conditions for applying the pricing adjustment. For more information on using decision tables, see [Using decision tables](https://www.servicenow.com/docs/access?context=using-decision-builder&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Pricing** &gt; **Attribute Adjustments**.

3.  In the Pricing - Attribute Adjustments list, select **New**.

4.  On the Attribute Adjustment form, specify the product characteristics used to determine the adjustment:

    1.  Enter the **Name** of the attribute adjustment rule, for example, Make and Model selection.

    2.  If you want to change the system-assigned **Code** based on the attribute adjustment name, enter a different alphanumeric value.

    3.  If you want the adjustment to apply to all price lists, select **Apply to all Price Lists**.

    4.  Select the **Product offering** to which this adjustment applies.

    5.  If this attribute adjustment applies to a specific price list line and not all price lists, select the **Price list line**.

    6.  Select the **Start Date** that this attribute adjustment begins.

    7.  Select the **End Date** that this attribute adjustment ends, if applicable.

    8.  Unlock the **Product Characteristics** field and select the product characteristics to be used to differentiate the product price.

    9.  Select **Save**.

5.  In the Attribute Adjustment, select **Create Rule**.

    The Decision Table for the adjustment opens in Workflow Studio and displays the inputs, which are the product characteristics that you selected, and the decision table that contains the columns for setting the attribute adjustment rule conditions.

6.  Set the attribute pricing rule:

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the row, select an attribute column and select the appropriate value.

        For example, if a product has attribute columns labeled **Make** and **Model**, select each column and then select the appropriate value.

    3.  In the Results section, select the **Adjustment Type** column and choose the type of adjustment, for example Markdown % or Markdown amount.

    4.  In the **Adjustment Value** column, enter the adjustment amount.

    5.  Select **Save**.

        The adjustments are made to the price lists or the price list line, depending on the options selected in step 3.

7.  Test your decision table.

    For more information on testing your decision table before publishing it, see [Test a decision table in Workflow Studio](https://www.servicenow.com/docs/access?context=test-decision-table-in-decision-builder&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

8.  In the **Details** tab for the attribute adjustment, select **Publish**.

    The pricing attribute adjustment is available to agents when they create an opportunity, quote, or an order.


