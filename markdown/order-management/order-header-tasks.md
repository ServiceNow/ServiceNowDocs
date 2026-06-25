---
title: Order header tasks
description: Order header tasks are associated with an order at the header or top order line item level, independent of domain orders or fulfillment tasks. They can be generated automatically or created manually to support validation and coordination activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/order-header-tasks.html
release: australia
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 2
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Order header tasks

Order header tasks are associated with an order at the header or top order line item level, independent of domain orders or fulfillment tasks. They can be generated automatically or created manually to support validation and coordination activities.

## Overview of order header tasks

Order header tasks extend the standard order task model to support task association at the order header level and the top order line item \(OLI\) level. Order header tasks operate independently of fulfillment logic and product specifications, unlike enrichment and fulfillment tasks that are tied to specific domain orders or order line items.

Order header tasks can be generated at three stages of the order life cycle:

-   After order submission
-   After order approval
-   After order fulfillment

## Task categories

Two task categories are introduced to differentiate order header tasks from existing enrichment and fulfillment tasks:

-   Order Header: Associated with the order at the header level, based on order-level parameters such as account and order action.
-   Top OLI: Associated with the top order line item, based on parameters available at the order line item level, such as product offering and order line item action.

## Automatic task generation

Order header tasks and top order line item tasks are generated automatically based on conditions configured in the Customer Order Task Policy decision table. Conditions can use any parameters available at the order or order line item level. For example:

-   Order header tasks can be triggered by account and order action.
-   Top order line item tasks can be triggered by product offering and order line item action.

For more information, see [Configure the customer order task policy using Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-order-task-policy.md).

## Manual task creation

Order agents can create order header tasks manually from the CSM Configurable Workspace. When an agent creates a task from the Order Tasks tab, the order number is automatically populated and is read-only.

For more information, see [Create an order header task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-order-header-task.md).

**Related topics**  


[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-configuring.md)

[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md)

