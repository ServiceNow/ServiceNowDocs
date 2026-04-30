---
title: Using Order Management
description: You can manage and fulfill customer orders and service orders in the Order Management application.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Using Order Management

You can manage and fulfill customer orders and service orders in the Order Management application.

## Action types for orders

The Order Management application supports the following types of customer and service orders.

|Order action type|Description|
|-----------------|-----------|
|Add|Add a customer order that is not associated with an existing order from the same customer.|
|Change|Change an existing order, which changes a previously ordered or fulfilled product or service.|
|Delete|Deletion of an existing customer order line item or product order.|

## Methods for capturing orders

You can capture customer \(product\) and service orders from the following sources:

-   Your agents can capture customer and service orders using the CSM Configurable Workspace.
-   If you have a Telecommunications Service Management subscription, you can capture orders from the following:
    -   Third-party order management systems through the Product Ordering Open \(TMF622\) or Service Order Open \(TMF641\) APIs.
    -   Through the Service Exchange in the San Diego and later releases.

-   **[Create an order in Order Management](../task/som-create-product-order.md)**  
Create a product or service order in Order Management.
-   **[Managing inflight order changes and cancellation requests](inflight-order-change-mgt-overview.md)**  
Manage how your organization receives changes for customer orders, service orders or individual line items that are still being orchestrated and fulfilled. By using inflight change order management, you can designate when you permit such changes. You can also assess the impact of the requested changes for an order or order line item, and automatically generate a plan to compensate for them when you approve the revision or cancellation request.
-   **[Managing order fallout](fallout-management-overview.md)**  
Learn how Fallout Management enables you to identify, investigate, and resolve order issues so that orders can be processed to completion.
-   **[Reviewing customer or partner accounts](reviewing-customer-accounts.md)**  
Learn how your order entry and fulfillment agents, managers, and fulfillers can use the 360 View in the Order Management application to get a better perspective about the activity that is associated with a customer's or partner's account.
-   **[View an order timeline](../task/view-order-timelines.md)**  
View Gantt chart timelines that display the status of a domain order and order tasks, show dependencies between order tasks, and identify tasks that are in jeopardy.
-   **[Monitoring Jeopardy Management](../task/monitoring-jeopardy-management.md)**  
Order managers and agents can monitor jeopardy-enabled fulfillment tasks. When a task enters jeopardy, managers can take action to ensure the fulfillment workflow isn’t delayed.

**Parent Topic:**[Using Sales Customer Relationship Management applications](som-using.md)

