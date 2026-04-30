---
title: Create a drop off list
description: Agents can create a drop off list of assets at any time.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using drop off lists, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Create a drop off list

Agents can create a drop off list of assets at any time.

## Before you begin

Role required: wm\_agent

## About this task

As an example, the agent might have several assets that were removed when completing a work order task and all of the assets need to be returned to a different stockroom.

After creating a drop-off list, there are two ways to add items to the list.

-   Use the **Add Defective** button to add items that are in their personal stockroom with a substate of **Defective**. For more information about defective items, see [Recording Asset Usage](t_RecordAssetUsage.md).
-   Create a transfer order line for an item in the personal stockroom.

    The item cannot have a substate of **Reserved** or **Defective**, and cannot already be included on another drop off list.


## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Pick Up/Drop Off** &gt; **Create Drop Off List**.

2.  Select a **To stockroom**.

    ![drop off list form](../../field-service-management/image/drop-off.png)

3.  Click **Submit**.

4.  Do one or both of the following:

    -   Click **Add Defective** to add all defective items in your personal stockroom to the drop off list.
    -   In the **Transfer Order Lines** related list, click **New**, select a **Model**, and click **Submit**.

        Only items in an agent's personal stockroom that are not reserved, not defective, and not included on another drop off list are available for selection.


