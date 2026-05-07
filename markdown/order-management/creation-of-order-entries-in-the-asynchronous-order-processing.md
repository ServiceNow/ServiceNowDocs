---
title: Create order entries manually during the asynchronous order processing
description: Skip the scheduled job and create order entries manually in the Order Management application for asynchronous order requests.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Asynchronous order processing, Order management, Configure, Sales Customer Relationship Management]
---

# Create order entries manually during the asynchronous order processing

Skip the scheduled job and create order entries manually in the Order Management application for asynchronous order requests.

## Before you begin

Role required: Order Integrator \[sn\_ind\_tmt\_orm.order\_integrator\]

## About this task

Before you can create order entries in the customer order table, records are staged in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. This table helps you to store and manage your order requests during the asynchronous processing of orders.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Inbound Queue Requests** &gt; **All**.

    The Inbound Queue Requests list view provides the following information.

<table id="table_mwd_24r_wvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource

</td><td>

Caller that created the record in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table.

</td></tr><tr><td>

Record id

</td><td>

Unique system-generated ID returned as orderID in the HTTP response.

</td></tr><tr><td>

State

</td><td>

State of the record in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table.-   **New**

Order records created.

-   **In Progress**

Scheduler picks orders and generates a system ID.

-   **Completed**

Scheduler successfully created the customer order record from the Inbound Queue table.

-   **Error**

Scheduler did not successfully create the customer order record.

</td></tr><tr><td>

External ID

</td><td>

External ID of the order from the Configure, Price, and Quote \(CPQ\) system.

</td></tr><tr><td>

Status code

</td><td>

HTTP status codes.-   201: Target record successfully created.
-   202: Record in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table successfully created.
-   400: Target record not created due to an error.


</td></tr><tr><td>

Error message

</td><td>

\(Optional\) Error message returned for an exception.

</td></tr><tr><td>

Payload

</td><td>

Payload received via an API.

</td></tr><tr><td>

System ID

</td><td>

Cluster node ID.

</td></tr><tr><td>

Reference table

</td><td>

Name of the target table, such as Customer Order.

</td></tr></tbody>
</table>4.  From the list, select a record to create an order.

5.  On the Inbound Queue page, select **Create Order**.

    An order is created in the New state and can be viewed by navigating to **Customer Orders** &gt; **All**.


## What to do next

[Approve orders in Order Management](../task/som-om-approve-product-order.md)

**Parent Topic:**[Asynchronous order processing for large customer and consumer orders](asynchronous-order-processing.md)

