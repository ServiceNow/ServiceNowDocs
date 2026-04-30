---
title: View and add enterprise asset shipments
description: Use the Shipments list to view all active enterprise asset shipments from a central location. If an existing shipment doesn’t appear on the list, you can add it manually.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing enterprise asset shipments, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# View and add enterprise asset shipments

Use the Shipments list to view all active enterprise asset shipments from a central location. If an existing shipment doesn’t appear on the list, you can add it manually.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_technician, sn\_eam.enterprise\_asset\_manager, or sn\_eam.enterprise\_admin

**Note:** Only the sn\_eam.enterprise\_admin role can add shipments manually.

## About this task

You can view and add shipments for your transfer orders, purchase orders, move orders, Return Merchandise Authorization \(RMA\) orders, disposal orders, resale orders, recall orders, reclamation requests, Advanced Shipment Notifications \(ASNs\), and lease contracts.

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  From the left navigation menu of the Asset operations view, navigate to **Shipment** &gt; **Shipments**.

3.  View the complete list of active enterprise asset shipments.

    Select a shipment to view additional shipment details, including the shipment source and associated enterprise assets.

4.  If an existing enterprise asset shipment doesn’t appear on the list, add it manually.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_o5b_nx4_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shipping carrier

</td><td>

Shipping carrier through which the enterprise assets were shipped.

</td></tr><tr><td>

Ship date

</td><td>

Date and time at which the enterprise assets were shipped.

</td></tr><tr><td>

Shipped from

</td><td>

Geographic location that the enterprise assets were shipped from.

</td></tr><tr><td>

Receive date

</td><td>

Date and time at which the shipment was received.

</td></tr><tr><td>

Tracking number

</td><td>

Tracking number that enables you to track the status and location of the shipment.

</td></tr><tr><td>

Shipped by

</td><td>

User who shipped the enterprise assets.

</td></tr><tr><td>

Shipped to

</td><td>

Geographic location that the enterprise assets were shipped to.

</td></tr><tr><td>

Shipment quantity

</td><td>

Quantity of assets shipped for the shipment record.This field value is automatically populated when the assets are shipped to the destination.

The shipment quantity is the sum of the asset quantities shipped for each shipment line.

**Important:** The **Shipment quantity** field is available with Enterprise Asset Management version 9.1.0 onwards.

</td></tr><tr><td>

Received by

</td><td>

User who received the shipment.

</td></tr><tr><td>

Ignore stale check

</td><td>

Option to ignore stale checks for the shipment.

</td></tr></tbody>
</table>    3.  Select **Save**.


**Parent Topic:**[Managing enterprise asset shipments](../concept/manage-shipments-eam.md)

