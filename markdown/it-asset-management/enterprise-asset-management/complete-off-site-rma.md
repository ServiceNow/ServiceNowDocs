---
title: Complete the RMA process for a defective enterprise asset through an off-site replacement or repair
description: Work with your asset vendor to perform all tasks that are required for an off-site replacement or repair so that you can complete the RMA process for a defective enterprise asset. You must perform this set of tasks separately for each defective enterprise asset that requires an off-site replacement or repair.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Closing an RMA order, Return Merchandise Authorization \(RMA\), Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the RMA process for a defective enterprise asset through an off-site replacement or repair

Work with your asset vendor to perform all tasks that are required for an off-site replacement or repair so that you can complete the RMA process for a defective enterprise asset. You must perform this set of tasks separately for each defective enterprise asset that requires an off-site replacement or repair.

## Before you begin

Before you can proceed with the RMA process for a defective enterprise asset off-site, you must complete the Prepare task for the associated RMA order line. See [Complete the Prepare task for an RMA order line](complete-rma-assessment.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **RMA orders** tab.

3.  From the list of available RMA orders, select the RMA order that you want to close.

    The RMA order record opens.

4.  On the **RMA Order Lines** tab of the RMA order record, select the RMA order line for the enterprise asset that you want to replace or repair.

    The RMA order line record opens.

5.  Complete and close the Shipment task for the RMA order line.

    To successfully complete and close this task, you must ship the defective enterprise asset back to the asset vendor.

    1.  On the **RMA Line Tasks** tab of the RMA order line record, select the task number for the **Shipment** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the RMA order line record header.![Current task field.](../image/rma-order-line-details-header.png)

        The Shipment task opens.

    2.  On the **Details** tab of the Shipment task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |RMA Line Task Details|
        |State|State of the task.|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Work notes list|Users who receive notifications when work notes are added to the task.|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Shipment|
        |Carrier|Shipping carrier through which you shipped the defective enterprise asset.|
        |Ship date|Date on which you shipped the defective enterprise asset.|
        |Tracking number|Tracking number that enables you to track the status and location of the shipment.|
        |Notes|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Select **Close Task**.

    The Shipment task automatically closes with an updated state of Closed Complete.

6.  Complete and close the Vendor RMA decision task for the RMA order line.

    To successfully complete and close this task, the asset vendor must either repair the defective enterprise asset, replace the defective enterprise asset with a new asset, or reject the RMA.

    1.  On the **RMA Line Tasks** tab of the RMA order line record, select the task number for the **Vendor RMA decision** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the RMA order line record header.![Current task field.](../image/rma-order-line-details-header.png)

        The Vendor RMA decision task opens.

    2.  On the **Details** tab of the Vendor RMA decision task, fill in the fields.

<table id="table_adc_fyz_3tb"><thead><tr><th>

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

Action that the asset vendor performed on the defective enterprise asset. Select one of the following options:-   **Repair**: Option indicating that the asset vendor successfully repaired the defective enterprise asset.
-   **Replace**: Option indicating that the asset vendor is replacing the defective enterprise asset with a new functioning asset.
-   **Reject**: Option indicating that the asset vendor rejected the RMA for the defective enterprise asset.

If you select this option, the **Reject reason** field appears below the **RMA decision** field. In the **Reject reason** field, specify why the asset vendor rejected the RMA.

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

    The Vendor RMA decision task automatically closes with an updated state of Closed Complete.

7.  Complete and close the Receive task for the RMA order line.

    To successfully complete and close this task, you must receive the new, repaired, or rejected enterprise asset from the asset vendor.

    If you are receiving a new enterprise asset as a replacement for the defective enterprise asset, you must also create an asset record for the new enterprise asset. See [Create enterprise assets](create-asset-eam.md) for detailed instructions.

    **Note:** When you create the asset record for the new enterprise asset, you must set the **State** field to **In stock**. You must also verify that the **Acquisition method** field is set to **RMA Replacement.**

    1.  On the **RMA Line Tasks** tab of the RMA order line record, select the task number for the **Receive** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the RMA order line record header.![Current task field.](../image/rma-order-line-details-header.png)

        The Receive task opens.

    2.  On the **Details** tab of the Receive task, fill in the fields.

<table id="table_odh_vzz_3tb"><thead><tr><th>

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

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Receive

</td></tr><tr><td>

Asset received

</td><td>

Option that indicates if you received the new, repaired, or rejected enterprise asset from the asset vendor.To complete and close the Receive task, you must set this field to **Yes**.

</td></tr><tr><td>

Replacement asset stockroom**Note:** This field appears only if the asset vendor replaced the defective enterprise asset with a new one.

</td><td>

Stockroom that the new enterprise asset is located in.

</td></tr><tr><td>

Replacement asset**Note:** This field appears only if the asset vendor replaced the defective enterprise asset with a new one.

</td><td>

New enterprise asset that has replaced the defective enterprise asset.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>    3.  Select **Close Task**.

    The Receive task automatically closes with an updated state of Closed Complete.


## Result

The RMA order line moves to the **Completed** stage.

If the asset vendor successfully replaced the defective enterprise asset with a new one, the **Details** tab of the RMA order line automatically updates with information about the new enterprise asset, including the name, model, and stockroom of the asset. In addition, the Enterprise Asset Management application automatically retires the defective enterprise asset, triggering the **State** and **Substate** fields to change to **Retired** and **Vendor credit** in the corresponding asset record.

If the asset vendor successfully repaired the defective enterprise asset, the **State** and **Substate** fields change to **In stock** and **Available** in the corresponding asset record.

If the asset vendor rejected the RMA, the defective enterprise asset remains in the In stock state and Pending repair substate. You must submit a new RMA order to take additional action on the asset.

## What to do next

Complete the RMA process for any remaining RMA order lines within the RMA order. After all RMA order lines reach the Completed stage, the RMA order is closed.

**Parent Topic:**[Closing a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets](../concept/closing-rma-order.md)

