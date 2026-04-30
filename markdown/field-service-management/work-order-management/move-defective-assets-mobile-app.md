---
title: Move defective assets through the transfer process
description: Add defective parts from your stockroom to the drop-off list. Generate transfer orders to move these items to the stockroom where it needs to be dropped off.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inventory, ServiceNow Agent mobile app, Use, Field Service Management]
---

# Move defective assets through the transfer process

Add defective parts from your stockroom to the drop-off list. Generate transfer orders to move these items to the stockroom where it needs to be dropped off.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **Inventory** &gt; **My Inventory**.

    Parts that are in available or reserved substate are displayed in the **Available** tab and the ones that are defective are displayed in the **Defective** tab.

3.  Click **Defective**.

4.  Select the part for drop-off.

5.  Do one of the following to move the part to the stockroom where it needs to be returned.

<table id="choicetable_ijp_w1y_2jb"><thead><tr><th align="left" id="d116871e107">

To

</th><th align="left" id="d116871e110">

Do this

</th></tr></thead><tbody><tr><td id="d116871e116">

**Drop off**

</td><td>

1.  Click the part.
2.  Swipe the part to the left and click **Add to drop-off list**.


</td></tr><tr><td id="d116871e137">

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

-   If there is an existing transfer order for the drop-off location, then the new transfer order line is added that transfer order.

    **Note:** The transfer order must be in **Draft** state.

-   If a transfer order for the drop-off location does not exist, then a new transfer order is created and the transfer order line added to that transfer order.

For more information on asset transfers, see [Move an asset through the transfer process](../../planning-and-policy/task/create-transfer-order-line-task.md).

