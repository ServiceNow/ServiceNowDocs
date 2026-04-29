---
title: Order quantity support
description: Learn how you can support and fulfill your customer orders for multiple instances of a product or service. You can create multiple domain orders that equal the order quantity for each instance of the product or service. This way, you can efficiently decompose and manage the fulfillment of your customer orders.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add products or services, Creating orders, Order Management, Use, Sales and Order Management]
---

# Order quantity support

Learn how you can support and fulfill your customer orders for multiple instances of a product or service. You can create multiple domain orders that equal the order quantity for each instance of the product or service. This way, you can efficiently decompose and manage the fulfillment of your customer orders.

## Example of order quantity

An instance of a product or service refers to an ordered item with a unique set of order characteristic values, such as the speed and memory size. A customer might order the same top-level product or service for different locations, but each might differ in their order characteristics. For example, if a customer orders a router for one of their locations, it might have a memory size selection that varies from the same router model that was ordered for another location. Order Management supports this order quantity processing for the following scenarios:

## Support for the order line item quantity that is provided by the customer when they order an item

If your customer places an order with more than one instance, the Quantity field on the order line item captures the number of instances of your customer order line items. The order decomposition process then creates the same number of product or service orders and manages the fulfillment process for each order independently.

## Support for the catalog-driven characteristic quantity

In this scenario, the decomposition process decomposes a product or service order into the required number of domain orders. These domain orders are based on the quantity mapping that you define in the product catalog between the source and target specifications that are used in a product offering. The quantity mapping in the specification relationship triggers the decomposition process to create the required number of domain orders for the fulfillment process.

## Support for the characteristic based quantity

In this scenario, you accept and support your customer order that has the information for order characteristics value which impacts the quantity of the domain orders. So, the order decomposition process refers to following information to create the required number of domain orders.

-   Specification relationship with quantity characteristic
-   Characteristic mapping

