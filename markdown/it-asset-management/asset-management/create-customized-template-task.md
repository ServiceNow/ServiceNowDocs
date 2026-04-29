---
title: Create a customized template task
description: Create customized template tasks to configure your specific task workflow for transfer order lines. Default template tasks are available with the Asset Management application. You can’t modify or delete a default template task.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Create a customized template task

Create customized template tasks to configure your specific task workflow for transfer order lines. Default template tasks are available with the Asset Management application. You can’t modify or delete a default template task.

## Before you begin

Role required: asset\_system\_admin or inventory\_user

## About this task

Template tasks help you progress through the various stages of the transfer order line. Custom template tasks are stored in the Custom Template Task \[alm\_custom\_template\_task\] table. The template tasks are based on model categories. For example, when you create a customized template task for the Application model category, whenever a transfer order line is created for the Application model category, the template tasks associated with the Application model category are used as transfer order line tasks. When you create customized template tasks, make a copy of the Transfer Order Line workflow and update the workflow accordingly. For example, if you need only four tasks out of five, you can delete the additional task from the workflow.

**Note:** Two template tasks can’t be created when they’re based on the same model category, the same order number and the same stage. The model category, the order, and the stage have to be unique for each template task. For example, you can’t create two template tasks for Prepare for Shipment, based on the Application model category, order number 200, and the stage as Requested. If you try to create an identical template task as mentioned in the example, an error message is displayed.

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Order Lines** &gt; **Template Tasks**.

    All the default template tasks that are available with the Asset Management application are listed.

2.  Click **New**.

    You can also customize a template task by copying a default template task. Click **Copy Default Template** and select a model category.

3.  Fill out the form fields \(as shown in the table\).

    |Field|Description|
    |-----|-----------|
    |Task name|Name of the template task|
    |Model category|Model category this template task is based on.|
    |Order|Order in which the template task is added to the transfer order line.|
    |Short description|Brief description about this template task.|
    |Next stage|Stage that this template task gets executed.|

4.  Click **Submit**.


**Parent Topic:**[Manage transfer order](../concept/manage-transfer-orders.md)

**Related topics**  


[Transfer order flow](../concept/transfer-order-flows.md)

[Transfer assets using transfer orders](t_TransferAssetsUsingTransferOrders.md)

[Summary of transfer order line tasks](../reference/r_SummaryOfTransferOrderStages.md)

[Delete a transfer order](t_DeleteATransferOrder.md)

[Delete a transfer order line](t_DeleteATransferOrderLine.md)

[Return items received in a transfer order](t_ReturnItemsRecInXferOrder.md)

[Create a template subtask](create-template-subtask.md)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md)

[Perform bulk updates for transfer order lines](create-bulk-transfer.md)

