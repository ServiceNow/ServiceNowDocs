---
title: Complete the Ship task for a defective Device as a Service DaaS asset
description: If you want to perform a replacement or an off-site repair for a defective DaaS asset, you must complete the associated Ship task by having the customer ship the asset to you. If you choose to repair the asset, you must complete the associated Ship task by shipping the asset back to the customer after a successful repair.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Complete the Ship task for a defective Device as a Service DaaS asset

If you want to perform a replacement or an off-site repair for a defective DaaS asset, you must complete the associated Ship task by having the customer ship the asset to you. If you choose to repair the asset, you must complete the associated Ship task by shipping the asset back to the customer after a successful repair.

## Before you begin

Before you can begin the Ship task, you must complete the preceding task.

-   If you are performing an on-site replacement, you must complete the preceding Evaluate RMA asset task by evaluating the asset and indicating that it must be replaced. For detailed instructions, see [Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset](evaluate-daas-asset-rma-response-order.md).
-   If you are performing an off-site repair or replacement, you must complete the preceding RMA assessment task by assessing the asset and indicating that it must be repaired or replaced off-site. For detailed instructions, see [Complete the RMA assessment task for a defective Device as a Service DaaS asset](assess-daas-asset-rma-response-order.md).
-   Before you can ship a repaired asset back to a customer, you must complete the preceding Evaluate asset task by evaluating the asset and verifying that it was repaired successfully. For detailed instructions, see [Complete the Evaluate asset task for a defective Device as a Service DaaS asset](evaluate-repaired-daas-asset-rma-response-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d137061e122">

Navigation option

</th><th align="left" id="d137061e125">

Procedure

</th></tr></thead><tbody><tr><td id="d137061e131">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to ship the asset for.

**Note:** You must select an order line that you have already completed the Evaluate RMA asset, RMA assessment, or Evaluate asset task for.

5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d137061e175">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to ship the asset for.

**Note:** You must select an order line that you have already completed the Evaluate RMA asset, RMA assessment, or Evaluate asset task for.

3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d137061e210">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Ship task that you want to complete.

4.  On the **Details** tab of the Ship task, fill in the fields.

<table id="table_xyl_nls_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Due date

</td><td>

Date and time at which you must complete the task.**Note:** This field is editable only if you are shipping the asset to the customer.

</td></tr><tr><td>

Shipping carrier

</td><td>

Shipping carrier through which you are shipping the asset. For example, **DHL**.

</td></tr><tr><td>

Ship from

</td><td>

Geographic location that you are shipping the asset from.

</td></tr><tr><td>

Ship date

</td><td>

Date and time at which you shipped the asset.

</td></tr><tr><td>

Assignment group

</td><td>

Group that the task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User who the task is assigned to.**Note:** This field is editable only if you are shipping the asset to the customer.

</td></tr><tr><td>

Tracking number

</td><td>

Tracking number that you can use to track the status and location of the asset shipment.

</td></tr><tr><td>

Ship to

</td><td>

Geographic location that you are shipping to asset to.

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
</table>5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Ship task closes with an updated state of Closed Complete.
-   A corresponding shipment record is automatically created for the asset shipment. A reference to the shipment record is populated in the **Shipment order** field of the Ship task. You can view and manage the shipment record from the Shipments list of the Asset operations view. For detailed instructions, see [View and add enterprise asset shipments](view-enterprise-asset-shipments.md).
-   A corresponding Receive asset task is automatically generated.

## What to do next

Complete the corresponding Receive asset task by confirming that the shipped asset was received. For detailed instructions, see [Complete the Receive asset task for a defective Device as a Service DaaS asset](receive-shipped-daas-asset-rma-response-order.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

