---
title: Create rules for calculating pricing of sold products with MACD changes
description: Set different price points for calculating the pricing of sold products that undergo MACD changes.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing the price basis for MACD products, Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create rules for calculating pricing of sold products with MACD changes

Set different price points for calculating the pricing of sold products that undergo MACD changes.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## About this task

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select Delta Price Treatment Matrix.

4.  In **Rule selection criteria**, select the option that indicates whether single or multiple rules are applied in the Delta Price Treatment Matrix.

    If multiple rules are applied, all applicable pricing rules are applied when determining the pricing for sold products. If the option is Single, the first rule based on rank is applied.

5.  Select **Edit Rule**.

    The Decision Table for the Delta Price Treatment Adjustment Matrix opens in Workflow Studio and displays the inputs, which include the Line Type and Action for MACD operations. These inputs are the fields \(columns\) for setting the conditions in the decision table.

    -   Inputs: Lists the default inputs **Line Type**,**Action**.
    -   Decision table: The conditions that you specify for the line types or MACD action, such as disconnect or suspend.
6.  In the Conditions section, select **Add new decision row**.


