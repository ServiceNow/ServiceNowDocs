---
title: Receive an asset
description: When assets are received and delivered to a stockroom, they’re added to the system.
locale: en-US
release: yokohama
product: Procurement
classification: procurement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Receive assets, Procurement, Asset Management, IT Service Management]
---

# Receive an asset

When assets are received and delivered to a stockroom, they’re added to the system.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

When you receive assets:

-   If you haven’t pre-created hardware assets, you can enter asset details and reserve them for users.
-   You can over receive an order wherein, the received quantity can be higher than the ordered quantity.
-   If you have ordered multiple items with different receiving stockrooms, you can receive them at the same time.

## Procedure

1.  View purchase orders.

<table id="choicetable_jg3_j33_4xb"><thead><tr><th align="left" id="d327657e71">

UI

</th><th align="left" id="d327657e74">

Action

</th></tr></thead><tbody><tr><td id="d327657e80">

**Core UI**

</td><td>

Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Purchase Orders**.

</td></tr><tr><td id="d327657e104">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Procurement**.
2.  Select the **Purchase orders** tab.


</td></tr><tr><td id="d327657e137">

**Enterprise Asset WorkWorkspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Procurement**.
2.  Select the **Purchase orders** tab.


</td></tr><tr><td id="d327657e170">

**OT Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **OT Asset Workspace** &gt; **Procurement**.
2.  Select the **Purchase orders** tab.


</td></tr></tbody>
</table>2.  Select a purchase order with a **Status** of **Ordered** or **Pending Delivery**.

3.  Select **Receive**.

    The Receive Purchase Order screen appears with the list of the products ordered.

4.  Select the **Received** check box for the line items that you’re receiving.

5.  To receive software assets:

    1.  Edit the **Receiving Stockroom** if the items arrived at a different stockroom than the one specified on the purchase order.

    2.  Edit the **Receiving Quantity** if the number of items delivered doesn't match the number ordered.

    3.  Edit the **Unit Cost** if the price changed between the time the item was ordered and the time it arrived at the stockroom.

        Enter a number. The number can include decimals.

    4.  Select **Capture Asset tags** to enter asset details.

        You can't enter details for assets more than the received rights.

    5.  In the **Capture Asset Tag** dialog box, select **Insert a new row**.

    6.  Enter the asset tag, serial number, rights, and License key.

6.  To receive hardware and consumables assets:

    1.  Edit the **Receiving Stockroom** if the items arrived at a different stockroom than the one specified on the purchase order.

        **Note:** The asset bundle when received creates the asset bundle with the status as **Bundle**. You must add the individual assets under the asset bundle.

    2.  Edit the **Receiving Quantity** if the number of items delivered doesn’t match the number ordered.

    3.  Select the **Reserve** toggle button to reserve the item.

        When a reserved item is received, the **State** and **Substate** fields on the corresponding asset record are automatically set to **In stock** and **Reserved**, respectively. If the **Reserve** button isn’t selected for an item, the **State** and **Substate** fields on the corresponding asset record are set to **In stock** and **Available**.

        **Note:** You can’t reserve consumables.

    4.  From the **Reserved for** list, select a user you want reserve the asset for.

        If a name was specified in the **Requested for** field on the Purchase order line item form, the name is added automatically but can be changed.

        You can add multiple users in the **Capture Asset tags** dialog box.

    5.  Select **Capture Asset tags** to enter asset details.

        You can’t enter details for assets more than the received quantity. You can also reserve assets for a user.

        **Note:** If you’ve pre-created the assets, you must select the ones you want to receive.

    6.  On the **Capture Asset Tag** dialog box, select **Insert a new row**.

    7.  Enter the asset tag and serial number.

        If you have activated the Enterprise Asset Management or OT Asset Management application, then the **MAC address** fields is also displayed.

    8.  From the **Reserved for** list, select the user for whom the item was ordered.

        If a name was specified in the **Requested for** field on the Purchase order line item form, the name is added automatically, but you can change it.

    9.  Edit the **Unit Cost** if the price changed between the time the item was ordered and the time it arrived at the stockroom.

        Enter a number. The number can include decimals.

7.  Select **Submit**.

    A confirmation message displays with the details of assets received.

8.  Select **OK**.

    A receiving slip is automatically created and can be viewed in the **Receiving Slips** related list. If items on a purchase order are received at different times, a new receiving slip is created each time any item on the purchase order is received. For example, if 30 laptop computers were ordered and arrived in three separate shipments, three receiving slips are created.

    Different assets are created for each hardware item. If it’s a software asset, one single asset is created for each license if you don't split the rights. For consumables, if an asset exists, it’s updated, or else, new assets are created.


**Parent Topic:**[Receive assets](../concept/c_ReceiveAssets.md)

**Related topics**  


[Create a receiving slip](t_CreateAReceivingSlip.md)

[Create a receiving slip line](t_CreateAReceivingSlipLine.md)

[Consumable assets](../concept/c_ReceiveAConsumableAsset.md)

