---
title: Create pricing adjustments for bundled products
description: Define price adjustments for a product when it is sold as part of a product bundle. You use the Configuration Component Price Adjustment Matrix to set the price adjustments for child product offerings that are bundled under a parent product offering.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create pricing adjustments for bundled products

Define price adjustments for a product when it is sold as part of a product bundle. You use the Configuration Component Price Adjustment Matrix to set the price adjustments for child product offerings that are bundled under a parent product offering.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## About this task

A pricing adjustment can be a markup or markdown percentage, amount, or a pricing override of the standalone product list price.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select Configuration Component Price Adjustment Matrix.

4.  Select **Edit Rule**.

    The Decision Table for the Configuration Component Price Adjustment Matrix opens in Workflow Studio and displays the inputs, which include the parent product offering and its child product offerings that comprise the bundle, and the decision table section that contains the columns for setting the conditions and the pricing adjustments to be applied to the child product offerings in the bundle.

5.  In the decision table set the pricing rule for the child product offerings in the bundle:

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the row, select the columns for the product offerings to be applied and select the appropriate values.

    3.  In the Results section, select the **Adjustment Type** column and choose the type of adjustment, for example Markdown % or Markdown amount.

    4.  In the **Adjustment Value** column, enter the adjustment amount.

    5.  In the **Adjustment Description** column, enter a brief description of the adjustment.

        This description is copied to the adjustment record linked to the quote or order line when the product offer is added to the quote or order. Consider creating a description that is formatted with a unique ID followed by a text description. You can use the unique ID to audit the adjustment generated when the quote or order is being configured, and the agent can use the description to understand the reason for the adjustment.

    6.  Select **Save**.

    7.  Select **Publish**.

        The adjustments are available to sales or order agents when working on quotes or orders or to customers using the Business Portal to place orders.


