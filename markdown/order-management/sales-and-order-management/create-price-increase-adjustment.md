---
title: Create a price increase adjustment
description: Create a price increase adjustment such as an renewal uplift. Use the Price Increase Defaulting Matrix to define conditions that control the price increase applied.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Blended pricing for contract consolidation of subscription renewals, Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create a price increase adjustment

Create a price increase adjustment such as an renewal uplift. Use the Price Increase Defaulting Matrix to define conditions that control the price increase applied.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator or sn\_csm\_pricing\_pricelist\_manager

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Context Rule Management** &gt; **Rule Matrices**.

3.  In the Rule Matrices list, select Price Increase Defaulting Matrix.

    The matrix details are displayed.

4.  Select **Edit Rule** to define conditions for the price increase.

    The Decision Table for the adjustment opens in Workflow Studio and displays the inputs for the price increase, and the decision table that contains the columns for setting the price increase conditions.

5.  Set the default price increase rule.

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the row, select the input column and set the value for the condition.

        For example, if the input is **Account**, choose the customer account to which the adjustment applies.

    3.  In the **Price Increase Type** column, select the type of price increase, such as Renewal Uplift.

    4.  In the Results section, select the **Adjustment Type** column and choose the type of adjustment, for example Markdown % or Markdown amount.

    5.  In the **Adjustment Value** column, enter the adjustment amount.

    6.  Select **Save**.

6.  Select **Publish**.


## Result

The pricing increases, for example uplifts for contract renewals, are applied based on the conditions set in the Price Increase Defaulting Matrix.

