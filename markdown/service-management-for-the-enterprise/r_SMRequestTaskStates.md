---
title: Request task states
description: Like requests, the associated request tasks follow a specific life cycle and move through a series of states, which are displayed in the State field on the task record.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring request task management, Request Management in a Service Management application, Service Management]
---

# Request task states

Like requests, the associated request tasks follow a specific life cycle and move through a series of states, which are displayed in the **State** field on the task record.

The request task states displayed depend on the SM application, as indicated in the table.

**Note:** The **State** field on the request task record is always read-only.

<table id="table_ohw_z45_1r"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Qualifier is not done describing the work.

</td></tr><tr><td>

Pending

</td><td>

Request task is ready to be assigned. Depending on the SM application, this state label may be expanded, for example, **Pending Dispatch** or **Pending Change**.

 The parent request state can change to **Qualified**, for example, if all associated tasks are in **Pending Dispatch** or a later state.

</td></tr><tr><td>

Assigned

</td><td>

Request task is pending acceptance from the assigned agent.

</td></tr><tr><td>

Accepted

</td><td>

Agent accepts the request task and is ready to be done.

</td></tr><tr><td>

Work In Progress

</td><td>

Work on the request task has started. The parent request state changes to **Work In Progress** if no associated tasks are in **Draft** state.

</td></tr><tr><td>

Closed Complete

</td><td>

Request task was completed to specification.

</td></tr><tr><td>

Closed Incomplete

</td><td>

Request task could not be completed as specified.

</td></tr><tr><td>

Canceled

</td><td>

Request task was canceled.

</td></tr></tbody>
</table>In addition to the **State** field, the different request task states are also shown visually at the top of each task record with the process flow formatter.

**Note:** If the **State flows are enabled** option in the configuration screen is not selected, the process flow formatter is removed.

**Parent Topic:**[Configuring request task management](../concept/c_RequestTasksMgmt.md)

