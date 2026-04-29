---
title: Order case and order case line item states
description: Order cases and order case line items move through several different states as agents work to resolve the individual case lines in order cases.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Order Operations Case Management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Order case and order case line item states

Order cases and order case line items move through several different states as agents work to resolve the individual case lines in order cases.

## Order case states

Order cases can be in the states listed in the following table. Actions available on the order case record enable agents to move cases from one state to another.

<table id="table_owz_fk3_lcc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The order case is in the Draft state.Select **Submit** on the order case record page to move the order case and all of the order case line items that are currently in the Draft state to New.

</td></tr><tr><td>

New

</td><td>

The order case has been submitted and is in the New state.Select **Assign to me** on the record page to assign the case to the logged-in user and move the order case and all of the order case line items currently in the New state to Work in Progress.

</td></tr><tr><td>

Work in Progress

</td><td>

The assigned agent is working on the order case.Select the following actions:

-   **Request Information**: use this action to request additional information from the contact or consumer. The state moves to Awaiting Information.
-   **Resolve Case**: use this action to propose a resolution to the contact or consumer. The state moves from Work in Progress to Resolved.

</td></tr><tr><td>

Awaiting Info

</td><td>

The agent is waiting for the contact to provide the requested information for the order case.Select **Information Received** to move the order case back to Work in Progress.

</td></tr><tr><td>

Resolved

</td><td>

The agent has proposed a resolution for the order case to the contact.Select **Close Case** on the record page to move the order case to Closed.

</td></tr><tr><td>

Closed

</td><td>

The order case has been resolved and the resolution has been accepted by the contact.When all of the case line items for an order case are in a terminal state, the case can be set to Closed. Terminal states include:

-   Resolved - Accepted
-   Resolved - Denied
-   Cancelled

</td></tr><tr><td>

Canceled

</td><td>

The order case has been canceled.Select **Cancel** to cancel an order case.

**Note:** You can only cancel order cases in the Draft state.

</td></tr></tbody>
</table>## Order case line item states

Order case line items can be in the states listed in the following table. The case line items in an order case can be in different states as the agent works to resolve each issue.

<table id="table_vx3_gcm_fdc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The order case line item is in the Draft state.When an order case is created and is in the Draft state, the associated order case line items are also in the Draft state.

</td></tr><tr><td>

New

</td><td>

The order case line item is in the New state.When an order case is submitted and moved to the New state, the associated order case line items that are currently in Draft state are also moved to the New state.

</td></tr><tr><td>

Work in Progress

</td><td>

The assigned agent is working on the order case line item.

</td></tr><tr><td>

Awaiting Info

</td><td>

The assigned agent has requested additional information about the order case line item and is waiting for a response.

</td></tr><tr><td>

Resolved - Accepted

</td><td>

The change to the order case line item has been accepted.

</td></tr><tr><td>

Resolved - Denied

</td><td>

The change to the order case line item has been denied.

</td></tr><tr><td>

Cancelled

</td><td>

The order case line item has been cancelled.

</td></tr></tbody>
</table>## Syncing the state of an order case with the order case line items

State changes for an order case can result in state changes for the associated order case line items. These changes are detailed in the following table.

<table id="table_ptj_wmk_tcc"><thead><tr><th>

Order case state

</th><th>

Order case line item tate

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Saving a new order case creates the case in the Draft state. Order case line items for the order case are also created in the Draft state.

</td></tr><tr><td>

New

</td><td>

When an agent submits an order case, the state is updated from Draft to New. The states of the associated order case line items that are currently in Draft state are also set to New.

</td></tr><tr><td>

Work in Progress

</td><td>

When an agent selects **Assign to me** on an order case in the New state, the state is updated from New to Work in Progress. The states of the associated order case line items are also set to Work in Progress.If any of the case line items are set to Work in Progress, then the case is also set to Work in Progress.

</td></tr><tr><td>

Resolved

</td><td>

If a case is set to Resolved, the status of each of the case line items is also set to Resolved.If all of the case line items are Resolved, then the case is set to Resolved.

</td></tr><tr><td>

Closed

</td><td>

When all of the case line items for an order case are in a terminal state, the case can be set to Closed. Terminal states include:-   Resolved - Accepted
-   Resolved - Denied
-   Cancelled

When an agent selects **Close Case** on an order case in the Solution Proposed state, the system updates the state to Closed.

</td></tr><tr><td>

Cancelled

</td><td>

When a user selects **Cancel** on an order case in the Draft state, the system updates the state to Cancelled. States for the order case line items associated with the order case are also set to Cancelled.**Note:** You can only cancel order cases in the Draft state.

</td></tr></tbody>
</table>