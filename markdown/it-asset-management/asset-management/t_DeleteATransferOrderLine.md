---
title: Delete a transfer order line
description: You can delete a transfer order line only if it's still in the draft stage.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transfer order tasks, Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Delete a transfer order line

You can delete a transfer order line only if it's still in the draft stage.

## Before you begin

Role required: asset\_system\_admin or inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must install the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

## Procedure

1.  Open a transfer order.

2.  Select the check box beside a transfer order line.

3.  From the Actions on the selected rows menu at the bottom of the list, select **Delete**.

    Alternatively, you can cancel a transfer order or a transfer order line while it is in **Requested** or **Shipment Preparation** stage. Once all the lines are canceled, the transfer order is automatically canceled.


**Parent Topic:**[Transfer order tasks](../concept/work-with-transfer-orders.md)

**Related topics**  


[Delete a transfer order](t_DeleteATransferOrder.md)

[Return items received in a transfer order](t_ReturnItemsRecInXferOrder.md)

