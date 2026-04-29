---
title: Configuring Jeopardy Management
description: You can configure Jeopardy Management to monitor tasks in a fulfillment plan and alert managers about the jeopardy levels.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales and Order Management]
---

# Configuring Jeopardy Management

You can configure Jeopardy Management to monitor tasks in a fulfillment plan and alert managers about the jeopardy levels.

There are several steps to set up Jeopardy Management in Order Management as listed in the following table.

<table id="table_wnk_l1d_rxb"><thead><tr><th>

Configuration actions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[../task/define-jm-enabled-fulfillment-flows.md](../task/define-jm-enabled-fulfillment-flows.md)

</td><td>

Define subflows for product and service specifications using the following Jeoapardy-specific Workflow Studio actions:-   Create Order Planned Task
-   All Place Holder Tasks Created for Domain Order
-   Set Task Relationships
-   All Relationships Created for Order Tasks on Domain Order
-   Set Order Task State

 All tasks are created in a Draft state.

</td></tr><tr><td>

[Configure the Order Jeopardy Enablement Policy](../task/enable-jeopardy-management.md)

</td><td>

Enable Jeopardy Management for product and service using the Order Jeopardy Enablement Policy in Decision Builder. **Note:** Enable Jeopardy Management for all fulfillment flows in an order or specification.

</td></tr><tr><td>

[../task/create-sla-definitions.md](../task/create-sla-definitions.md)

</td><td>

Define service level agreements \(SLA\) based on request type and specify the proper start and end conditions to monitor order task progression.

</td></tr><tr><td>

[Configuring Jeopardy Management](configuring-jeopardy-management.md)

</td><td>

Set up decision policy tables to retrieve jeopardy information. Policy tables include:-   Configure Order Task Assignment Policy
-   Configure Order Line Jeopardy Level Calculation Policy
-   Configure Order Task Jeopardy Level Calculation Policy

</td></tr><tr><td>

Set business hours for tasks in Jeopardy Management

</td><td>

Use the **sn\_ind\_tmt\_orm.order\_task\_schedule** system property to set business hours for tasks.

</td></tr></tbody>
</table>## Additional attributes in Jeopardy Management

The following section contains additional information about Jeopardy Management:

-   Is Jeopardy Management domain separated? Yes.
-   How does Jeopardy Management interact with domain separation? Tables are domain separated.
-   Does Jeopardy Management introduce new roles or access control list \(ACL\)? Yes, read access for the Task SLA table \(task\_sla\) is granted to the following roles:
    -   sn\_ind\_tmt\_orm.service\_order\_agent
    -   sn\_ind\_tmt\_orm.order\_fulfilment\_agent

## Demo data

If you have a Telecommunications subscription, the following fulfillment subflows are included with the demo data for Order Management for Telecommunications and Media:

-   Ethernet Edge Device Fulfillment
-   Ethernet Modem Fulfillment
-   Change Ethernet Edge Device
-   Disconnect Ethernet Edge Device
-   Disconnect Ethernet Modem
-   Network Interface Profile Fulfillment
-   Change Network Interface Profile
-   Disconnect Network Interfact Profile
-   EVC Configuration Fulfillment
-   Disconnect EVC Configuration Service

