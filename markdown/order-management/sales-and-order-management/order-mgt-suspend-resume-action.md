---
title: Suspend and resume products and services
description: You can use suspend and resume actions to temporarily suspend or inactivate your product and service inventories. That way, you can capture a customer's suspend request and resume the products and services later.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Managing post-fulfillment order changes, Order Management, Use, Sales Customer Relationship Management]
---

# Suspend and resume products and services

You can use suspend and resume actions to temporarily suspend or inactivate your product and service inventories. That way, you can capture a customer's suspend request and resume the products and services later.

## About suspend and resume actions

You can temporarily suspend or inactivate your product and service inventories. The suspend and resume requests are managed as orders with the changes in the inventory of the product and service orders during the order decomposition and fulfillment process. An order suspension and resume action can occur immediately or at a future date.

With suspend and resume actions, you can do the following tasks:

-   Ingest and fulfill the suspend product and service orders.
-   Ingest and fulfill the resume product and service orders for suspended inventories.
-   Support future-dated suspend and resume orders by using a scheduler.
-   Manage the product inventory state for suspend and resume scenarios.

## How the Suspend and Resume actions work

The process for the suspend and resume actions is as follows:

1.  A customer order of type Suspend or Resume is received in the order management system. After reviewing the order details, a fulfillment manager approves the customer order.
2.  When a customer order is approved, a new Product Inventory Operations \[sn\_prd\_invt\_product\_inventory\_operations\] table is created as a related list in the order line items form. In case of scheduled scenario, as part of fulfillment process the state of the product inventory operations record marks to Scheduled state for order line items.
3.  A pre-configured scheduler tracks the Product Inventory Operations table to check for any future scheduled date of the customer order:
    -   If your customer order contains order line items with a future date \(a date value for the `committedDueDate` field on the order line items form\), the suspend or resume action starts on the scheduled date.
    -   If your customer order doesn't include any date for the suspend or resume action, it starts immediately at the time of closure of the orders.
4.  At the time of order closure, the following changes occur:
    -   For a scheduled scenario, the scheduler picks up the record with a Scheduled state from the Product Inventory Operations table on the scheduled date and marks the record state to Completed. And the inventory state of the order line item is updated to Suspended for the suspend action and to Active for the resume action in the product inventory table.
    -   For an immediate scenario, the state of the record in the Product Inventory Operations table is updated to Completed. And the inventory state of the order line item is updated to Suspended for the suspend action and to Active for the resume action in the product inventory table.
5.  The inventory state in the Product Inventory Operations table is updated to Canceled in the following two scenarios:
    -   During the inflight changes or due to the cancellation of any order line items.
    -   The dates for both the suspend and resume operations are scheduled, but the date for the resume operation is before the date of the suspend operation.

## Additional validations and scenarios

When the order line items for the suspend or resume actions are combined with the change or disconnect actions in a single order and the inventory state of any order line item is in a pending state, the order approval fails. The reason is due to the approval validation for the change or disconnect order.

**Note:** During the order approval for suspend or resume or no change actions, the product inventory should not be in the Installation Pending state.

In the order creation process for the suspend or resume actions, the `committedDueDate` field value on the order line item form can be a past date, present date, or a future date. If it's a past or present date, the inventory state should be set as Active for the suspend action and set as Suspended for the resume action.

If the `committedDueDate` field value of the customer order line items is invalid \(the date field value exceeds the calendar date\) for the suspend or resume action, it's then considered as an immediate action.

In the suspend or resume type of customer orders, the parent order has precedence over a child order. If the parent order is scheduled for an immediate suspend or resume action, but the child order is scheduled for any future date, the entire inventory hierarchy is considered for the immediate action.

If the top order line item for suspend or resume action is scheduled for a future date, the entire inventory hierarchy is then considered for the suspend or resume action. Child order line items are considered for suspend or resume action when they’re combined with a change or a no-change action.

For an inflight change of the suspend or resume type order, only Cancellation is supported. If an order line item or the entire order gets canceled, the Product inventory Operations record is marked as Canceled during the order fulfillment process. The state change doesn't occur for the Product inventory record.

In the order creation process for the suspend or resume action, you can use the external inventory ID in the payload instead of the system-generated ID for the inventory.

**Parent Topic:**[Managing post-fulfillment order changes](managing-orders.md)

