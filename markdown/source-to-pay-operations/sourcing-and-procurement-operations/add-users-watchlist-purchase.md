---
title: Add users to the watchlist of the purchase
description: You can add one or more users to the watchlist of the purchase request. The users on the Watchlist receive email notifications when specific conditions are fulfilled and the purchase request status is updated.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-10-17"
reading_time_minutes: 2
breadcrumb: [Provide a reason for your purchase, Complete your checkout, Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add users to the watchlist of the purchase

You can add one or more users to the watchlist of the purchase request. The users on the Watchlist receive email notifications when specific conditions are fulfilled and the purchase request status is updated.

## Before you begin

Role required: sn\_shop.shopper

## About this task

You can view and edit the **Watchlist** either from the **Reason for purchase** page or on the Purchase requisition under **My Purchases** in the Shopping hub. For more information, see [Activity stream](../concept/activity-stream.md). By default, you can add up to 20 users in the watchlist. You can modify this value by configuring the system properties. For more information, see [Components installed with Sourcing and Procurement Operations](../reference/installed-with-FSC.md).

**Note:** This limit for the number of users on the watchlist is applicable only while making the purchase request. You can add more users to the watchlist after the purchase request is created. However, you can add more users only at the purchase requisitions page.

## Procedure

1.  In the Reason for purchase page, if you're on the Apply to **Entire purchase** view, perform the following steps:

    1.  On the **Watchlist** field, select one or more users to the watchlist of the purchase request using the search option.

    2.  Select **Save Watchlist**.

        This watchlist applies to the **Entire purchase**, and therefore the watchlist is also applicable to the entire purchase request.

        ![Add users to the watchlist of the entire purchase](../../source-to-pay-operations/image/spo-complete-checkout-watchlist2.png "Add users to the watchlist of the entire purchase")

2.  In the Reason for purchase page, if you're on the Apply to **Product** view, perform the following steps:

    1.  On the **Watchlist** field of each product or item, select one or more users to the watchlist of the purchase request using the search option.

    2.  Select **Save Watchlist**.

        The users on the watchlist for each product or item will be combined into one purchase request and then cascaded to the header level. You can verify this by checking the My purchases page.

        ![Add users to the watchlist of the products](../../source-to-pay-operations/image/spo-complete-checkout-watchlist.png "Add users to the watchlist of the products")

    3.  Similarly, you can add users to the watchlist of the purchase request of other products/items.


**Parent Topic:**[Provide a reason for your purchase](provide-reason-for-purchase.md)

