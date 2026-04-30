---
title: Invoice case and invoice case line states
description: Invoice cases and invoice case lines move through several different states as agents work to resolve the individual case lines in invoice cases.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Case Management for Invoice Operations, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Invoice case and invoice case line states

Invoice cases and invoice case lines move through several different states as agents work to resolve the individual case lines in invoice cases.

## Invoice case states

Invoice cases can be in the states listed in the following table. Actions available on the invoice case record enable agents to move cases from one state to another.

<table id="table_owz_fk3_lcc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The invoice case is in the Draft state.Select **Submit Case** on the invoice case record page to move the invoice case and all of the invoice case lines that are currently in the Draft state to New.

</td></tr><tr><td>

New

</td><td>

The invoice case has been submitted and is in the New state.Select **Assign to me** on the record page to assign the case to the logged-in user and move the invoice case and all of the invoice case lines currently in the New state to Work in Progress.

</td></tr><tr><td>

Work in Progress

</td><td>

The assigned agent is working on the invoice case.Select the following actions:

-   **Request Information**: Use this action to request additional information from the contact or consumer. The state moves to Awaiting Information.
-   **Propose solution**: Use this action to propose a resolution to the contact or consumer. The state moves from Work in Progress to Resolved.

</td></tr><tr><td>

Awaiting Info

</td><td>

The agent is waiting for the contact to provide the requested information for the invoice case.Select **Information Received** to move the invoice case back to Work in Progress.

</td></tr><tr><td>

Resolved

</td><td>

The agent has proposed a resolution for the invoice case to the contact.Select **Close Case** on the record page to move the invoice case to Closed.

</td></tr><tr><td>

Closed

</td><td>

The invoice case has been resolved and the resolution has been accepted by the contact.When all of the case lines for an invoice case are in a Final state, the case can be set to Closed. Final states include:

-   Resolved - Accepted
-   Resolved - Denied
-   Canceled

</td></tr><tr><td>

Canceled

</td><td>

The invoice case has been canceled.Select **Cancel** to cancel an invoice case.

**Note:** You can only cancel invoice cases in the Draft state.

</td></tr></tbody>
</table>## Invoice case line states

Invoice case lines can be in the states listed in the following table. The case lines in an invoice case can be in different states as the agent works to resolve each issue.

<table id="table_vx3_gcm_fdc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The invoice case line is in the Draft state.When an invoice case is created and is in the Draft state, the associated invoice case lines are also in the Draft state.

</td></tr><tr><td>

New

</td><td>

The invoice case line is in the New state.When an invoice case is submitted and moved to the New state, the associated invoice case lines that are currently in Draft state are also moved to the New state.

</td></tr><tr><td>

Work in Progress

</td><td>

The assigned agent is working on the invoice case line.

</td></tr><tr><td>

Awaiting Info

</td><td>

The assigned agent has requested additional information about the invoice case line and is waiting for a response.

</td></tr><tr><td>

Resolved - Accepted

</td><td>

The change to the invoice case line has been accepted.

</td></tr><tr><td>

Resolved - Denied

</td><td>

The change to the invoice case line has been denied.

</td></tr><tr><td>

Canceled

</td><td>

The invoice case line has been canceled.

</td></tr></tbody>
</table>**Note:** An agent can manually change the state of each invoice case line to Resolved - Accepted, Resolved - Denied, or Canceled. When all of the invoice case lines are in one of these states, the state of the invoice case changes to Resolved.

## Syncing the state of an invoice case with the invoice case lines

State changes for an invoice case can result in state changes for the associated invoice case lines. These changes are detailed in the following table.

<table id="table_ptj_wmk_tcc"><thead><tr><th>

Invoice case state

</th><th>

Invoice case line state

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Saving a new invoice case creates the case in the Draft state. Invoice case lines for the invoice case are also created in the Draft state.

</td></tr><tr><td>

New

</td><td>

When an agent submits an invoice case, the state is updated from Draft to New. The states of the associated invoice case lines that are currently in Draft state are also set to New.

</td></tr><tr><td>

Work in Progress

</td><td>

When an agent selects **Assign to me** on an invoice case in the New state, the state is updated from New to Work in Progress. The states of the associated invoice case lines are also set to Work in Progress.If any of the case lines are set to Work in Progress, then the case is also set to Work in Progress.

</td></tr><tr><td>

Resolved

</td><td>

If a case is set to Resolved, the status of each of the case lines is also set to Resolved.If all of the case lines are Resolved, then the case is set to Resolved.

</td></tr><tr><td>

Closed

</td><td>

When all of the case lines for an invoice case are in a final state, the case can be set to Closed. Final states include:-   Resolved - Accepted
-   Resolved - Denied
-   Canceled

When an agent selects **Close Case** on an invoice case in the Solution Proposed state, the system updates the state to Closed.

</td></tr><tr><td>

Canceled

</td><td>

When a user selects **Cancel** on an invoice case in the Draft state, the system updates the state to canceled. States for the invoice case lines associated with the invoice case are also set to canceled.**Note:** You can only cancel invoice cases in the Draft state.

</td></tr></tbody>
</table>