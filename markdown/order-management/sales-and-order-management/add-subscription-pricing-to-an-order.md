---
title: Add subscription pricing to an order
description: Add contract pricing to an order or order line items including start and end dates in Order Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Add subscription pricing to an order

Add contract pricing to an order or order line items including start and end dates in Order Management.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

Subscription pricing is a model where customers pay a recurring fee for products or services, typically at regular monthly or annually.

In an order, you can set the contract start date and end date, or you can enter a term and the contract end date is automatically calculated.

Subscription pricing can be added at the order header level or at the order line item level.

See [Subscription revenue metrics](../concept/som-subscription-pricing.md) for more information about how contract pricing works.

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**

4.  Select the order that you’re working with.

5.  Select the More Actions icon ![](../image/icon-three-dot-menu.png) and select **Order details**.

6.  In the **Dates** section, add a **Contract start date** and a **Contract end date**.

    When the dates are entered, the following information automatically updates.

    |Field|Description|
    |-----|-----------|
    |Total monthly recurring price|Shows the monthly recurring price based on the dates entered in subscription pricing.|
    |Total annual recurring price|Shows the total annual recurring subscription pricing based on the dates entered.|
    |Total amount|Shows the total amount of the subscription pricing according to the contract start and end dates.|
    |Term|Shows the number of months the subscription is valid based on the contract start and end dates.|

7.  Select **Update**.


**Related topics**  


[Order details page - Dates fields](../reference/field-descriptions-customer-orders.md#)

