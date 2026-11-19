---
title: Configuring inflight changes
description: You can use inflight change order management to manage the receipt of changes for customer or service orders that are still in the process of being orchestrated and fulfilled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/configure-inflight-order-change-mgt.html
release: zurich
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Configuring inflight changes

You can use inflight change order management to manage the receipt of changes for customer or service orders that are still in the process of being orchestrated and fulfilled.

Inflight change order management handles modifications to orders that are already in progress after submission but before fulfillment is complete. This capability is essential for real-world scenarios where customers need to adjust quantities, swap products, change configurations, or cancel portions of an order while fulfillment activities are already underway.

Inflight change order management enables you to decide when you permit such changes to ongoing orders, assesses the impact of the requested changes for an order, and automatically generates a compensation plan for them.

**Note:** Characteristic, Contact, Quantity, or Price inflight revision types are standard in the ServiceNow AI Platform but you can define additional ones as per the requirements of your enterprise. To learn more, see the "Types of Inflight order changes" section in the [Managing inflight order changes and cancellation requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/inflight-order-change-mgt-overview.md).

-   **[Create additional inflight order change types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/define-inflight-order-change-types.md)**  
Define your own enterprise-specific inflight order change types that are used to categorize revisions or requests for cancellations, product orders, service orders, and their related line items.
-   **[Configuring order tasks to respond to inflight revision and cancellation requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configuring-order-tasks-respond-to-inflight-revision-cancellation-requests.md)**  
Configure your order task records to respond to inflight order changes and cancellation requests using Workflow Studio.

**Parent Topic:**[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/order-mgt-configuring.md)

