---
title: Customer order decomposition
description: Learn about the customer order decomposition, including quantity-based decomposition, handling change orders with updated quantity characteristics, and support for quantity revisions in in-flight orders.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Order decomposition, Order Management, Use, Sales Customer Relationship Management]
---

# Customer order decomposition

Learn about the customer order decomposition, including quantity-based decomposition, handling change orders with updated quantity characteristics, and support for quantity revisions in in-flight orders.

## Quantity-based decomposition

Quantity based decomposition enables you to decompose your order into separate domain orders as per the order quantity to manage the fulfillment process and independently. This method also supports:

-   Revision of order line item quantity for in-flight orders to fulfill customer’s request to modify \(increase or decrease\) the quantity of the order.
-   Support for change of product order to fulfill a customer's request to update the quantity characteristics. It leads to either the creation of new product inventories or the cancellation of existing product inventories.

## Support for a change order with an update for quantity characteristics

When you receive a customer request to revise an order through changing a product characteristic or characteristic value, you can upgrade or downgrade an existing product inventory. As a part of the fulfillment process, you either create new product inventories or cancel existing product inventories.

-   If a change in a quantity characteristic option leads to additional new product inventories, the decomposition process creates the domain orders for the target specification and inventories for the fulfillment process.
-   If a change in a quantity characteristic option leads to the cancellation of some existing inventories, the decomposition process creates the domain orders needed to manage both the cancellation and changes to the inventories.
    -   The fulfillment process notifies the order fulfillment manager to identify the inventories require cancellation or update.
    -   The decomposition process sets the **Needs Attention** field to **True** for the domain orders.
    -   The order fulfillment manager then views these orders in the Needs Attention widget. The order fulfillment manager can wait to open the domain orders, select the product inventories for cancellation, or update it to resume the order decomposition and fulfillment process.

## Support for quantity revision for in-flight orders

When the order fulfillment process is in progress, and you receive a request to revise to increase or decrease an order line item quantity, it is captured as a quantity change. To incorporate the revision, the decomposition process then either creates additional domain orders \(referred to internally as a `+ve change`\) or cancels the existing domain orders \(referred to internally as a `+ve change`\) for the order fulfillment.

-   If the order revision request is for an increase to the order line item quantity, the decomposition process creates new domain orders to match the updated order line item quantity.
-   If the order revision request is for a reduction in the order line item quantity, the decomposition process initiates the cancellation process for some of the domain orders to match the reduced order line item quantity.

**Related topics**  


[Order quantity support in Order Management](order-quantity-support.md)

