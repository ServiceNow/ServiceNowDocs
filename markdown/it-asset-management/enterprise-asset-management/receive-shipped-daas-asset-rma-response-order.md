---
title: Complete the Receive asset task for a defective Device as a Service DaaS asset
description: After a customer ships a defective DaaS asset to you for repair or replacement, or after you ship a repaired DaaS asset back to a customer, complete the Receive asset task by verifying that the asset was received successfully.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 4
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Receive asset task for a defective Device as a Service DaaS asset

After a customer ships a defective DaaS asset to you for repair or replacement, or after you ship a repaired DaaS asset back to a customer, complete the Receive asset task by verifying that the asset was received successfully.

## Before you begin

Before you can begin the Receive asset task, you must complete the preceding Ship task by having the customer ship the asset to you or by shipping the asset back to the customer. For detailed instructions, see [Complete the Ship task for a defective Device as a Service DaaS asset](ship-daas-asset-rma-response-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d126183e94">

Navigation option

</th><th align="left" id="d126183e97">

Procedure

</th></tr></thead><tbody><tr><td id="d126183e103">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to verify the asset receipt for.

**Note:** You must select an order line that you have already completed the Ship task for.

5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d126183e147">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to verify the asset receipt for.

**Note:** You must select an order line that you have already completed the Ship task for.

3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d126183e182">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Receive asset task that you want to complete.

4.  On the **Details** tab of the Receive asset task, fill in the fields.

<table id="table_xyl_nls_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Due date

</td><td>

Date and time at which you must complete the task.**Note:** This field is editable only if you are verifying that a customer received the asset.

</td></tr><tr><td>

Asset

</td><td>

Asset that was shipped.

</td></tr><tr><td>

Asset received

</td><td>

Option that indicates if the asset was received. Select either **Yes** or **No**.

</td></tr><tr><td>

Assignment group

</td><td>

Group that the task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User who the task is assigned to.**Note:** This field is editable only if you are verifying that a customer received the asset.

</td></tr><tr><td>

Tracking number

</td><td>

Tracking number that you can use to track the status and location of the asset shipment.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom that the asset was added to.

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

-   The Receive asset task closes with an updated state of Closed Complete.
-   If you successfully received a defective DaaS asset from a customer for an on-site replacement, the RMA response order line moves to the Completed stage. A corresponding inbound asset order is automatically created.
-   If you successfully received a defective DaaS asset from a customer for an off-site repair or replacement, a corresponding Evaluate RMA asset task is automatically generated.
-   If a customer successfully received a DaaS asset that you repaired, the RMA response order line moves to the Completed stage.

## What to do next

-   If you successfully received a defective DaaS asset from a customer for an on-site replacement, complete the corresponding inbound asset order to provide the customer with a new asset. For detailed instructions, see [Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md).
-   If you successfully received a defective DaaS asset from a customer for an off-site repair or replacement, complete the corresponding Evaluate RMA asset task by evaluating the asset and determining whether you want to repair or replace it. For detailed instructions, see [Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset](evaluate-daas-asset-rma-response-order.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

