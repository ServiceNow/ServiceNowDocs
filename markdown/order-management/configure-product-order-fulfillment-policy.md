---
title: Configure product order fulfillment policy using Decision Tables
description: Associate fulfillment subflows with the product specifications by using the Product Order Fulfillment Policy in Decision Tables for move order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-product-order-fulfillment-policy.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Configure product order fulfillment policy using Decision Tables

Associate fulfillment subflows with the product specifications by using the Product Order Fulfillment Policy in Decision Tables for move order.

## Before you begin

Role required: admin

## About this task

Add rows to the Product Order Fulfillment Policy decision table to specify which products should go through fulfillment. Add the product fulfillment subflow to a new row in this table with the appropriate conditions​​. Conditions can be a combination of action, category, and move operation.

## Procedure

1.  Navigate to **All** &gt; **Decision Builder**.

2.  Select the **Product Order Fulfillment Policy** decision table.

3.  To trigger the subflow configured for move, do the following:

    1.  Select **true** in the Move Operation column.
    2.  Select **Change** in the action column.
    \[Omitted image "product-order-fulfillment-policy.png"\] Alt text: product order fulfillment policy.

4.  To trigger separate subflow for change and not move, do the following:

    1.  Select **Change** in action column.
    2.  Select **false** in the move operation column.
5.  Select **Save**.


## Result

A list of subflows appear in the results section. These sub flows create the fulfillment tasks for an order line item during the fulfillment process. For more information, see [Decision Builder user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/decision-builder-user-interface.md).

**Parent Topic:**[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-configuring.md)

**Related topics**  


[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md)

[Using Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-order-management.md)

