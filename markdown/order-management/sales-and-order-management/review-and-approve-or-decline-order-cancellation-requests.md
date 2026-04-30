---
title: Review and approve order revisions or cancellation requests
description: Review a customer or service order that has a pending revision or cancellation request so that you can make sure that the order is correct and complete. You can also approve the order and order line item revisions or cancellations requests.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing inflight order changes and cancellation requests, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Review and approve order revisions or cancellation requests

Review a customer or service order that has a pending revision or cancellation request so that you can make sure that the order is correct and complete. You can also approve the order and order line item revisions or cancellations requests.

## Before you begin

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.order\_fulfillment\_manager, sn\_ind\_tmt\_orm.service\_order\_manage, sn\_ind\_tmt\_orm.service\_order\_agent

## About this task

When you approve a revised order, it enables it to continue in its modified state through the rest of the fulfillment process. When you approve a cancellation request, it finalizes the cancellation and prevents the order from continuing through fulfillment processing.

To learn more about how the states of orders change when you approve them, see [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#).

## Procedure

1.  Navigate to **All** &gt; **Customer Order Management** &gt; **Workspace** &gt; **Configurable Workspace Home**.

2.  Select the customer order or service order that you want to approve revisions or cancellation requests for.

3.  In the customer order or service order, review the revision or cancellation request, and then click **Save** if you made any changes.

4.  To formally approve the order revision or cancellation, click **Approve**.


## Result

Orders with unapproved revisions have a Revision in Progress state. When you approve them, their state changes to In Progress. Orders with unapproved cancellation requests have an Assessing the Cancellation state. When you approve them, their order state changes to Cancellation in Progress.

**Parent Topic:**[Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)

