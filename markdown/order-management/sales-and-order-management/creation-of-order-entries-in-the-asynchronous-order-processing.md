---
title: Create order entries manually during the asynchronous order processing
description: Skip the scheduled job and create order entries manually in the Order Management application for asynchronous order requests.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Asynchronous order processing, Order management, Configure, Sales Customer Relationship Management]
---

# Create order entries manually during the asynchronous order processing

Skip the scheduled job and create order entries manually in the Order Management application for asynchronous order requests.

## Before you begin

Role required: admin

## About this task

Before you can create the order entries in the customer order table, all these records are staged in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. This table helps you to store and manage your order requests during the asynchronous processing of orders.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate **Inbound Queue Requests** &gt; **All**.

    The following table describes the details displayed on the list view.

<table id="table_mwd_24r_wvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record ID

</td><td>

System-generated ID of the target table.

</td></tr><tr><td>

State

</td><td>

State of the record in the Inbound Queue.-   **New**

The order records are created.

-   **In Progress**

When the scheduler picks the orders and generates a system ID.

-   **Completed**

The scheduler has successfully created the customer order record from the Inbound Queue table.

-   **Error**

If the scheduler doesn't successfully create the customer order record.

</td></tr><tr><td>

External ID

</td><td>

External ID of the order from the Configure, Price, and Quote \(CPQ\) system.

</td></tr><tr><td>

Status Code

</td><td>

HTTP status codes. If the target record is created successfully, it displays 2xx or 4xx.-   **201**

If the target record is successfully created.

-   **202**

If the record in the Inbound Queue table is successfully created.

-   **400**

If the target record isn’t created due to any error.

</td></tr><tr><td>

Resource

</td><td>

Information about which caller created the record in the inbound queue table​.

</td></tr><tr><td>

Error message

</td><td>

\(Optional\) Error message that is returned for an exception​.

</td></tr><tr><td>

Payload

</td><td>

Payload that was received via an API​.

</td></tr><tr><td>

System ID

</td><td>

Cluster node ID.

</td></tr><tr><td>

Reference table

</td><td>

Name of the target table.

</td></tr></tbody>
</table>4.  Select a record using which you want to create an order.

5.  On the Inbound Queue page, select **Create Order**.

    An order is created in the New state and can be viewed by navigating to **Customer Orders** &gt; **All**.


## What to do next

[Approve orders in Order Management](../task/som-om-approve-product-order.md)

**Parent Topic:**[Asynchronous order processing for large customer and consumer orders](asynchronous-order-processing.md)

