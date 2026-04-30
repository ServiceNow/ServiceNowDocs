---
title: Synchronization of information between Order Management and Field Service Management - Workflow scenario
description: The integration between Order Management and Field Service Management provides support for the end-to-end order fulfillment process. The following scenario shows the seamless synchronization of data, customer information, status, and other updates between Order Management and Field Service Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrating Order Management with FSM, Integrate, Sales Customer Relationship Management]
---

# Synchronization of information between Order Management and Field Service Management - Workflow scenario

The integration between Order Management and Field Service Management provides support for the end-to-end order fulfillment process. The following scenario shows the seamless synchronization of data, customer information, status, and other updates between Order Management and Field Service Management.

## Scenario

After the order fulfillment manager approves the order in Order Management, work orders are automatically created in Field Service Management for conditions that are specified in the decision tree. As the field service agents work on those work orders, the order fulfillment agent can see the updates in the Work Notes section of that Domain Order. An agent cannot close a domain order unless all the work orders associated with it are closed. This workflow shows synchronization of information between Order Management and Field Service Management.

1.  An order fulfillment agent creates a new customer order in the Order Management workspace.
2.  The agent then selects the location for which the order needs to be placed. For multiple locations, multiple order line items are created.
3.  The agent then reviews and places the order.
4.  The order fulfillment manager approves the order. The order line items have domain orders as part of the order fulfillment flow. According to the configurations in the decision table, work orders are automatically created in Field Service Management.
5.  The agent can view the work orders created for the domain orders in the **Details** tab. In the Activity section, the agent tracks all the updates for the work orders in the work notes.
    -   When the status of a work order changes in Field Service Management, the details are displayed in the work notes of the Order Management workspace.
    -   If a work order is canceled, the work order status is displayed in the Order Management work notes section.
    -   In case of inflight changes, the work order is automatically updated. The current status and the updated information are displayed in the work notes section.
6.  The agent can edit an order line item if required. If the agent selects the **PONR** \(Point of No Return\) option, no changes can be made to the order line item in the workflow anymore.
7.  After all the work orders are closed, the order fulfillment manager can review the all the work orders and close the domain order.

    **Note:** The agent cannot close a domain order unless all the work orders associated with that domain order are closed.


