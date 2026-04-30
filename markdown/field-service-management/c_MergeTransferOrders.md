---
title: Merge transfer orders
description: After you submit a new transfer order, the system examines all existing transfer orders attached to the current work order task to determine if the new transfer order can be merged with any of the existing orders.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage transfer orders, Managing inventory in Field Service Management, Using Field Service Management, Field Service Management]
---

# Merge transfer orders

After you submit a new transfer order, the system examines all existing transfer orders attached to the current work order task to determine if the new transfer order can be merged with any of the existing orders.

The system uses these criteria to merge transfer orders:

-   Created from the Field Service Management application. \(Configure the transfer order record to add the **Type** field.\)
-   In the **Draft** stage.
-   Same **From Stockroom**.
-   Same **Destination Stockroom**.

If an existing transfer order matches these criteria, the new transfer order line is placed under the existing transfer order. If no existing transfer order matches these criteria, a new transfer order is created and the transfer order line is added. It is good practice to view the transfer order and ensure that all information is correct. For example, check that the **Delivery by date** on the transfer order is appropriate for the **Required by date** on the part requirement. Transfer orders created in the Field Service Management application are not merged or combined with transfer orders created from any other application, such as Procurement.

When all the transfer order lines under a part requirement are delivered to the assigned agent's personal stockroom, the part requirement is marked **Delivered**. When both the consumable and non-consumable assets are delivered, the system changes their **State** to **In stock** and their **Substate** to **Reserved** \(in [Asset Management](https://www.servicenow.com/docs/access?context=c_AssetManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)\).

**Parent Topic:**[Manage transfer orders](c_TransferOrders.md)

