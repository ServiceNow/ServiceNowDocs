---
title: Create a product attribute-based pricing adjustment
description: Create a pricing adjustment for a product offering based on its product characteristics, such as the product size or color. A pricing adjustment can be a markup or markdown percentage, amount, or a pricing override.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a product attribute-based pricing adjustment

Create a pricing adjustment for a product offering based on its product characteristics, such as the product size or color. A pricing adjustment can be a markup or markdown percentage, amount, or a pricing override.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator, sn\_csm\_pricing.pricelist\_manager

## About this task

In this task, you specify the product characteristics to which the pricing adjustment applies. Next, you use a decision table to set the attribute adjustment rule, which defines the conditions for applying the pricing adjustment. For more information on using decision tables, see [Using decision tables](https://www.servicenow.com/docs/access?context=using-decision-builder&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Note:** Starting with Pricing Matrixes release v10.0.0, a decision rule row can have more than one condition.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Attribute Adjustments**.

3.  In the Pricing - Attribute Adjustments list, select **New**.

4.  On the Attribute Adjustment form, specify the product characteristics used to determine the adjustment:

    1.  Enter the **Name** of the attribute adjustment rule, for example, Make and Model selection.

    2.  If you want to change the system-assigned **Code** based on the attribute adjustment name, enter a different alphanumeric value.

    3.  Select Price as the **Type** of adjustment.

    4.  If you want the adjustment to apply to all price lists, select **Apply to all Price Lists**.

    5.  Select the **Product offering** to which this adjustment applies.

    6.  If this attribute adjustment applies to a specific price list line and not all price lists, select the **Price list line**.

    7.  Select the **Start Date** that this attribute adjustment begins.

    8.  Select the **End Date** that this attribute adjustment ends, if applicable.

    9.  In the **Product Characteristics** field, select the product characteristics to be used to differentiate the product price.

    10. Select **Save**.

5.  In the Attribute Adjustment, select **Create Rule**.

    The Decision Table for the adjustment opens in Workflow Studio and displays the inputs, which are the product characteristics that you selected, and the decision table that contains the columns for setting the attribute adjustment rule conditions.

6.  Set the attribute pricing rule:

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the row, select an attribute column and select the appropriate value.

        For example, if a product has attribute columns labeled **Make** and **Model**, select each column and then select the appropriate value.

        You can enter multiple rules with multiple conditions for a given product offering.

    3.  In the Results section, select the **Adjustment Type** column and choose the type of adjustment, for example Markdown % or Markdown amount.

    4.  In the **Adjustment Value** column, enter the adjustment amount.

    5.  Select **Save**.

        The adjustments are made to the price lists or the price list line, depending on the options selected in step 4f.

        **Note:** At transaction time, the Attribute Adjustment table does not support rule selection criteria set as single. It supports only multiple evaluations as true.

7.  Test your decision table.

    For more information on testing your decision table before publishing it, see [Test a decision table in Workflow Studio](https://www.servicenow.com/docs/access?context=test-decision-table-in-decision-builder&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

8.  In the **Details** tab for the attribute adjustment, select **Publish**.

    When a product offering is added to a transaction, such as a quote or order line, the pricing attribute adjustments are applied after the agent or customer selects the attribute options. For example, when agents or customers use the CPQ Configurator to add a configurable product offering, the base price of the product is displayed initially. After the appropriate attribute options are selected, the price adjustments for the selected attributes are applied to the base price of the product. The resulting price displayed is the list price of the product offering, based on attribute conditions and associated markup or markdown values set in the Attribute Adjustment decision table.


