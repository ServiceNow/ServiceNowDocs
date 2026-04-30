---
title: Complete the Prepare task for a recalled enterprise asset
description: Complete the Prepare task for a recalled enterprise asset so that you can proceed with replacing, repairing, or retiring the given enterprise asset.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Completing a recall order for your enterprise assets, Managing recalled enterprise assets, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the Prepare task for a recalled enterprise asset

Complete the Prepare task for a recalled enterprise asset so that you can proceed with replacing, repairing, or retiring the given enterprise asset.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## About this task

**Important:** The Prepare task is applicable only to recall orders in which the **Remediation** field set to **Repair**, **Replace**, or **Retire**. If the **Remediation** field is set to **Notation**, you can proceed directly to the Notation task instead. See [Complete the Notation task for a recalled enterprise asset](complete-notation-task-recall-order.md) for more information on the Notation task.

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **Recall orders** tab.

3.  From the list of available recall orders, select the recall order that you want to complete.

    The recall order record opens.

4.  On the **Recalled Assets** tab of the recall order record, select the enterprise asset that you want to replace, repair, or retire.

    The recalled asset record opens.

5.  On the **Recall Tasks** tab, select the task number for the **Prepare** task.

    Alternatively, select the task number that is displayed in the **Current task** field of the recalled asset record header.![Current task field.](../image/current-task-recall-orders.png)

    The Prepare task opens.

6.  On the **Details** tab of the Prepare task, fill in the fields.

<table id="table_qhs_wnx_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Recall task details

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom of the recalled enterprise asset.**Note:** This field is editable only under the following conditions:

-   The **Remediation** field in the associated [recall order](submit-recall-order.md) is set to **Repair**. In addition, the **Remediation action** field in this Prepare task is set to **Off-site Repair**.
-   The **Remediation** field in the associated [recall order](submit-recall-order.md) is set to **Retire**.
 **Important:** If the recalled enterprise asset has not already been moved to a stockroom, you must move it to an available stockroom before you can proceed with the asset retirement or off-site repair.

</td></tr><tr><td>

Remediation action

</td><td>

Option that indicates how you want to proceed with the recall process for the enterprise asset.**Note:** This field is editable only if the **Remediation** field in the associated [recall order](submit-recall-order.md) is set to **Repair**.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the task is assigned.

</td></tr><tr><td>

Scheduled date

</td><td>

Date and time at which you plan to complete this task.

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
</table>7.  Close the Prepare task.

    You can either close the Prepare task for only the specified enterprise asset or bulk update and close the Prepare task for multiple enterprise assets.

    If you want to close the Prepare task for only the specified enterprise asset, select **Close Task**.

    If you want to bulk update and close the Prepare task for multiple enterprise assets, select **Include more assets**. When the Select assets for bulk update dialog box opens, select the check box for each enterprise asset that you want to bulk update and close the Prepare task for. Select **Close Task** to close the dialog box and return to the Prepare task.

    **Important:** You can bulk update the Prepare task only for enterprise assets that have the same task name, state, assignment group, and assigned to user.


## Result

The Prepare task automatically reloads with an updated state of Closed Complete.

If you are proceeding with an on-site repair, enterprise assets with a state of In use are updated with a state of In maintenance. In addition, enterprise assets with a state of In Stock are updated with a substate of Pending repair.

If you are proceeding with an off-site repair, enterprise assets with a state of either In use or In maintenance are updated with a state of In stock and a substate of Pending repair.

If you are proceeding with an asset replacement, enterprise assets with a state of In use are updated with a state of In maintenance. In addition, enterprise assets with a state of In stock are updated with a substate of Pending repair.

If you are proceeding with an asset retirement, enterprise assets are updated with a state of In stock and substate of Pending disposal.

## What to do next

Complete all subsequent replacement, repair, or retirement tasks.

**Parent Topic:**[Completing a recall order for your enterprise assets](../concept/completing-recall-order-enterprise-assets.md)

