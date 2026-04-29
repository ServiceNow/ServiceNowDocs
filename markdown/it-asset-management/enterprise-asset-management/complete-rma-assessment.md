---
title: Complete the Prepare task for an RMA order line
description: Complete the Prepare task for an RMA order line so that you can proceed with replacing or repairing the given enterprise asset. Alternatively, you can reject the RMA to avoid taking any action on the given enterprise asset.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Closing an RMA order, Return Merchandise Authorization \(RMA\), Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the Prepare task for an RMA order line

Complete the Prepare task for an RMA order line so that you can proceed with replacing or repairing the given enterprise asset. Alternatively, you can reject the RMA to avoid taking any action on the given enterprise asset.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, navigate to the Inventory view.

2.  Select the **RMA orders** tab.

3.  From the list of available RMA orders, select the RMA order that you want to close.

    The RMA order record opens.

4.  On the **RMA Order Lines** tab of the RMA order record, select the RMA order line of the enterprise asset that you want to replace, repair, or take no action on.

    The RMA order line record opens.

5.  On the **RMA Line Tasks** tab of the RMA order line record, select the task number for the **Prepare** task.

    Alternatively, select the task number that is displayed in the **Current task** field of the RMA order line record header.![Current task field.](../image/rma-order-line-details-header.png)

    The Prepare task opens.

6.  On the **Details** tab of the Prepare task, fill in the fields.

<table id="table_qhs_wnx_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

RMA Line Task Details

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom that the defective enterprise asset is located in. This field populates automatically.

</td></tr><tr><td>

Vendor

</td><td>

Vendor of the defective enterprise asset. This field populates automatically.

</td></tr><tr><td>

Vendor RMA number

</td><td>

RMA reference number provided by the asset vendor.

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

RMA type

</td><td>

Option that indicates how you want to proceed with the RMA process for the defective enterprise asset. Select one of the following options:-   **On-site**: Option to complete the RMA process on-site. With this option, you can repair the defective enterprise asset on-site.
-   **Off-site**: Option to complete the RMA process off-site with the asset vendor. With this option, the defective enterprise asset can be replaced or repaired off-site by the asset vendor.
-   **Reject**: Option to reject the RMA for the defective enterprise asset. With this option, you can avoid taking any action on the defective enterprise asset.


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
</table>7.  Select **Close Task**.


## Result

The Prepare task automatically closes with an updated state of Closed Complete.

## What to do next

If you set the **RMA type** field to **On-site** or **Off-site**, complete all subsequent replacement or repair tasks to move the RMA order line to the **Completed** stage. If you set the **RMA type** field to **Reject**, the RMA order line automatically moves to the Completed stage, and no further action is required.

**Parent Topic:**[Closing a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets](../concept/closing-rma-order.md)

