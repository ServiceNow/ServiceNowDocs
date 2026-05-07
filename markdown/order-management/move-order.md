---
title: Move order
description: The move order helps agents to change the location for product inventory at the order line level.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing post-fulfillment order changes, Order Management, Use, Sales Customer Relationship Management]
---

# Move order

The move order helps agents to change the location for product inventory at the order line level.

The move order is triggered from the TMF 622 and 641 APIs.

When the action is **Change** and move operation is **true**. Two sets of domain orders and composedof items are created with the action state **Add** and **Change**. The inventory hierarchies present in change domain order are got replicated for add domain order. If the Order Characteristics values are available for change domain order, it gets replicated for add domain order.

The state of inventory for an add domain order becomes **Installation pending**.

The state of inventory for change domain order becomes **Change pending**.

If the move order is canceled for all the product inventory records before the PONR, then all the product inventory records that are associated with the move order are changed to **Active** state from **Change Pending** state.

For all the product inventory records that are in **Activation pending** state are moved to the **Inactive** state, after cancellation is completed.

On successful completion of the order, the old inventory with state **Change pending** becomes **Inactive**. The new inventory with state **Activation pending** becomes **Active**.

**Parent Topic:**[Managing post-fulfillment order changes](managing-orders.md)

