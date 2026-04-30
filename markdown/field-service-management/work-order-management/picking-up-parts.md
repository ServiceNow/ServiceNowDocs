---
title: Picking up parts
description: You can view a summarized list of transfer orders for all the assets that are waiting to be picked up physically.Pick up parts that you requested from peer agents that are ready for pickup and then close the transfer order line.When you are at a task site and need a missing part to complete your job, you can pick up the part by transferring it from an available stockroom.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inventory, ServiceNow Agent mobile app, Use, Field Service Management]
---

# Picking up parts

You can view a summarized list of transfer orders for all the assets that are waiting to be picked up physically.

## Pick up parts for your part requests

Pick up parts that you requested from peer agents that are ready for pickup and then close the transfer order line.

### Before you begin

The Field Service Advanced Parts Sourcing plugin \(com.snc.fsm\_advanced\_parts\_sourcing\) must be activated. For more information, see [Additional plugins for Field Service Management](../reference/field-service-additional-plugins.md).

Role required: wm\_agent

### Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **Inventory**.

3.  Tap **My requests**.

4.  Tap the part request for which you wanted to view the transfer orders.

5.  Tap the **Transfer orders** tab of the selected part request.

6.  Select the transfer orders for which you want to pick up parts.

7.  Tap **Confirm pickup**.


### Result

A message appears to indicate that the pickup and transfer order is completed. The transfer order line state changes to Delivered.

## Pick up a part to complete tasks

When you are at a task site and need a missing part to complete your job, you can pick up the part by transferring it from an available stockroom.

### Before you begin

Role required: wm\_agent or wm\_dispatcher

### Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **Parts to receive**.

3.  Tap a part for pick up, swipe to the left and select **Confirm pickup**.

    The sourcing stages for the part appears. If the part is in **Received** or **In Transit** stage, you can confirm pick up.

4.  Select **Confirm pickup**.


### Result

The sourcing stage moves to **Delivered** and the part is added to your inventory and is marked as available.

