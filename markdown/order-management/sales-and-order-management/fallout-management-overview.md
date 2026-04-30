---
title: Managing order fallout
description: Learn how Fallout Management enables you to identify, investigate, and resolve order issues so that orders can be processed to completion.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Managing order fallout

Learn how Fallout Management enables you to identify, investigate, and resolve order issues so that orders can be processed to completion.

## Overview

Order fallout refers to the failures that occur due to errors and exceptions that may take place during order fulfillment. These exceptions include the following:

-   Incorrect data
-   Connectivity problems
-   Inadequate inventory supply
-   Other unforeseen issues

Some issues could originate in inbound and outbound external systems that integrate with Order Management. A single order task can have multiple types of fallout issues.

The following table provides examples of fallout errors and exceptions that can occur during order processing:

<table id="table_hny_kmr_drb"><thead><tr><th>

Type of failure

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Failures in downstream fulfillment systems

</td><td>

Fulfillment system can't process the request due to incorrect or missing data.

</td></tr><tr><td>

Failure to complete system interaction in a timely manner

</td><td>

Timeouts that occur during system interactions.

</td></tr><tr><td>

Failure in connection

</td><td>

-   Network connectivity issue.
-   Unable to locate or route a request to a target system.

</td></tr><tr><td>

Unavailable inventory

</td><td>

Inventory stock isn't available in the Enterprise Resource Planning \(ERP system\) to fulfill certain items on the order.

</td></tr></tbody>
</table>## Fallout Management functions

With Fallout Management, you can track each order fallout and automatically trigger the actions and interventions that can resolve your order fallout in a timely manner. The following diagram shows the order fallout management flow.

![Infographic displaying the order fallout management flow. For the image description, refer to the text that follows.](../image/order-fallout-management.png "Order Fallout Management flow")

Fallout Management enables you to identify the orders in a failed state. Fallout tasks can be triggered and automatically routed to the appropriate team to investigate, diagnose, and resolve the underlying issue that is stopping order fulfillment. With Fallout Management, you can identify, route, assign, manage, and monitor the entire life cycle of an order fallout.

## Fallout Management tools

The Fallout Management function includes the following tools:

-   **Order fallout tracking**

    With this tool, you can assign a unique number to each order fallout to track the progress of the fallout, from inception through resolution. By using an Order Fallout dashboard, a designated order fallout manager can view the status of all open fallout records. To learn more, see [Review a fallout record](../task/select-order-fallout-records-review.md#).

-   **Fallout resolution**

    With this tool, you can use the ServiceNow AI Platform features such as routing, notifications, and Workflow Studio to process order fulfillment exceptions in an automated manner. To learn more, see [Create automated and manual fallout records](creating-automated-manual-fallout-records.md#).


For example, your customer orders a router, but insufficient inventory quantities are available in your ERP system to reserve the item and fulfill the order.

-   You create a fallout record for tracking and investigative purposes. This record places the customer order line item on hold.
-   An order fulfillment agent can follow up to determine what is causing the shortage. It can be due to the unavailability of the host ERP system or because of an actual stock outage for the ordered item. If it's due to a stock outage, someone can take remedial action to contact the customer, reorder the item, or find a suitable replacement.

After you resolve the issue, you can restore the customer order line item back to a normal state for completion of the order.

Without a fallout management process, your order fulfillment personnel would have to analyze and resolve these fallout issues manually. These additional tasks would result in a longer fulfillment process and could lead to poor customer and employee experiences.

-   **[Creating automated and manual fallout records](creating-automated-manual-fallout-records.md#)**  
With Fallout Management, a provider can create manual or automated fallout records for specific order tasks so that your orders can continue processing through to completion.
-   **[Review a fallout record](../task/select-order-fallout-records-review.md#)**  
Review a fallout record to make sure that the detailed information is correct and complete.

**Parent Topic:**[Using Order Management](reviewing-approving-fulfilling-orders.md)

