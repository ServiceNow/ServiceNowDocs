---
title: Work order task states
description: Work orders are made up of at least one work order task. Work order tasks states are sequential and progress from one state to the next.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring work order tasks, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Work order task states

Work orders are made up of at least one work order task. Work order tasks states are sequential and progress from one state to the next.

Depending on your configuration, work order tasks may follow this sequence, a unique sequence, or automatically move from state to state when defined requirements are met.

<table id="table_lvz_jlt_kbc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The qualifier isn't done describing the work and the dispatch group is empty on the work order task.

</td></tr><tr><td>

Pending dispatch

</td><td>

The qualifier adds the dispatch group and selects **Qualified** on the work order task.

</td></tr><tr><td>

Scheduled

</td><td>

The work order task is soft booked but not confirmed. The work order task is pending assignment from the dispatcher.**Note:** This state only shows if use scheduled state is enabled. For more information, see [Configure the Scheduled state](../task/configure-scheduled-state.md).

</td></tr><tr><td>

Assigned

</td><td>

The dispatcher confirms assignment of the work order task. The task is pending acceptance from the assigned Field Service agent.

</td></tr><tr><td>

Accepted

</td><td>

The Field Service agent accepts the task and they're ready to work on it.**Note:** If the Field Service agent selects **Start travel** on the work order task, then the task enters the On route substate.

</td></tr><tr><td>

Work in Progress

</td><td>

The Field Service agent starts work and selects Start work on the work order task.

</td></tr><tr><td>

Closed Complete

</td><td>

The work order task was completed to specification.**Note:** The substate of Closed Complete is Complete.

</td></tr><tr><td>

Closed Incomplete

</td><td>

The task couldn't be completed as specified.**Note:** The substate of Closed Incomplete is Complete.

</td></tr><tr><td>

Cancelled

</td><td>

The task was canceled.

</td></tr></tbody>
</table>