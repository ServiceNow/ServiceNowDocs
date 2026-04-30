---
title: Sync a quote with an opportunity
description: Agents can sync quote information with an opportunity to ensure that information is consistent between both applications in Quote Management.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Quote Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Sync a quote with an opportunity

Agents can sync quote information with an opportunity to ensure that information is consistent between both applications in Quote Management.

## Before you begin

Role required: sales\_agent

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Quote** &gt; **All-Quotes** and select a quote that you want to sync with an opportunity.

3.  In the **Details** tab of the quote, go to the **Source Opportunity** option and choose the opportunity you want to sync with.

4.  Select **Save**.

    The **Enable sync** button is enabled.

5.  Select the **Enable Sync** option.

    Current Information and future changes to the quote are automatically synced. The following areas show the sync status.

    -   The **Sync** check box shows that the quote is synced.
    -   The **Sync** flag on the secondary header changes to **Yes**.
    -   The **Synced** column in the Quotes related list on the Opportunity record shows **Yes** when sync is activated and **No** when the quote isn’t synced.
6.  Turn off automatic sync by selecting the **Disable sync** button.

    **Note:** When sync is enabled, the following conditions occur:

    -   No changes can be made to that opportunity \(for example, adding line items, changing quantities\). ​
    -   Additional changes should be made to the quote record.
    -   The opportunity record is updated asynchronously with the latest product offerings and prices that are added to the quote.
    -   The synced opportunity state changes to closed when the quote is marked as complete

