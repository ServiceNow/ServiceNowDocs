---
title: Enable public access for a catalog item
description: Configure a catalog item to enable access for guest users.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enabling guest users to submit a catalog item on the Customer Service Portal, Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Enable public access for a catalog item

Configure a catalog item to enable access for guest users.

## Before you begin

Role required: admin, catalog\_admin

## About this task

By default, the catalog items aren’t available for guest users. To make the catalog item available, edit the Available for and Not Available for user criteria.

## Procedure

1.  Find the catalog items.

    1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

    2.  Search and select the required item.

2.  Make the item available for the guest user.

    1.  Select the **Available for** related list.

    2.  Select **Edit**.

    3.  Search and move **Guest User** from Collection to Service Category Request.

        ![showing moving guest user](../image/catalogitem-guestuser.png)

3.  Edit the **Not Available For** tab.

    1.  Select the **Not Available For** related list.

    2.  Select **Edit**.

    3.  Move **SNC External** \(if available\) from Not Available For to Collection.

    4.  Select **Save**.

4.  Select **Update**.


## Result

The catalog item is made public. The guest users can now view it.

