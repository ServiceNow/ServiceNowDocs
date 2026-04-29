---
title: Return items received in a transfer order
description: When you receive a transfer order and if there’s a problem with all or some of the items, you can return the transfer order.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Return items received in a transfer order

When you receive a transfer order and if there’s a problem with all or some of the items, you can return the transfer order.

## Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

## About this task

Items in a transfer order must be received before they can be returned.

## Procedure

1.  Navigate to **All** &gt; **Inventory Management** &gt; **Transfer Orders**.

2.  Select a transfer order that is in the **Received** stage.

3.  Click the transfer order line **Number** of the item to return.

4.  Click **Return**.

5.  Enter a quantity to return.

6.  Enter a reason for the return.

7.  Select the **Defective** check box to return items that are broken.

    Defective items are returned to the stockroom from which they were delivered, but aren’t added to available stock. Instead, they’re tracked in the separate category named "Defective" so they can’t be requested or transferred again.

8.  Click **OK**.

9.  Click **Update**.

    A new transfer order line is automatically created.

    A new corresponding parent transfer order is also automatically created with the new transfer order line on it.

10. If you’re returning a consumable, navigate to the transfer order line record, and click the model name to open the model record.

    The model record shows which stockrooms contain the model. The one defective model is listed.

    **Note:** The defective model is still at the stockroom to which it was delivered. The defective model must be transferred back to the stockroom where it originated.

11. Move the new transfer order through the regular transfer order process.

    Items are automatically returned to the stockroom from which they were delivered. A transfer order line item that has been returned can’t be delivered later.

    If you return another defective model from the same, original order, the two defective returns are merged into one line item.


**Parent Topic:**[Manage transfer order](../concept/manage-transfer-orders.md)

**Related topics**  


[Transfer order flow](../concept/transfer-order-flows.md)

[Transfer assets using transfer orders](t_TransferAssetsUsingTransferOrders.md)

[Summary of transfer order line tasks](../reference/r_SummaryOfTransferOrderStages.md)

[Delete a transfer order](t_DeleteATransferOrder.md)

[Delete a transfer order line](t_DeleteATransferOrderLine.md)

[Create a customized template task](create-customized-template-task.md)

[Create a template subtask](create-template-subtask.md)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md)

[Perform bulk updates for transfer order lines](create-bulk-transfer.md)

