---
title: Copy a price list
description: Duplicate a published price list and its associated price list lines, attribute adjustments, and decision tables. You can copy a price list, update the pricing in the copied price list if needed, then publish it.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Copy a price list

Duplicate a published price list and its associated price list lines, attribute adjustments, and decision tables. You can copy a price list, update the pricing in the copied price list if needed, then publish it.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator, sn\_csm\_pricing.pricelist\_manager

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Price Lists**.

3.  Select the published price list to be copied and select **Copy**.

    The state changes to Copy in Progress and a message indicates that the copy is starting. You can't edit the price list, price list lines, any attribute adjustments, and related decision tables during the copy process. Each price list line and the other related pricing features are copied asynchronously. During the copy process, you can refresh the page to see the items copied. When the copy process completes, the following occurs:

    -   The copied price list is available in the Draft state and opens in a new tab.
    -   Any errors that occurred during the copy process, for example a price list line didn't get copied, are displayed in a message in the copied price list.
4.  Select **Save**.

    When the price list copy is in the Draft state, you can add or change price list lines or delete the price list. When you finish updating the copied price list, you can publish it so that it’s available for use.


