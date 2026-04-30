---
title: View asset usage
description: The Field Service Management application tracks the consumable and non-consumable parts that are used or changed during the execution of work order tasks.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Execute work order tasks, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# View asset usage

The Field Service Management application tracks the consumable and non-consumable parts that are used or changed during the execution of work order tasks.

## Before you begin

Role required: wm\_agent

## About this task

The **Asset Usages** related list on the Work Order Task form displays the assets that are used during the execution of a task and also any existing assets that are removed from the task location.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Assigned to me**.

2.  Open a work order task.

3.  Select the **Asset Usages** related list.

    The possible statuses of an asset usage are listed in the following table.

<table id="table_ghg_xyc_kyb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Used

</td><td>

When an agent records the use of an asset, the asset is added to the Asset Usages related list with a status of **Used**. Non-consumable assets are marked as being **In Use** and assigned to the caller identified on the work order.

 Consumable assets are marked as **Consumed**.

</td></tr><tr><td>

Not used

</td><td>

When a transfer order line is delivered to an agent, a new asset usage record is created with a status of **Not Used**. If the agent does not use the asset and the work order task is closed, the asset usage record remains **Not Used**. The asset is marked as **In Stock Available** in the agent's personal stockroom.

</td></tr><tr><td>

Removed

</td><td>

When an agent records the removal of an asset, the asset is added to the Asset Usages related list with a status of **Removed**. If an asset is removed because it is not working, it should be marked as **Defective**. If an asset is not faulty, it must be marked as **Available**.

</td></tr></tbody>
</table>
