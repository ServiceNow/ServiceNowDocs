---
title: Manually update transactions
description: Manually update imported software transactions that weren't automatically labeled with a software product and publisher to track all software spending.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management]
---

# Manually update transactions

Manually update imported software transactions that weren't automatically labeled with a software product and publisher to track all software spending.

## Before you begin

Role required: sam\_user

## About this task

Sometimes, Software Spend Detection can't match a transaction to a software publisher and product. If Software Spend Detection can identify the publisher but not the product, the transaction is categorized as Unnormalized in the list of products for that publisher in the Software Spend Detection dashboard. The transaction amount is added to the total cost for that publisher. If Software Spend Detection can't identify the publisher, the transaction is added to **Unnormalized Transactions** and is excluded from the Software Spend Detection dashboard. The transaction amount isn't included in any of the spend amounts shown on the dashboard.

## Procedure

1.  Navigate to **All** &gt; **Software Spend Detection** &gt; **Unnormalized Transactions**.

    **Note:** By default, this list shows only transactions identified as software by Software Spend Detection. To include transactions not identified as software, remove the filter condition **Is software = true**.

    ![Remove the Is software = true filter condition by selecting the arrow in the filter.](../image/spend-manually-update.gif)

2.  Select a transaction date.

3.  Select values for the **Publisher** and **Product** fields.

    **Note:** You can create software publishers and products directly from this form by selecting the Lookup using list icon \(![Lookup using list icon.](../../../common/image/List_SearchIcon.png)\) next to the field and then selecting **New**.

4.  Clear or select the **Is software** check box to indicate if the transaction is a software purchase.

5.  Select **Update**.

    The transaction is removed from the list of unnormalized transactions and is added to the Software Spend Detection dashboard.


**Parent Topic:**[Software Spend Detection](../concept/software-spend-detection.md)

