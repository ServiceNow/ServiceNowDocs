---
title: Create an order case
description: Create an order case for a customer order or for selected order lines.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-10-30"
reading_time_minutes: 2
breadcrumb: [Creating an order case, Order Operations Case Management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create an order case

Create an order case for a customer order or for selected order lines.

## Before you begin

Role required: sn\_order\_case.creator, sn\_order\_case.agent, sn\_customerservice\_agent, admin

## Procedure

1.  In CSM Configurable Workspace, create an order case in one of the following ways.

    -   Select **Create case** from a customer order.
    -   Select **Create case** from the Order Line Items list on a customer order. \(This UI action is enabled if one or more order lines are selected.\)
    -   Select **Create case** from an interaction record.
    -   Select **New** from the Order Cases list view.
2.  Select an order-related service from the case type selector modal and then select **Create case**.

    This modal displays the services that are available for order cases, such as Sales Order Change Request or Sales Order Dispute.

3.  Fill in the following details on the Create New Order Case intake form.

    -   **Account**: the account for the order.
    -   **Scope of request**: the agent can create a case for order lines from a single order or for multiple complete orders.
    -   **Order number**: the order number associated with the order case.
    -   **Short description**: a brief description of the order case.
    Depending on where you create the order case from, some of these fields are auto filled with information from the customer order or interaction records.

    **Note:** Default values that have been configured for a service definition record can auto populate fields on the order case record. If the **Account**, **Contact**, or **Contract** field values are also defined in the selected service definition record, those values take priority over the values from the customer order record.

4.  Select **Save**.

    Saving the Create New Order Case intake form creates the order case record in Draft state.

5.  View the order case record details and the order case line items and make any necessary changes.

    You can perform the following tasks while the order case is in Draft state:

    -   Add orders or order lines to the order case.
    -   Delete orders or order lines from the order case.
    -   Create new order case line items.
    -   Edit the details of order case line items.
    -   Assign order case line items to yourself.
6.  Select **Submit**.

    Submitting the order case record moves the order case and the order case line items currently in the Draft state to the New state and enables you to begin working to resolve the order case.


## What to do next

After submitting an order case, you can:

-   [Add or delete orders or order lines to an order case](csm-order-ops-create-order-case.md)
-   [Create new order case lines for an order case](csm-order-ops-order-case-add-lines.md)
-   [Edit the information in order case line records](csm-order-ops-order-case-edit-lines.md)
-   [Create tasks for order case lines and assign them to other users](csm-order-ops-order-case-create-task.md)

