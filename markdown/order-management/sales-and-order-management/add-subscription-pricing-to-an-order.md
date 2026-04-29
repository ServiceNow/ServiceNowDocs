---
title: Add subscription pricing to an order
description: Add contract pricing to an order or order line items including start and end dates in Order Management.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating orders, Order Management, Use, Sales and Order Management]
---

# Add subscription pricing to an order

Add contract pricing to an order or order line items including start and end dates in Order Management.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

Subscription pricing is a pricing model where customers pay a recurring fee for products or services, typically at regular intervals such as monthly or annually.

In an order, you can set the contract start date and end date, or you can enter a term and the contract end date is automatically calculated.

Subscription pricing can be added at the order header level or at the order line item level.

See [Subscription revenue metrics](../concept/som-subscription-pricing.md) for more information about how contract pricing works.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Orders** &gt; **All**

3.  Select the order that you’re working with.

4.  Select the More Actions icon ![](../image/icon-three-dot-menu.png) and select **Order details**.

5.  In the **Order Details** tab, add a **Contract start date** and a **Contract end date**.

    When the dates are entered, the following information automatically updates.

    |Field|Description|
    |-----|-----------|
    |Total monthly recurring price|Shows the monthly recurring price based on the dates entered in subscription pricing.|
    |Total annual recurring price|Shows the total annual recurring subscription pricing based on the dates entered.|
    |Total amount|Shows the total amount of the subscription pricing according to the contract start and end dates.|
    |Term|Shows the number of months the subscription is valid based on the contract start and end dates.|

6.  Select **Update**.


**Related topics**  


[Order details page - Dates fields](../reference/field-descriptions-customer-orders.md#)

