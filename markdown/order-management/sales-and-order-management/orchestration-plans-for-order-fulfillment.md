---
title: Using the order orchestration UI
description: By using the order orchestration user interface \(UI\), you can make sure that you do all the tasks that are required to fulfill your customer orders. You can also view the complete order hierarchy, the status of the associated decomposed orders, the order line items, and the order tasks.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order orchestration, Order Management, Use, Sales and Order Management]
---

# Using the order orchestration UI

By using the order orchestration user interface \(UI\), you can make sure that you do all the tasks that are required to fulfill your customer orders. You can also view the complete order hierarchy, the status of the associated decomposed orders, the order line items, and the order tasks.

As an order fulfillment manager or agent, the order orchestration UI is your command center for managing the end-to-end fulfillment process. Use the order orchestration UI to track all domain orders and order tasks for an order, order line item, or domain order. You can also use the UI to review and resolve any issues for related order tasks and domain orders.

## Accessing the UI

You can access the order orchestration UI in the following two ways:

-   From the Order Details page: Go to the Order breakdowns section and select **View order orchestration**.

-   From individual order lines: Open an order line item, then navigate to the **Order Orchestration** tab.


Use the order orchestration UI to see:

-   A pictorial representation that shows the hierarchy of all order line items, domain orders, and order tasks for an order, order line item, or a domain order.
-   The dependencies between the domain orders and order tasks.
-   The current state of the associated order line items, domain orders, and order tasks in the hierarchy.

The following image shows the order orchestration UI:

![Infographic showing order orchestration tab view of a order. For text description, refer to using order orchestration UI for fulfillment section.](../image/orchestration-plan-ui.png "Order orchestration UI")

By using the order orchestration UI, you can perform the following actions:

-   View a hierarchical visual representation of all order line items, domain orders, and order tasks for the selected order.
-   Open a node in the hierarchy and view the additional details.
-   Determine the current state of the associated order line items, domain orders, and order tasks.
-   Identify any order delays or fallouts in the order fulfillment process, and resolve them on time.

## Fulfilling multi-site orders

The order orchestration UI is especially helpful when you fulfill customer orders that involve multiple products that are fulfilled at multiple locations. For example, a customer orders the SD-WAN Service Package for their San Jose, San Diego, Denver, and Dallas locations. That means that there’s a minimum of three order line items for each of the four locations:

-   One line item for the SD-WAN Service Package
-   One line item for the SD-WAN Controller product
-   One line item for the SD-WAN Edge product

If the same customer also orders an optional SD-WAN Security product for each location, there would be an extra four order line items. That is, there's one order line item for each of the four locations \(San Jose, San Diego, Denver, and Dallas\).

To initiate the fulfillment process for a multi-site order, the Order Management application decomposes the order into multiple domain orders for fulfillment. The domain orders are the product, service, and resource orders that are generated during decomposition. Each decomposed order has a corresponding fulfillment flow with several order tasks. To fulfill an order by the delivery dates that you promise to your customer, you must complete all the related domain orders and resolve all the related order tasks on time.

**Parent Topic:**[Order orchestration](order-orchestration.md)

**Related topics**  


[Order fulfillment](reviewing-orchestration-plans-order-fulfillment.md)

[Review an order orchestration plan](../task/review-order-fulfillment-orchestration-plan.md)

[Managing order fallout](fallout-management-overview.md)

