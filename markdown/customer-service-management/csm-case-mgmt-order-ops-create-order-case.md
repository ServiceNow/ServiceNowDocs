---
title: Creating an order case
description: Agents can create order cases from a customer order, from an interaction record, or from the Order Cases list view in CSM Configurable Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Order Operations Case Management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Creating an order case

Agents can create order cases from a customer order, from an interaction record, or from the Order Cases list view in CSM Configurable Workspace.

Agents can create order cases in the following ways:

-   Selecting **Create case** from a customer order.
-   Selecting **Create case** from the Order Line Items list on a customer order. \(This action is enabled if one or more order lines are selected.\)
-   Selecting **Create case** from an interaction record.
-   Selecting **New** from the Order Cases list view.

After initiating an order case, the agent can select an order-related service from the case type selector modal. This modal displays the services that are available for order cases, such as Sales Order Change Request or Sales Order Dispute.

Selecting **Create case** from the case type selector modal displays the Create New Order Case intake form where the agent can enter the following order case details:

-   **Account**: the account for the order.
-   **Scope of request**: the agent can create a case for order lines from a single order or for multiple complete orders.
-   **Order number**: the order number associated with the order case.
-   **Short description**: a brief description of the order case.

**Note:** Depending on where the agent creates the order case from, some of these fields are auto filled.

Selecting **Save** on the intake form displays the Order case record page. From this record, agents can:

-   Add order lines to the order case.
-   Delete order lines from the order case.
-   Create new order case line items.
-   Edit the details of order case line items.
-   Assign order case line items to themselves.

Selecting **Submit** on the Order case record moves the order case and the order case line items currently in the Draft state to the New state. Once in the New state, agents can begin working to resolve the order case. This can include creating tasks for order case line items and assigning them to team members.

## Scope of request

An agent can create the following types of order cases:

-   Cases that reference one or more order lines from a single customer order.
-   Cases that reference multiple complete customer orders.

The Order case record includes the **Scope of request** field. Depending on where the agent initiates the creation of an order case, this field is auto-filled with one of the following values:

-   **Specific line items, Single order**: The system creates an order case and converts the selected order lines from the customer order to case line items on that order case.
-   **Multiple orders**: The system creates an order case and converts the order header from each customer order to a case line item on that order case.

For example, if an agent creates an order case by selecting **Create case** on a customer order, the scope of request is **Multiple orders**. If an agent selects one or more order lines and then selects **Create case** from the Order Line Items list on a customer order, the scope of request is **Specific line items, Single order**.

## Add orders and order line items to an order case

Order cases include a list of order case line items. Depending on how the order case is created, these case line items represent either customer orders or order lines from a single order.

Once an order case has been created, agents can add additional orders or order lines to that case by selecting **Add** on the Order Case Line action bar. Selecting this action displays a modal that shows information based on the values in the **Origin table** field and **Order number** field on the case record.

-   If the **Origin table** is set to Customer Order and the **Order number** field is empty, the case type selector modal shows a list of orders associated with the account selected in the **Account** field. The case type selector modal displays "Add orders to case".
-   If the **Origin table** is set to Customer Order and the **Order number** field includes an order, the case type selector modal shows a list of order lines associated with that order. The case type selector modal header is "Add order lines to case".

The agent can select a line item from the modal and then select **Add** to add it to the order case as an order case line item.

