---
title: Move defective assets through the transfer process
description: Add defective parts from your stockroom to the drop-off list. Generate transfer orders to move these items to the stockroom where it needs to be dropped off.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage your inventory using the Now Mobile Agent application, Use the Now Mobile Agent application to perform tasks, Using Field Service Management, Field Service Management]
---

# Move defective assets through the transfer process

Add defective parts from your stockroom to the drop-off list. Generate transfer orders to move these items to the stockroom where it needs to be dropped off.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## Procedure

1.  Open the Now Mobile Agent application.

2.  Tap **Inventory** &gt; **My Inventory**.

    Parts that are in available or reserved substate are displayed in the **Available** tab and the ones that are defective are displayed in the **Defective** tab.

3.  Click **Defective**.

4.  Select the part for drop-off.

5.  Do one of the following to move the part to the stockroom where it needs to be returned.

<table id="choicetable_ijp_w1y_2jb"><thead><tr><th align="left" id="d106636e101">

To

</th><th align="left" id="d106636e104">

Do this

</th></tr></thead><tbody><tr><td id="d106636e110">

**Drop off**

</td><td>

1.  Click the part.
2.  Swipe the part to the left and click **Add to drop-off list**.


</td></tr><tr><td id="d106636e131">

**View part details and then drop off**

</td><td>

1.  Click the part and open the form.
2.  Verify the model number and part quantity.
3.  Click the overflow icon and select **Add to drop-off list**.


</td></tr></tbody>
</table>6.  Click **To Stockroom**, select a stockroom for drop-off.

7.  Do one of the following:

    -   In iOS, click **Submit**.
    -   In Android, click the send icon.

## Result

A new transfer order line is created.

-   If there’s an existing transfer order for the drop-off location, then the new transfer order line is added that transfer order.

    **Note:** The transfer order must be in the **Draft** state.

-   If a transfer order for the drop-off location doesn’t exist, then a new transfer order is created and the transfer order line added to that transfer order.

For more information on asset transfers, see [Move an asset through the transfer process](../../planning-and-policy/task/create-transfer-order-line-task.md).

**Parent Topic:**[Manage your inventory using the Now Mobile Agent application](../concept/easily-track-parts.md)

