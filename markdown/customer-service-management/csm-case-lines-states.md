---
title: Case line item states
description: A case line item can be in one of several different states as agents work to resolve a case and the associated case line items. The case line items in a case can be in different states as the agent works to resolve each issue.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Case lines and workflows, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case line item states

A case line item can be in one of several different states as agents work to resolve a case and the associated case line items. The case line items in a case can be in different states as the agent works to resolve each issue.

<table id="table_vx3_gcm_fdc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The case line item is in the Draft state.When a case is created and is in the Draft state, the associated case line items are also created in the Draft state.

</td></tr><tr><td>

New

</td><td>

The case line item is in the New state.When a case is submitted and moved to the New state, the associated case line items that are currently in the Draft state are also moved to the New state.

</td></tr><tr><td>

Work in Progress

</td><td>

The assigned agent is working on the case line item.

</td></tr><tr><td>

Awaiting Info

</td><td>

The assigned agent has requested additional information about the case line item and is waiting for a response.

</td></tr><tr><td>

Resolved - Accepted

</td><td>

The change to the case line item has been accepted.

</td></tr><tr><td>

Resolved - Denied

</td><td>

The change to the case line item has been denied.

</td></tr><tr><td>

Canceled

</td><td>

The case line item has been canceled.

</td></tr></tbody>
</table>## Syncing the state of a case with the case line items

The Case lines and workflows application syncs the state of the case line items with the parent case.

<table id="table_ptj_wmk_tcc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

When a case is created for an item with multiple lines, such as an order, new case line items are also created. The case and case line items are created in the Draft state.

</td></tr><tr><td>

New

</td><td>

When a case is submitted, the state is updated from Draft to New. The states of the associated case line items that are currently in the Draft state are also set to New.

</td></tr><tr><td>

Work in Progress

</td><td>

When an agent selects **Assign to me** on a case in the New state, the state is updated from New to Work in Progress. The states of the associated order case line items that are currently in the New state are also set to Work in Progress.If any of the associated case line items are set to Work in Progress, the case is set to Work in Progress.

</td></tr><tr><td>

Resolved

</td><td>

When a case is set to Resolved, the status of each associated case line item is also set to Resolved.If all of the case line items are Resolved, the case is set to Resolved.

</td></tr><tr><td>

Closed

</td><td>

If all of the case line items are in a terminal state, the case can be set to Closed. Terminal states include:

-   Resolved - Accepted
-   Resolved - Denied
-   Canceled

</td></tr><tr><td>

Canceled

</td><td>

When a case in the Draft state is set to canceled, the status of each associated case line item is also set to canceled.**Note:** Agents can only cancel cases in the Draft state.

</td></tr></tbody>
</table>