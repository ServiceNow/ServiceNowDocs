---
title: Configuring inflight changes
description: You can use inflight change order management to manage the receipt of changes for customer or service orders that are still in the process of being orchestrated and fulfilled.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales and Order Management]
---

# Configuring inflight changes

You can use inflight change order management to manage the receipt of changes for customer or service orders that are still in the process of being orchestrated and fulfilled.

Inflight change order management handles modifications to orders that are already in progress after submission but before fulfillment is complete. This capability is essential for real-world scenarios where customers need to adjust quantities, swap products, change configurations, or cancel portions of an order while fulfillment activities are already underway.

Inflight change order management enables you to decide when you permit such changes to ongoing orders, assesses the impact of the requested changes for an order, and automatically generates a compensation plan for them.

**Note:** Characteristic, Contact, Quantity, or Price inflight revision types are standard in the ServiceNow AI Platform but you can define additional ones as per the requirements of your enterprise. To learn more, see the "Types of Inflight order changes" section in the [Managing inflight order changes and cancellation requests](inflight-order-change-mgt-overview.md).

-   **[Create additional inflight order change types](../task/define-inflight-order-change-types.md)**  
Define your own enterprise-specific inflight order change types that are used to categorize revisions or requests for cancellations, product orders, service orders, and their related line items.
-   **[Configuring order tasks to respond to inflight revision and cancellation requests](../task/configuring-order-tasks-respond-to-inflight-revision-cancellation-requests.md)**  
Configure your order task records to respond to inflight order changes and cancellation requests using Workflow Studio.

**Parent Topic:**[Configuring Order Management](order-mgt-configuring.md)

