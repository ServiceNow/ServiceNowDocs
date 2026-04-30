---
title: Complete the RMA process for a defective enterprise asset through an on-site repair
description: Perform all tasks that are required for an on-site repair so that you can complete the RMA process for a defective enterprise asset. You must perform this set of tasks separately for each defective enterprise asset that requires an on-site repair.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Closing a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets, Requesting a Return Merchandise Authorization \(RMA\) for defective enterprise assets, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the RMA process for a defective enterprise asset through an on-site repair

Perform all tasks that are required for an on-site repair so that you can complete the RMA process for a defective enterprise asset. You must perform this set of tasks separately for each defective enterprise asset that requires an on-site repair.

## Before you begin

Before you can proceed with the RMA process for a defective enterprise asset on-site, you must complete the Prepare task for the associated RMA order line. See [Complete the Prepare task for an RMA order line](complete-rma-assessment.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **RMA orders** tab.

3.  From the list of available RMA orders, select the RMA order that you want to close.

    The RMA order record opens.

4.  On the **RMA Order Lines** tab of the RMA order record, select the RMA order line for the enterprise asset that you want to repair.

    The RMA order line record opens.

5.  Complete and close the On-site repair task for the RMA order line.

    To successfully complete and close this task, you must either repair the defective enterprise asset on-site, move the RMA process off-site with the asset vendor, or reject the on-site repair request.

    1.  On the **RMA Line Tasks** tab of the RMA order line record, select the task number for the **On-site repair** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the RMA order line record header.![Current task field.](../image/rma-order-line-details-header.png)

        The On-site repair task opens.

    2.  On the **Details** tab of the On-site repair task, fill in the fields.

<table id="table_qhs_wnx_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

RMA Line Task Details

</td></tr><tr><td>

State

</td><td>

State of the task.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the task is assigned.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications when work notes are added to the task.

</td></tr><tr><td>

RMA decision

</td><td>

Action that you performed on the defective enterprise asset. Select one of the following options:-   **Repair**: Option indicating that you successfully repaired the defective enterprise asset on-site.
-   **Off-site**: Option indicating that you are moving the RMA process off-site with the asset vendor. Select this option if you are unable to repair the defective enterprise asset on-site.
-   **Reject**: Option indicating that you rejected the on-site repair request.


</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>    3.  Select **Close Task**.

    The On-site repair task automatically closes with an updated state of Closed Complete.

    If you set the **RMA decision** field to **Off-site**, proceed to [Complete the RMA process for a defective enterprise asset through an off-site replacement or repair](complete-off-site-rma.md) to continue with the RMA process off-site.


## Result

If you successfully repaired the defective enterprise asset, the RMA order line moves to the Completed stage. In the corresponding asset record, the **State** field changes to **In stock** and the **Substate** field changes to **Available**.

If you moved the RMA process off-site, a Shipment task automatically populates on the **RMA Line Tasks** tab of the RMA order line. You must then ship the defective enterprise asset back to the asset vendor so that they can complete the remaining replacement or repair tasks off-site. See [Complete the RMA process for a defective enterprise asset through an off-site replacement or repair](complete-off-site-rma.md) for detailed instructions on how to replace or repair a defective enterprise asset off-site.

If you rejected the on-site repair request, the RMA order line moves to the Completed stage. However, the defective enterprise asset remains in the In stock state and Pending repair substate. You must submit a new RMA order to take additional action on the asset.

## What to do next

Complete the RMA process for any remaining RMA order lines within the RMA order. After all RMA order lines reach the Completed stage, the RMA order is closed.

**Parent Topic:**[Closing a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets](../concept/closing-rma-order.md)

