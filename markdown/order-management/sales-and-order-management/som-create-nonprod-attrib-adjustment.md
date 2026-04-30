---
title: Create a non-product attribute pricing adjustment
description: Create a pricing adjustment for a product offering based on non-product characteristics, such as billing state or shipping zip code. You use the Standard Price Adjustment Matrix to define the pricing adjustment.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a non-product attribute pricing adjustment

Create a pricing adjustment for a product offering based on non-product characteristics, such as billing state or shipping zip code. You use the Standard Price Adjustment Matrix to define the pricing adjustment.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator, sn\_csm\_pricing\_pricelist\_manager

## About this task

Non-product attributes are represented as context variables, which identify non-product characteristics, such as account, shipping state, and product offering. Pricing Management provides a set of default context variables for non-product attributes. You can view the list of context variables for non-product attributes in the **Context variables** field in the Standard Price Adjustment Rule Matrix. You can also review a list of system-defined context variables in the Context Variables \[sn\_csm\_ctxrul\_mgt\_context\_variable\] table.

However, if you have a non-product attribute that is not available as a default context variable, such as sales channel, your system administrator can [create a custom context variable](som-create-context-variable.md) for that attribute. You can then use the custom context variable as an input in the decision table for the Standard Price Adjustment Matrix.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select Standard Price Adjustment Matrix.

4.  If you want to remove any of the context variables in the Content variables section In the Rule Matrix Standard Price Adjustment Matrix record, delete the pills that represent context variables for non-product attributes.

5.  If you have a large number of rows in the decision table and you want to optimize rule matrix performance, in **Query optimization variables**, select one or more context variables that the system uses to filter the pricing decision table rows that are evaluated.

6.  Select the option in **Rule selection criteria** that indicates whether single or multiple rules are applied in the Standard Adjustment Matrix.

    If multiple rules match and the option is marked true, all applicable pricing rules are applied when evaluating adjustments for product offers. If the option isn’t selected, the first rule based on priority is applied for adjustment calculation.

7.  Select **Edit Rule**.

    The Decision Table for the Standard Price Adjustment Matrix opens in Workflow Studio and displays the inputs, which are the default non-product characteristics available, and the decision table section that contains the columns for setting the non-product attribute adjustment rule conditions.

8.  If you have a custom context variable to add as an input, select **+Add** and add the custom variable **Label**, **Type**, **Reference** \(if applicable\), **Mandatory** indicator, and **Add condition column**, which adds the variable to the Conditions section.

9.  In the decision table, set the pricing rule for the non-product attribute:

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the row, select the columns for the non-product attributes to be applied, such as **Shipping State** and **Account**, and select the appropriate values.

    3.  In the Results section, select the **Adjustment Type** column and choose the type of adjustment, for example Markdown % or Markdown amount.

    4.  In the **Adjustment Value** column, enter the adjustment amount.

    5.  In the **Adjustment Description** column, enter a brief description of the adjustment, for example, Adjustment for state location.

    6.  Select **Save**.

10. Select **Publish** to apply the pricing rule for the non-product attribute.

    The adjustments are available to sales or order agents when working on quotes or orders.


