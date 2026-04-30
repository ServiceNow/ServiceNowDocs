---
title: Copy a cost book
description: Duplicate a cost book and its cost book lines.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Copy a cost book

Duplicate a cost book and its cost book lines.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator, sn\_csm\_pricing\_pricelist\_manager

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Pricing** &gt; **Cost Books**.

3.  Select the published cost book to be copied and select **Copy**.

    The state changes to Copy in Progress and a message indicates that the copy is starting. Each cost book line is copied asynchronously, but you can refresh the page to see the cost book lines copied. When the copy process completes, the following occurs:

    -   The copied cost book is available in the Draft state and opens in a new tab.
    -   Any errors that occurred during the copy process, for example a cost book line doesn’t get copied, are displayed in a message in the copied cost book list.
4.  Select **Save**.

    When the cost book is in the Draft state, you can add cost book lines or delete the cost book. When you finish any changes to the copied cost book, you can publish it so that it's available for use and retire the former cost book.


