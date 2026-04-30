---
title: Consumable and non-consumable models
description: The transfer process is slightly different for consumables than it is for non-consumables.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transfer orders, Inventory, Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Consumable and non-consumable models

The transfer process is slightly different for consumables than it is for non-consumables.

Consumable assets, such as computer keyboards, are not tracked individually in transfer orders. Non-consumable assets, such as network routers, are configuration items that are tracked individually in transfer orders.

-   **Consumable models**

    If the model being transferred is a consumable, the system can order all the items at once if you specify a **Requested quantity** on a single transfer order line. After the quantity is specified, the system determines whether the selected stockroom has enough quantity to fulfill the part requirement. If the stockroom cannot fill the entire part requirement, the system enters the quantity available in the stockroom automatically. For example, if the requirement is for 25 keyboards and the selected stockroom only contains 10, the available quantity of 10 is added. The user must create another transfer order line manually to order the remaining 15 keyboards from another stockroom.

-   **Non-consumable models**

    If the model being transferred is a non-consumable asset, create one transfer order line per asset. The system creates as many transfer order lines as the required quantity. This approach is used so that each configuration item can change its status and stockroom location independently. For example, if the part requirement specifies two Canon i960 Photo printers, and printers are managed as configuration items, then the system generates two transfer orders lines - one per configuration item. After the agent receives the part \(item state changes to **In Stock** and substate changes to **Reserved**\) and uses it, the asset is listed as **In Use** by the caller who originated the work order.


