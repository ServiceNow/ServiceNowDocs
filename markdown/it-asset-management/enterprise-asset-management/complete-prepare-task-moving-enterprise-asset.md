---
title: Complete the Prepare task for a moving enterprise asset
description: Complete the Prepare task for an enterprise asset so that you can proceed with moving the asset between locations.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Completing an enterprise asset move order, Managing enterprise asset move orders, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Complete the Prepare task for a moving enterprise asset

Complete the Prepare task for an enterprise asset so that you can proceed with moving the asset between locations.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager, sn\_eam.enterprise\_admin, or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, navigate to **Asset operations** &gt; **Moves** &gt; **Move orders**.

2.  From the list of available move orders, select the move order that you want to complete.

    The move order record opens.

3.  On the move order record, select the **Enterprise move lines** tab.

4.  From the list of available enterprise move lines, select the enterprise move line for the enterprise asset that you want to move.

    The enterprise move line record opens.

5.  On the **Enterprise move tasks** tab, select the task number for the **Prepare** task.

    Alternatively, select the task number that is displayed in the **Current task** field of the enterprise move line record header.![Current task field.](../image/current-task-move-orders.png)

    The Prepare task opens.

6.  On the **Details** tab of the Prepare task, fill in the fields.

<table id="table_vxh_vyg_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Enterprise move task

</td></tr><tr><td>

Assignment group

</td><td>

Group that the task is assigned to. This field populates automatically based on the group that the entire move order is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User who the task is assigned to. This field populates automatically based on the user who the entire move order is assigned to.

</td></tr><tr><td>

Scheduled date

</td><td>

Date and time at which the task is scheduled to be completed.

</td></tr><tr><td>

Priority

</td><td>

Priority of the task.

</td></tr><tr><td>

Move type

</td><td>

Type of enterprise asset move. Select one of the following options:-   **Local Move**: Option to move the enterprise asset to a different location without shipping it.
-   **Ship**: Option to ship the enterprise asset to a different location.


</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>7.  Select **Close Task**.


## Result

The Prepare task is automatically updated with a state of Closed Complete.

If you set the **Move type** field to **Local Move**, the Enterprise Asset Management application automatically generates a corresponding Local move task for the enterprise move line. If you set the **Move type** field to **Ship**, the Enterprise Asset Management application automatically generates a corresponding Ship task for the enterprise move line.

## What to do next

If you set the **Move type** field to **Local Move**, proceed to [Complete the local move for an enterprise asset](complete-local-move-enterprise-asset.md) to complete the move.

If you set the **Move type** field to **Ship**, proceed to [Complete the shipment for a moving enterprise asset](complete-shipment-moving-enterprise-asset.md) to complete the shipment.

**Parent Topic:**[Completing an enterprise asset move order](../concept/completing-enterprise-asset-move-order.md)

