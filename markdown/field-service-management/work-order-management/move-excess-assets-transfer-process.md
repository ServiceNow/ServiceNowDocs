---
title: Move excess assets through the transfer process from a mobile device
description: Move your excess consumable parts from your stockroom to the drop-off list by using the ServiceNow Agent application on your mobile device. You can generate transfer orders to move these items to the stockroom where it must be dropped off.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inventory, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Move excess assets through the transfer process from a mobile device

Move your excess consumable parts from your stockroom to the drop-off list by using the ServiceNow Agent application on your mobile device. You can generate transfer orders to move these items to the stockroom where it must be dropped off.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **Inventory** &gt; **My Inventory**.

    The parts that are in an available or a reserved substate are displayed in the **Available** tab.

3.  Select **Available**.

4.  Select the part that you want to drop off.

5.  Move the part to be returned to the stockroom by doing one of the following actions.

<table id="choicetable_ijp_w1y_2jb"><thead><tr><th align="left" id="d108142e109">

Option

</th><th align="left" id="d108142e112">

Description

</th></tr></thead><tbody><tr><td id="d108142e118">

**Drop off**

</td><td>

1.  Select the part.
2.  Swipe the part to the left and select **Add to drop-off list**.
3.  Select the quantity that you want to return.


</td></tr><tr><td id="d108142e142">

**View part details and then drop off**

</td><td>

1.  Select the part and open the form.
2.  Verify the model number and part quantity.
3.  Select the overflow icon and select **Add to drop-off list**.


</td></tr></tbody>
</table>6.  Select the part and open the form.

7.  Select the Overflow ![Overflow icon.](../image/OverflowIcon.png) icon and then select **Add to drop-off list**.

8.  Verify the model number.

9.  Select **Quantity** and enter the quantity that you want to return to the stockroom.

10. Select **Drop off stock room** and then select a stockroom where you want to drop off your parts.

11. Do one of the following actions depending on whether you have an Apple iOS or Google Android device:

    -   In an Apple iOS device, select **Submit**.
    -   In a Google Android device, select the send icon.

## Result

A new transfer order line is created.

-   If there’s an existing transfer order for the drop-off location, then the new transfer order line is added that transfer order.

    **Note:** The transfer order must be in the **Draft** state.

-   If a transfer order for the drop-off location doesn’t exist, a new transfer order is created and the transfer order line is added to that transfer order.

For more information on asset transfers, see [Move an asset through the transfer process](../../planning-and-policy/task/create-transfer-order-line-task.md).

## What to do next

Check the status of the part in the Parts to drop-off list.

