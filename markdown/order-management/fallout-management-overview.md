---
title: Managing order fallout
description: Order fallout occurs when an order encounters an error in its normal fulfillment flow. Learn how Fallout Management enables you to identify, investigate, and resolve order issues so that orders can be processed to completion.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Managing order fallout

Order fallout occurs when an order encounters an error in its normal fulfillment flow. Learn how Fallout Management enables you to identify, investigate, and resolve order issues so that orders can be processed to completion.

## Overview of order fallout

Order fallout refers to the failures that occur due to errors and exceptions that may take place during order fulfillment. Fallout is a task-type object created to support scenarios where an order fails to proceed. These exceptions include the following:

-   Incorrect data
-   Connectivity problems
-   Inadequate inventory supply
-   Other unforeseen issues

Some issues could originate in inbound and outbound external systems that integrate with Order Management. A single order task can have multiple types of fallout issues.

The following table provides examples of fallout errors and exceptions that can occur during order processing.

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
</table>## Order fallout management flow

With Fallout Management, you can track each order fallout and automatically trigger the actions and interventions that can resolve your order fallout in a timely manner. The following diagram shows the order fallout management flow. Fallout Management processes order fallout through the following stages:

1.  Identify and classify order fallout: Detect orders that have encountered errors or exceptions and classify the type of fallout.
2.  Notify and assign order fallout: Route the fallout record to the appropriate team and notify them to begin investigation.
3.  Resolve order fallouts: During runtime execution, fallout can be resolved through one of two paths:
    -   Manual intervention: An agent investigates and resolves the fallout directly.
    -   Automated process followed by manual intervention: An automated process attempts resolution first. If the automated process cannot resolve the fallout, it is escalated for manual intervention.
4.  Verify and close order fallout: Confirm the issue is resolved and close the fallout record so the order can continue to fulfillment.

Fallout Management enables you to identify the orders in a failed state. Fallout tasks can be triggered and automatically routed to the appropriate team to investigate, diagnose, and resolve the underlying issue that is stopping order fulfillment.

## Fallout Management tools

The Fallout Management function includes the following tools:

-   **Order fallout tracking**

    With this tool, you can assign a unique number to each order fallout to track the progress of the fallout, from inception through resolution. By using an Order Fallout dashboard, a designated order fallout manager can view the status of all open fallout records. To learn more, see [Review a fallout record](../task/select-order-fallout-records-review.md#).

-   **Fallout resolution**

    With this tool, you can use the ServiceNow AI Platform features such as routing, notifications, and Workflow Studio to process order fulfillment exceptions in an automated manner. To learn more, see [Creating automated fallout records](creating-automated-manual-fallout-records.md).


For example, your customer orders a router, but insufficient inventory quantities are available in your ERP system to reserve the item and fulfill the order.

-   You create a fallout record for tracking and investigative purposes. This record places the customer order line item on hold.
-   An order fulfillment agent can follow up to determine what is causing the shortage. It can be due to the unavailability of the host ERP system or because of an actual stock outage for the ordered item. If it's due to a stock outage, someone can take remedial action to contact the customer, reorder the item, or find a suitable replacement.

After you resolve the issue, you can restore the customer order line item back to a normal state for completion of the order.

Without a fallout management process, your order fulfillment personnel would have to analyze and resolve these fallout issues manually. These additional tasks would result in a longer fulfillment process and could lead to poor customer and employee experiences.

-   **[Creating automated fallout records](creating-automated-manual-fallout-records.md)**  
With Fallout Management, a provider can create automated fallout records for specific order tasks so that your orders can continue processing through to completion.
-   **[Create a manual fallout record](../task/create-manual-order-fallout-record.md)**  
Create a fallout record manually for an order task that has a condition or issue that prevents it from being completed.
-   **[Review a fallout record](../task/select-order-fallout-records-review.md#)**  
Review a fallout record to make sure that the detailed information is correct and complete.
-   **[Update a fallout record](../task/review-update-selected-order-fallout-records.md)**  
Review the detailed information for a selected fallout record to verify that the information is correct and complete. You can change the fallout type, state, or priority. You can even assign it to a specific person to follow up on.
-   **[Resolve order fallouts](../task/resolve-order-fallouts.md)**  
Learn how to close the order fallout tasks in Order Management so that you can progress with order fulfillment.

**Parent Topic:**[Using Order Management](using-order-management.md)

