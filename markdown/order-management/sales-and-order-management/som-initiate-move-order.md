---
title: Start a move order
description: Start a move order to update product inventory location.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Start a move order

Start a move order to update product inventory location.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

A move order enables agents to change the location for product inventory at the order line level. The move order is executed using the change order function in Order Management.

Once the move order is started, the updated location is propagated to the selected inventory.

## Procedure

1.  In the **Configurable Workspace**, select the **List** ![](../image/Lists.png) view.

2.  Open the order line item that requires an inventory location change and update the location field, then select **Save**.

3.  Return to the **Customer Orders** form and select **New**.

4.  In the **Create a new Order** dialog box, select an **Account** and then under **Order action**, select **Change**.

    ![New order interceptor dialog showing the order action as change.](../image/som-change-order-interceptor.png)

5.  From the **Catalog**, select **Manage** to open the order line for the location change.

6.  Navigate to the **location** field in the order line and update to the location.

7.  Select **Update**.

8.  Review the changes that you made and select **Review &amp; Submit**.

    The change order is propagated through all affected order lines and order tasks.


**Parent Topic:**[Create an order in Order Management](som-create-product-order.md)

