---
title: Configure Service Order Fulfillment Policy using Decision Tables
description: Associate fulfillment subflows with the service specifications by using the Service Order Fulfillment Policy in Decision Tables for move order.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales and Order Management]
---

# Configure Service Order Fulfillment Policy using Decision Tables

Associate fulfillment subflows with the service specifications by using the Service Order Fulfillment Policy in Decision Tables for move order.

## Before you begin

Role required: admin

## About this task

Add rows to the Service Order Fulfillment Policy decision table to specify which products should go through fulfillment. Add the service fulfillment subflow to a new row in this table with the appropriate conditions​​. Conditions can be a combination of action, category, and move operation.

## Procedure

1.  Navigate to **All** &gt; **Decision Builder**.

2.  Select the **Service Order Fulfillment Policy** decision table.

3.  To trigger the subflow configured for move, do the following:

    1.  Select **true** in the Move Operation column.
    2.  Select **Change** in the action column.
    ![service order fulfillment policy.](../image/service-order-fulfillment-policy.png)

4.  To trigger the separate subflow for change, do the following:

    1.  Select **Change** in action column.
    2.  Select **false** in the move operation column.
5.  Select **Save**.


## Result

A list of subflows appear in the results section. These sub flows create the fulfillment tasks for an order line item during the fulfillment process. For more information, see [Decision Builder user interface](https://www.servicenow.com/docs/access?context=decision-builder-user-interface&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Parent Topic:**[Configuring Order Management](../concept/order-mgt-configuring.md)

