---
title: Move an asset through the transfer process
description: Use transfer order line tasks to move assets through the shipment or drop-off transfer process.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a transfer order, Manage transfer orders, Manage inventory in FSM, Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Move an asset through the transfer process

Use transfer order line tasks to move assets through the shipment or drop-off transfer process.

## Before you begin

Role required: wm\_agent, wm\_qualifier, wm\_dispatcher, wm\_admin, or qualifier combination role

## About this task

Transfer order line tasks are created to move transfer order lines from one stage to the other. A transfer order line initially has one transfer order line task for completing the fulfillment. When you fulfill a asset requirement and close the task, the system automatically creates two transfer order line tasks: one to prepare for shipment and another one to drop off the asset.

Closing a transfer order line completes the task, moves the transfer order line task to the next stage, and creates the next task in the process until you close all tasks required for completing the transfer order line. For more information on the stages of transfer, see [Transfer order flow](https://www.servicenow.com/docs/access?context=transfer-order-flows&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Sourcing** &gt; **Sourcing Transfer Orders**.

2.  Select a transfer order to transfer the asset.

3.  From the **Transfer Order Line** related list, select a transfer order line.

4.  From the **Transfer Order Line Tasks** related list, select a transfer order line task that is ready for fulfillment.

    Eligible tasks have the short description text "Ready for fulfillment" and the state Open.

5.  Click **Close Task** to complete fulfillment and start the asset transfer process.

    The transfer order line task that was ready for fulfillment moves to the Closed Complete state.

    The system automatically creates two new transfer order line tasks:

    -   The short description text for the transfer order line task to prepare for shipment is "Prepare for shipment" and the state is Open.
    -   The short description text for the transfer order line task for drop off is "Receive" and the state is Open.
6.  Drop off or prepare for shipment.

<table id="choicetable_mhs_zj4_rhb"><thead><tr><th align="left" id="d110541e152">

To

</th><th align="left" id="d110541e155">

Do this

</th></tr></thead><tbody><tr><td id="d110541e161">

**Prepare for shipment**

</td><td>

When you are ready to ship the asset: 1.  Click and open the transfer order line task created to prepare for shipment.

This task has the short description text "Prepare for shipment' and the state Open.

2.  Click **Close Task**.

The system automatically does the following:

    -   Moves the transfer order line task created to prepare for shipment to the Closed Complete state.
    -   Opens a transfer order line task for shipping the asset. The short description text for this transfer order line task is "Ship" and the state is Open.
    -   Moves the transfer order line task created for drop off to the Closed Skipped state.
3.  Click and open the transfer order line task created for shipping the asset.

This task has the short description text "Ship" and the state Open.

4.  If the asset is a consumable, in the **Quantity received** field, enter the number of assets to be delivered.
5.  When the shipment is ready for shipping, click **Close Task**.

This task automatically moves to the Closed Complete state.

6.  Click and open the transfer order line task created for receiving the shipment.

This task has the short description text "Receive" and the state Open.

7.  When the shipment is ready for transit, click **Close Task**.

This task automatically moves to the Closed Complete state.

8.  Click and open the transfer order line task created for delivering the asset.

This task has the short description text "Deliver" and the state Open.

9.  After the shipment is delivered, click **Close Task**.

This task automatically moves to the Closed Complete state.

</td></tr><tr><td id="d110541e243">

**Drop off**

</td><td>

When you are ready to drop off the part or asset:1.  Click and open the transfer order line task created for drop off.

This task has the short description text "Receive" and the state Open.

2.  If the asset is a consumable, in the **Quantity received** field, enter the number of part or asset to be dropped off.
3.  When the parts or assets are ready for drop-off, click **Close Task**.

The system automatically moves the transfer order line created to prepare for shipment to the Closed Skipped state.

4.  Click and open the transfer order line for delivery.

This task has the short description text "Delivery" and the state Open.

5.  When the part or asset is delivered, click **Close Task**.

The task moves to the Closed Complete state.

</td></tr></tbody>
</table>
