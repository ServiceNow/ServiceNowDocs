---
title: Transfer orders for Asset Management
description: Transfer orders move assets between company stockrooms.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Manage transfer order, Use, Asset Management, IT Asset Management]
---

# Transfer orders for Asset Management

Transfer orders move assets between company stockrooms.

The Asset Management application enables asset managers to create transfer orders for moving assets between company stockrooms.

Consumable assets and non-consumable assets can be transferred as follows:

-   If an asset is consumable, it can be transferred and the quantity can be greater than one. Consumable parts are tracked by the system qualitatively.
-   If an asset is non-consumable, it must be transferred as a single entity with a quantity of one. Non-consumable parts correspond to assets defined in the system.

**Important:** In the Asset Management application, the Transfer Order Line workflow manages the processing of transfer order lines. If your ServiceNow instance has the following plugins activated, the transfer order lines are processed using a workflow, depending on the plugin installed.

-   If the Service Management Core plugin is activated, the Transfer Order Line SM core workflow manages the processing of the transfer order lines.
-   If the Field Service Management plugin \(com.snc.work\_management\) is activated, the Transfer Order Line SMCore workflow manages the processing of the transfer order lines.

For more information, see [Move an asset through the transfer process](https://www.servicenow.com/docs/access?context=create-transfer-order-line-task&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

## Transfer order lines

Transfer Order Lines is a new module under Inventory with Template Tasks and Template Subtasks as the sub modules. Transfer order lines allow the transfer of multiple assets on one transfer order. Actions such as shipment preparation can take place at the transfer order line level. Pre-allocated assets can be included in a transfer order line, but can only be transferred in their full quantity. A business rule prevents the same asset from being transferred on two different transfer orders at the same time.

**Note:** The Transfer Order and the Transfer Order Line workflows have moved from the Procurement plugin to the Asset Management plugin. The Transfer Order Line workflow runs only if no other workflows are matched or running on a specific record.

## Transfer order line tasks

When you create a transfer order line, based on the model category specified in the asset, a transfer order line task is automatically created. Transfer order line tasks are created to move transfer order lines from one stage to the other. Transfer order line tasks also help you to track service levels and the time frame needed to complete a transfer order.

Default template tasks are available with the Asset Management application. The template tasks are based on model categories. Default template tasks cannot be deleted or modified. If required, you can also create your own customized template tasks. For more information, see [Create a customized template task](../task/create-customized-template-task.md). When you create a transfer order line and select an asset, that asset corresponds to a model category. If a customized template task exists for that model category then that template task is added to the transfer order line as a transfer order line task. If no customized template task match is found for the asset you selected, then the default template task is added as a transfer order line task.

Closing a transfer order line task completes the task and creates the next task in the process. For example, once you close the Ready for fulfillment task, the state for this task appears as **Closed Complete** and a new task is opened for the next stage, Ready for Shipment. This process continues till you close all the tasks required for completing the transfer order line. As you close a task and as a task moves from one stage to the next, the asset gets automatically updated too. For example, when the transfer order line moves from Ready to Fulfillment to Prepare for Shipment, the asset's status also moves from available to reserved.

**Note:**

If you skip a transfer order line task and select **Closed Skipped**, the asset is not updated automatically. Once the asset is received or delivered, you can make the update manually.

If you are upgrading from any previous release to the New York release, and you have an open transfer order line that is still being processed, all the transfer order line tasks associated with that transfer order line are simultaneously created and displayed in the transfer order line form layout. Based on the stage of the transfer order line, the tasks that still need to be processed will be open; all the other tasks that have already been completed will be closed. Based on the order, if you close a later transfer order line task, all the previous tasks, which are currently open, automatically will be **Closed Skipped**.

## Transfer order line subtasks

To further add granularity and efficiency to the process, you can also create subtasks for each transfer order line task. Each transfer order line task can have multiple subtasks. For example, before preparing for shipment, for a computer, you may want to create subtasks for imaging the computer or adding additional software. If subtasks have been defined for a particular transfer order line task, then the subtasks are automatically added to the transfer order line task. Once all the subtasks are closed, the transfer order line task is automatically closed. For more information, see [Create a template subtask](../task/create-template-subtask.md).

-   **[Transfer assets using transfer orders](../task/t_TransferAssetsUsingTransferOrders.md)**  
Transfer assets from one location to the other by moving the assets through the transfer order process. Transfer order lines specify the exact items that comprise a transfer order.
-   **[Summary of transfer order line tasks](../reference/r_SummaryOfTransferOrderStages.md)**  
As assets move through the transfer process, the stage of a transfer order is updated based on the individual transfer order lines tasks.
-   **[Delete a transfer order](../task/t_DeleteATransferOrder.md)**  
You can delete a transfer order only if the transfer order is still in the draft stage.
-   **[Delete a transfer order line](../task/t_DeleteATransferOrderLine.md)**  
You can delete a transfer order line only if it's still in the draft stage.
-   **[Return items received in a transfer order](../task/t_ReturnItemsRecInXferOrder.md)**  
When you receive a transfer order and if there’s a problem with all or some of the items, you can return the transfer order.

**Parent Topic:**[Manage transfer order](../../hardware-asset-management/concept/manage-transfer-orders.md)

**Related topics**  


[Transfer order flow](transfer-order-flows.md)

[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md)

[Perform bulk updates for transfer order lines](../task/create-bulk-transfer.md)

[Transfer order flow](transfer-order-flows.md)

