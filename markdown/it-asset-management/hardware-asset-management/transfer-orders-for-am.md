---
title: Transfer orders for Asset Management
description: Transfer orders move assets between company stockrooms.Transfer assets from one location to the other by moving the assets through the transfer order process. You create a transfer order and move it from its initial Draft status to the final Received status.As assets move through the transfer process, the stage of a transfer order is always based on the individual transfer order lines tasks.You can delete a transfer order only if the transfer order is still in the draft stage.You can delete a transfer order line only if it's still in the draft stage.When you receive a transfer order and if there’s a problem with all or some of the items, you can return the transfer order.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 17
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Transfer orders for Asset Management

Transfer orders move assets between company stockrooms.

The Asset Management application enables asset managers to create transfer orders for moving assets between company stockrooms.

Consumable assets and non-consumable assets can be transferred as follows:

-   If an asset is consumable, it can be transferred and the quantity can be greater than one. Consumable parts are tracked by the system qualitatively.
-   If an asset is non-consumable, it must be transferred as a single entity with a quantity of one. Non-consumable parts correspond to assets defined in the system.

**Important:** The Transfer Order Line workflow in the Asset Management application handles the processing of transfer order lines. However, if the Service Management Core plugin is also activated on your ServiceNow instance, the Transfer Order Line SM core workflow will process the transfer order lines instead. For more information, see [Move an asset through the transfer process](https://www.servicenow.com/docs/access?context=create-transfer-order-line-task&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

## Transfer order lines

Transfer Order Lines is a new module under Inventory with Template Tasks and Template Subtasks as the sub modules. Transfer order lines allow the transfer of multiple assets on one transfer order. Actions such as shipment preparation can take place at the transfer order line level. Pre-allocated assets can be included in a transfer order line, but can only be transferred in their full quantity. A business rule prevents the same asset from being transferred on two different transfer orders at the same time.

**Note:** The Transfer Order and the Transfer Order Line workflows have moved from the Procurement plugin to the Asset Management plugin. The Transfer Order Line workflow runs only if no other workflows are matched or running on a specific record.

## Transfer order line tasks

When you create a transfer order line, based on the model category specified in the asset, a transfer order line task is automatically created. Transfer order line tasks are created to move transfer order lines from one stage to the other. Transfer order line tasks also help you to track service levels and the time frame needed to complete a transfer order.

Default template tasks are available with the Asset Management application. The template tasks are based on model categories. Default template tasks cannot be deleted or modified. If required, you can also create your own customized template tasks. For more information, see [Create a customized template task](../task/t_CreateATransferOrder.md#). When you create a transfer order line and select an asset, that asset corresponds to a model category. If a customized template task exists for that model category then that template task is added to the transfer order line as a transfer order line task. If no customized template task match is found for the asset you selected, then the default template task is added as a transfer order line task.

Closing a transfer order line task completes the task and creates the next task in the process. For example, once you close the Ready for fulfillment task, the state for this task appears as **Closed Complete** and a new task is opened for the next stage, Ready for Shipment. This process continues till you close all the tasks required for completing the transfer order line. As you close a task and as a task moves from one stage to the next, the asset gets automatically updated too. For example, when the transfer order line moves from Ready to Fulfillment to Prepare for Shipment, the asset's status also moves from available to reserved.

**Note:**

If you skip a transfer order line task and select **Closed Skipped**, the asset is not updated automatically. Once the asset is received or delivered, you can make the update manually.

If you are upgrading from any previous release to the New York release, and you have an open transfer order line that is still being processed, all the transfer order line tasks associated with that transfer order line are simultaneously created and displayed in the transfer order line form layout. Based on the stage of the transfer order line, the tasks that still need to be processed will be open; all the other tasks that have already been completed will be closed. Based on the order, if you close a later transfer order line task, all the previous tasks, which are currently open, automatically will be **Closed Skipped**.

## Transfer order line subtasks

To further add granularity and efficiency to the process, you can also create subtasks for each transfer order line task. Each transfer order line task can have multiple subtasks. For example, before preparing for shipment, for a computer, you may want to create subtasks for imaging the computer or adding additional software. If subtasks have been defined for a particular transfer order line task, then the subtasks are automatically added to the transfer order line task. Once all the subtasks are closed, the transfer order line task is automatically closed. For more information, see [Create a template subtask](../task/t_CreateATransferOrder.md#).

**Parent Topic:**[Using Hardware Asset Management](../../hardware-asset-management/concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../../hardware-asset-management/concept/Work-with-hardware-normalization.md)

[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

[Consumables life cycle](c_FollowLifeCycleConsumbl.md)

[Manage asset bundles from your inventory](../../hardware-asset-management/task/create-bundled-assets.md)

[Manage various assets through asset classes](c_AssetClasses.md)

[Manage your inventory through pallet assets](../../hardware-asset-management/concept/pallets-for-inventory-management.md)

[Create fixed assets](c_CreatingFixedAssets.md#)

[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

[Manage loaner assets](../../hardware-asset-management/task/manage-loaner-asset.md)

[Donate assets to charity organizations](../../hardware-asset-management/concept/donate-asset-to-charity-organizations.md)

[Exclude assets](../../hardware-asset-management/task/exclude-assets.md)

[Use Advanced Shipment Notification](../../hardware-asset-management/task/advanced-shipment-notification.md)

[Use Organization Management](../reference/org-mgmt.md#)

[Manage RMA requests](../../hardware-asset-management/concept/manage-rma-req.md)

[Create an inventory stock order request](../../hardware-asset-management/task/create-inventory-stock-order.md)

[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md#)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md#)

[Create a disposal order](../../hardware-asset-management/task/create-disposal-order.md)

[Use a hardware asset request flow](../../hardware-asset-management/task/hardware-request-flow.md)

[Audit your inventory](../../hardware-asset-management/task/audit-your-inventory.md)

[Request a Hardware Asset Refresh](../../hardware-asset-management/task/hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](../../hardware-asset-management/task/manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../../hardware-asset-management/concept/manage-asset-reclaim.md)

[View RFID information of assets](../../hardware-asset-management/task/view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../../hardware-asset-management/concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../../hardware-asset-management/concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../../hardware-asset-management/concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../../hardware-asset-management/concept/tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](../../hardware-asset-management/task/track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](../../hardware-asset-management/concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../../hardware-asset-management/concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../../hardware-asset-management/concept/configure-ham-tco.md)

[Manage and monitor hardware asset performance](../../hardware-asset-management/concept/manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](../../hardware-asset-management/concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../../hardware-asset-management/concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../../hardware-asset-management/concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](../../hardware-asset-management/concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](../../hardware-asset-management/concept/manage-hardware-asset-tasks-mobile-agent.md)

[Acknowledge receipt of assets on the Employee Center portal](../../hardware-asset-management/task/receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](../../hardware-asset-management/task/trigger-flow-ham.md)

## Transfer assets using transfer orders

Transfer assets from one location to the other by moving the assets through the transfer order process. You create a transfer order and move it from its initial **Draft** status to the final **Received** status.

### Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Orders** &gt; **Create Transfer Order**.

2.  In the **From Stockroom** list, select a stockroom from which you want to ship the items.

3.  In the **To Stockroom** list, select a stockroom where you want to ship the items.

    **Note:** If you select the same stockroom in both the From Stockroom and To Stockroom fields, the transfer order automatically moves from **Draft** to **Received** when a transfer order line is added.

4.  Select a date and time for the delivery from the **Delivery by date** date picker.

5.  Select **Submit**.

6.  Open the transfer order.

7.  Next to **Transfer Order Lines**, click **New**.

8.  Select a model for the transfer order line.

9.  If the model is a consumable, specify a quantity in **Quantity Requested**.

10. Click **Submit**.

    After creating transfer order lines, the transfer order and all the transfer order lines are in the draft stage. While a transfer order or a transfer order line is in the draft stage, it can be deleted.

    **Note:** When an asset is part of a transfer order set to **Draft**, the asset record updates to show the asset as reserved. You can't request or transfer the asset while it’s reserved.

    When you create a transfer order line, based on the model category specified in the asset, a transfer order line task is automatically created. The transfer order line task helps you to progress through the various stages of the transfer order line. Each transfer order line task represents a particular stage in the transfer process. As you close a task, a new task is created and the transfer process moves to the next stage.

11. Open the transfer order line task and click **Close Task**.

    The transfer order line task is completed and a new transfer order line task is opened.


### What to do next

Keep closing each task until you reach the last stage \(Received\). After you close the task for the Received stage, the transfer order line is completed and closed. All transfer order lines and the transfer order are marked **Delivered**.

## Summary of transfer order line tasks

As assets move through the transfer process, the stage of a transfer order is always based on the individual transfer order lines tasks.

<table id="table_zyp_pwb_fr"><thead><tr><th>

Transfer order line stages

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

When a transfer order line is created for the asset.On the asset form, the **State** field value remains **In stock**, and the **Substate** field value is updated to **Pending transfer**.

</td></tr><tr><td>

Requested

</td><td>

This task is created first for the transfer order line.On the asset form, the **State** field value remains **In stock**, and the **Substate** field value remains **Pending transfer**.

</td></tr><tr><td>

Shipment Preparation

</td><td>

After the **Requested** task is closed, this task is created. This task deals with preparing the transfer order line for shipment. Specify the values for the shipment tracking fields such as **Shipping carrier**, **Vendor**, **Tracking number**, and **Ship date**. On the asset form, the **State** field value remains **In stock**, and the **Substate** field value remains **Pending transfer**.

</td></tr><tr><td>

In Transit

</td><td>

After the **Shipment Preparation** task is closed, this task is created.On the asset form, the **State** field value changes to **In transit**, and the **Substate** field value is updated to **Reserved**.

</td></tr><tr><td>

Received

</td><td>

After the **In Transit** task is closed, this task is created. On the asset form, the **State** field value changes to **In stock**, and the **Substate** field value is updated to **Available**. The **Stockroom** field value is updated as the asset is received in the destination stockroom.

</td></tr><tr><td>

Delivered

</td><td>

After the **Received** task is closed, this task is created. After you close the **Delivered** task, the transfer order line is completed. On the asset form, the **State** field value remains **In stock** and the **Substate** field value is updated to **Reserved**.

</td></tr></tbody>
</table>## Delete a transfer order

You can delete a transfer order only if the transfer order is still in the draft stage.

### Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must install the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

### Procedure

1.  Navigate to **All** &gt; **Inventory Management** &gt; **Transfer Orders** &gt; **Transfer Orders**

2.  Select the check box beside a transfer order.

3.  From the Actions on the selected rows menu at the bottom of the list, select **Delete**.


**Related topics**  


[Delete a transfer order line](transfer-orders-for-am.md#)

[Return items received in a transfer order](transfer-orders-for-am.md#)

## Delete a transfer order line

You can delete a transfer order line only if it's still in the draft stage.

### Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must install the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

### Procedure

1.  Open a transfer order.

2.  Select the check box beside a transfer order line.

3.  From the Actions on the selected rows menu at the bottom of the list, select **Delete**.

    Alternatively, you can cancel a transfer order or a transfer order line while it is in **Requested** or **Shipment Preparation** stage. Once all the lines are canceled, the transfer order is automatically canceled.


**Related topics**  


[Delete a transfer order](transfer-orders-for-am.md#)

[Return items received in a transfer order](transfer-orders-for-am.md#)

## Return items received in a transfer order

When you receive a transfer order and if there’s a problem with all or some of the items, you can return the transfer order.

### Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

### About this task

Items in a transfer order must be received before they can be returned.

### Procedure

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


