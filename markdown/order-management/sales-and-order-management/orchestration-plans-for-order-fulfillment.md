---
title: Orchestration plans for order fulfillment
description: By using the Orchestration Plan user interface \(UI\), you can make sure that you do all the tasks that are required to fulfill your customer \(product\) orders. You can also view the complete order hierarchy, the status of the associated decomposed orders, the order line items, and the order tasks.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Orchestration plans for order fulfillment

By using the Orchestration Plan user interface \(UI\), you can make sure that you do all the tasks that are required to fulfill your customer \(product\) orders. You can also view the complete order hierarchy, the status of the associated decomposed orders, the order line items, and the order tasks.

## Using the Orchestration Plan UI

As an order fulfillment manager or agent, you use the Orchestration Plan UI to track all related domain orders and order tasks for an order, order line item, or domain order. You can also use the UI to review and resolve any issues for related order tasks and domain orders.

The following example shows the Orchestration Plan UI:

![Infographic showing order orchestration tab view of a order. For text description, refer to using orchestration plan UI for fulfillment section.](../image/orchestration-plan-ui.png "Orchestration Plan UI")

Use the Orchestration Plan UI to see:

-   A pictorial representation that shows the hierarchy of all order line items, domain orders, and order tasks for an order, order line item, or a domain order.
-   The dependencies between the domain orders and order tasks.
-   The current state of the associated order line items, domain orders, and order tasks within the hierarchy.

By using the Orchestration Plan UI, you can perform the following actions:

1.  View a hierarchical visual representation of all order line items, domain orders, and order tasks for the selected order.
2.  Open a node in the hierarchy and view the additional details.
3.  Determine the current state of the associated order line items, domain orders, and order tasks.
4.  Identify any order delays or fallouts in the order fulfillment process, and resolve them on time.

## Fulfilling multi-site orders

The Orchestration Plan UI is especially helpful when you fulfill customer orders that involve multiple products that are fulfilled at multiple locations. For example, a customer orders the SD-WAN Service Package for their San Jose, San Diego, Denver, and Dallas locations. That means that there’s a minimum of three order line items for each of the four locations:

-   One line item for the SD-WAN Service Package
-   One line item for the SD-WAN Controller product
-   One line item for the SD-WAN Edge product

If the same customer also orders an optional SD-WAN Security product for each location, there would be an extra four order line items. That is, there's one order line item for each of the four locations \(San Jose, San Diego, Denver, and Dallas\).

To initiate the fulfillment process for a multi-site order, the Order Management application decomposes the order into multiple domain orders for fulfillment. The domain orders are the product, service, and resource orders that are generated during decomposition. Each decomposed order has a corresponding fulfillment flow with several order tasks. To fulfill an order by the delivery dates that you promise to your customer, you must complete all the related domain orders and resolve all the related order tasks on time.

**Note:** To learn about the Order Management data model and order decomposition, see:

-   [Order Management data model](../reference/order-mgt-order-data-model.md)
-   

**Related topics**  


[reviewing-orchestration-plans-order-fulfillment]

[Managing order fallout](fallout-management-overview.md)

