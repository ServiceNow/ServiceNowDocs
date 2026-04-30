---
title: Summary of transfer order line tasks
description: As assets move through the transfer process, the stage of a transfer order is always based on the individual transfer order lines tasks.
locale: en-US
release: yokohama
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Transfer orders for Asset Management, Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Summary of transfer order line tasks

As assets move through the transfer process, the stage of a transfer order is always based on the individual transfer order lines tasks.

<table id="table_zyp_pwb_fr"><thead><tr><th>

Transfer order line stages

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

When a transfer order line is created.On the asset form, the **State** field value remains **In stock**, and the **Substate** field value is updated to **Pending transfer**.

</td></tr><tr><td>

Requested

</td><td>

This task is created first for the transfer order line.On the asset form, the **State** field value remains **In stock**, and the **Substate** field value remains **Pending transfer**.

</td></tr><tr><td>

Shipment Preparation

</td><td>

After the **Requested** task is closed, this task is created. This task deals with preparing the transfer order line for shipment. Specify the values for the shipment tracking fields such as **Shipping carrier**, **Vendor**, **Tracking number**, and **Ship date**.On the asset form, the **State** field value remains **In stock**, and the **Substate** field value remains **Pending transfer**.

</td></tr><tr><td>

In Transit

</td><td>

After the **Shipment Preparation** task is closed, this task is created.On the asset form, the **State** field value changes to **In transit**, and the **Substate** field value is updated to **Reserved**.

</td></tr><tr><td>

Received

</td><td>

After the **In Transit** task is closed, this task is created.On the asset form, the **State** field value changes to **In stock**, and the **Substate** field value is updated to **Available**. The **Stockroom** field value is updated as the asset is received in the destination stockroom.

</td></tr><tr><td>

Delivered

</td><td>

After the **Received** task is closed, this task is created. After you close the **Delivered** task, the transfer order line is completed.On the asset form, the **State** field value remains **In stock** and the **Substate** field value is updated to **Reserved**.

</td></tr></tbody>
</table>**Parent Topic:**[Transfer orders for Asset Management](../concept/transfer-orders-for-am.md)

