---
title: Create a configurable pricing plan
description: Create a configurable pricing plan by copying the default pricing plan provided in Pricing Management.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configurable pricing plans, Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create a configurable pricing plan

Create a configurable pricing plan by copying the default pricing plan provided in Pricing Management.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Pricing Plans**.

3.  Select the default pricing plan and select **Copy**.

    The copy of the default pricing plan opens in a new tab in the Draft state.

4.  Provide the pricing plan details:

    1.  Enter the **Name** of the pricing plan.

    2.  If you want price adjustments to be applied after price overrides, select the **Apply adjustments after price override** option.

        If you select this option, after the system applies a price override, any remaining pricing steps are run. If you don't select this option, any pricing steps scheduled after the price override is applied are not run.

    3.  Enter a new **Description** for the custom pricing plan.

5.  Select **Save**.

    The configurable pricing plan is created with the **Name** that you provided.


## What to do next

[Add or change a pricing plan step](add-pricing-step.md).

