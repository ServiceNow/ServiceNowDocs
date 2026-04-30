---
title: Staggered decomposition
description: Learn how you can stagger the decomposition for your customer orders. You can decompose your customer orders in multiple iterations by using the available information at the domain level, rather than decomposing an entire customer order at one time after it is approved for fulfillment.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Staggered decomposition

Learn how you can stagger the decomposition for your customer orders. You can decompose your customer orders in multiple iterations by using the available information at the domain level, rather than decomposing an entire customer order at one time after it is approved for fulfillment.

The following diagram shows how the staggered decomposition process works. You can start the decomposition process with the information that you already have for your order and order line items. The decomposition process skips the domain orders \(product or service or resource orders\) that you don't have the required information for at this time. When you add this information later, the decomposition process triggers and completes the processing for the remaining domain orders.

![Workflow showing the staggered decomposition process. For the text description, refer to the preceding paragraph.](../image/staggered-decomposition.png "Staggered decomposition processing")

## Contrast to earlier decomposition processing

Before staggered decomposition was available, order decomposition processing started immediately after a customer order was approved for fulfillment. Order decomposition was based on the specification relationships and decomposition rules that were defined in the product catalog.

If the decomposition rule depended on any characteristic value that was not available at the time of order decomposition, the order processing skipped the decomposition of orders. However, in staggered decomposition, with the initial decomposition, the decomposition automatically triggers again for the skipped orders when the dependent characteristic value is available. The characteristic value can be set by your order fulfillment users or by the attribute propagation rules.

## How staggered decomposition works

To support order decomposition in a staggered manner, you can use this method to retrigger the decomposition process for the skipped domain orders when the characteristic values are assigned in the corresponding decomposition rules.

When you approve an order, the order decomposition process starts. The decomposition process creates domain orders by using the information that is available from the order, order line items, and catalog definition. It also evaluates the decomposition rules to create the target domain orders. If the decomposition feature fails to evaluate the decomposition rules due to the unavailability of characteristic values, the decomposition is stopped for those domain orders.

When the characteristic values are available either from a user’s action or from an attribute propagation rule, the decomposition process is retriggered. The process then creates the required domain orders and completes the order decomposition. If you again update the characteristic value after the order decomposition is complete, it does not trigger the decomposition for the domain order.

