---
title: Create a receiving slip line
description: When assets arrive at a stockroom and you receive them, a receiving slip is created on the purchase order. You create a receiving slip line to identify the specific assets and quantities that were received.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Receive assets, Procurement, IT Asset Management]
---

# Create a receiving slip line

When assets arrive at a stockroom and you receive them, a receiving slip is created on the purchase order. You create a receiving slip line to identify the specific assets and quantities that were received.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

If the asset already exists, the asset record is updated when you save the receiving slip line. If the asset does not already exist, a new hardware or software asset record is created. The **Model category** and **Configuration item** fields are automatically filled in on the new asset record based on information in the request, purchase order, or receiving slip. If **Asset Tag** and **Serial Number** information exists, it is not overwritten.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Receiving** &gt; **Receiving Slips** and open a receiving slip.

2.  In the **Receiving Slip Lines** related list, select **New**.

    The following fields are completed automatically.

    -   A **Number** is assigned.
    -   In **Received**, the current date and time are added.
    -   In **Received by**, the currently logged in user is added.
3.  In **Purchase Order Line**, select the reference lookup icon and select a purchase order line.

    The **Purchase Order Line** field is required if the parent receiving slip has an associated purchase order. Only purchase order lines that are associated with the same purchase order linked to the parent receiving slip are available for selection.

4.  In **Quantity**, enter the number of items received.

    For example, five items were ordered, but only two are being received.

5.  Edit the **Received by**, **Requested for**, and **Unit cost** fields, as needed.

6.  Select **Submit**.


## Result

The **Receiving stockroom** field on the Receiving Slip record becomes read-only.

**Parent Topic:**[Receive assets](../concept/c_ReceiveAssets.md)

**Related topics**  


[Receive an asset](t_ReceiveAnAsset.md)

[Create a receiving slip](t_CreateAReceivingSlip.md)

