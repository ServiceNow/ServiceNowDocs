---
title: Approve orders in Order Management
description: Approve an order in Order Management to begin decomposition and fulfillment process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Approving orders, Order Management, Use, Sales Customer Relationship Management]
---

# Approve orders in Order Management

Approve an order in Order Management to begin decomposition and fulfillment process.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_fulfilment\_manager, sn\_ind\_tmt\_orm.order\_approver

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace.** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select the order that you want to review and approve.

    Orders ready for approval are in the New state.

5.  Review the order line items.

6.  Select **Reprice** to recalculate prices when updates are made to an order line item.

7.  To add more products to this order, select **New**.

8.  Delete selected order line items by selecting **Delete**.

    When you delete an order line item, the prices are recalculated.

9.  **Note:** Before approving an order, the system validates contract information based on the order line type. For recurring or entitlement offerings, the **Contract start date**, **Contract end date**, and **Term** are required before the order can be approved. For one‑time offerings, **Contract start date** and **Contract end date** must be empty. If these conditions are not met, the order cannot be approved and must be updated by an agent before approval can proceed.

    When you're satisfied with the order details, select **Approve**.


## Result

The order is approved and the order state changes to In progress while it’s being validated, before it enters fulfillment.

