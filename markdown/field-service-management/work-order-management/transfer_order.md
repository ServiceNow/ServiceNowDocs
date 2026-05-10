---
title: Transfer part orders through the Field Service Contractor Portal
description: Use a transfer order to move required parts between company stockrooms or to a location where a requesting agent can receive the parts.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Requesting and receiving required parts, Contractor Portal, Completing work orders on the web interface, Use, Field Service Management]
---

# Transfer part orders through the Field Service Contractor Portal

Use a transfer order to move required parts between company stockrooms or to a location where a requesting agent can receive the parts.

## Before you begin

Role required: wm\_ext\_manager

## About this task

You can process only transfer orders that contain parts sourced from a warehouse that you manage.

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor Portal** &gt; **My Lists** &gt; **Transfer Orders**.

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

<table id="choicetable_mhs_zj4_rhb"><thead><tr><th align="left" id="d118535e137">

To

</th><th align="left" id="d118535e140">

Do this

</th></tr></thead><tbody><tr><td id="d118535e146">

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

</td></tr><tr><td id="d118535e228">

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
