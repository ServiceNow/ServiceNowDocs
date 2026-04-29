---
title: Review an order orchestration plan
description: Track the progress of an order in the fulfillment process by reviewing the orchestration plan for the order, its order line items, and domain product, service, or resource orders. By using the order orchestration UI, you can easily identify and resolve any delays or fallouts so that you can do the order fulfillment process more efficiently.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Order fulfillment, Order Management, Use, Sales and Order Management]
---

# Review an order orchestration plan

Track the progress of an order in the fulfillment process by reviewing the orchestration plan for the order, its order line items, and domain product, service, or resource orders. By using the order orchestration UI, you can easily identify and resolve any delays or fallouts so that you can do the order fulfillment process more efficiently.

## Before you begin

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.order-fulfillment\_agent, sn\_ind\_tmt\_orm.order\_fulfillment\_manager, sn\_ind\_tmt\_orm.service\_order\_manager

## About this task

By using the order orchestration UI, you can perform the following actions:

-   View a hierarchical visual representation of all order line items, domain orders, and order tasks for the selected order.
-   Open a node in the hierarchy and view the additional details.
-   Determine the current state of the associated order line items, domain orders, and order tasks.
-   Identify any order delays or fallouts in the order fulfillment process, and resolve them on time.

To learn more, see [Using the order orchestration UI](../concept/orchestration-plans-for-order-fulfillment.md).

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders**.

    -   To view all customer orders, select **All**.
    -   To view only open, unfulfilled customer orders, select **Open**.
4.  Select an order you want to fulfill.

5.  Access the order orchestration UI for a selected order, order line item, or domain order by performing the respective task from the following table.

<table id="choicetable_u3t_rjd_54b"><thead><tr><th align="left" id="d42826e133">

Task

</th><th align="left" id="d42826e136">

Description

</th></tr></thead><tbody><tr><td id="d42826e142">

**Review the orchestration plan for an entire customer order**

</td><td>

In the Customer Order form, under Order breakdowns, select **View order orchestration**.

</td></tr><tr><td id="d42826e154">

**Review the orchestration plan for a customer order line item**

</td><td>

1.  On the Order Details page, select an order line item from the **Line items** tab.
2.  Select the **Order Orchestration** tab.


</td></tr><tr><td id="d42826e178">

**Review the orchestration plan for a domain order associated with a customer order line item**

</td><td>

To view the orchestration plan for a domain order \(product, service, or resource\), perform the following steps:1.  On the Order Details page, select an order line item from the **Line items** tab.
2.  Navigate to the one of the following tabs for which you want to view the orchestration details:
    -   **Product Orders**
    -   **Service Orders**
    -   **Resource Orders**
3.  Select the **Order Orchestration** tab.


</td></tr></tbody>
</table>6.  On the order orchestration UI, review the visual representation of the order, including all domain product, resource, service orders, order tasks, and their current states as described in the following table.

<table id="table_as2_qdv_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ORD

</td><td>

Unique system-assigned number for the customer order. Both customer orders and service orders have an assigned ID with a prefix of ORD.

</td></tr><tr><td>

Address, city, state

</td><td>

Orchestration plan hierarchy level that represents the individual shipping locations for the domain orders of an order line item.

</td></tr><tr><td>

Order line item

</td><td>

Orchestration plan hierarchy level that contains the individual order line items that are associated with each shipping location. An order line item can also contain child line items, which are shown in the order hierarchy. Each order line item contains the following elements: -   **Description**

Description of the product or service ordered on this line item.

-   **Order line item identifier**

System-assigned customer or service order line item number.

-   **Task overview**

Overview of the total number of domain orders and order tasks that are associated with the order line item that have been fulfilled.

</td></tr><tr><td>

Domain orders and order tasks

</td><td>

Orchestration plan hierarchy level that contains the individual domain orders and order tasks for an order line item. A domain order can also contain child domain orders, which are shown in the order hierarchy. Each domain order or order task contains the following elements:

-   **Type**

Type of related transaction:

    -   Domain order - Product Order, Service Order, or Resource Order
    -   Order Task
-   **Description**

Description of the product or service on this domain order or order task.

-   **Identifier**

System-assigned domain product or order task number.

-   **State**

Current state of the domain product or order task. To learn more, see:

    -   [Customer order states](../reference/order-mgt-state-values.md)
    -   [Service order states](../reference/service-order-mgt-state-values.md)


</td></tr></tbody>
</table>
## What to do next

[Review and close fulfillment tasks](order-mgt-customer-order-tasks.md)

**Parent Topic:**[Order fulfillment](../concept/reviewing-orchestration-plans-order-fulfillment.md)

**Related topics**  


[View an order timeline](view-order-timelines.md)

