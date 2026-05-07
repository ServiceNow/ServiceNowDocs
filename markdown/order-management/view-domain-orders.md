---
title: View domain orders
description: View product, service, or resource orders for tracking the fulfillment process, verifying that all required tasks and suborders are created correctly, and confirming that the order progresses through its life cycle as expected.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order decomposition, Order Management, Use, Sales Customer Relationship Management]
---

# View domain orders

View product, service, or resource orders for tracking the fulfillment process, verifying that all required tasks and suborders are created correctly, and confirming that the order progresses through its life cycle as expected.

## Before you begin

Role required: sn\_ind\_tmt\_orm.fulfillment\_agent, sn\_ind\_tmt\_orm.fulfillment\_manager, or process admin

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select an order for viewing domain orders.

5.  From the **Line items** tab, select an order line item.

6.  Select one of the following options depending on whether your order is a customer or service order.

    -   Customer order: Select **Product Orders** tab to view product orders associated with the order line.
    -   Service order: Select **Service Orders** tab to view service orders associated with the order line.
7.  Select the product or service order record to view the associated child objects.

8.  View the service and resource orders by navigating to the **Service Orders** and **Resource Orders** tabs respectively.

9.  Select **Associated Move Domain Order** tab in the related list to view the cease domain order and provide domain order.

    When a move order is raised, you can view these domain orders in the related lists:

    -   Cease domain order: Shows a domain order linked to an old inventory from the existing service location.
    -   Provide domain order: Shows a domain order linked to a new inventory in the new service location.
10. Select **Associated Composed of Item** tab in the related list to view the cease composed of item and provide composed of item.

    When a move order is raised, you can view these composed of items in the related lists:

    -   Cease composed of item: Shows old composed of Items from the existing service location.
    -   Provide composed of item: Shows new Composed of Items in the new service location.

