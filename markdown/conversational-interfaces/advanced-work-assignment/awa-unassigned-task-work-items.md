---
title: Check unassigned task work items
description: View a list of unassigned task work items in Advanced Work Assignment, such as cases and incidents, that are currently waiting in the queue and are not assigned to any agents. You can use this list to debug, implement advanced work assignments, or determine why certain work items are unassigned.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Check unassigned task work items

View a list of unassigned task work items in Advanced Work Assignment, such as cases and incidents, that are currently waiting in the queue and are not assigned to any agents. You can use this list to debug, implement advanced work assignments, or determine why certain work items are unassigned.

## Before you begin

Role required: awa\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Management** &gt; **Unassigned Task Work Items**.

    -   To create a task, click **New**.
    -   To modify an existing task, select the task to be updated.
2.  On the form, fill in the fields.

<table id="table_an4_hkf_mjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Whether the task is still being worked on or is complete.

</td></tr><tr><td>

Display Name

</td><td>

Task name.

</td></tr><tr><td>

Offered on

</td><td>

Date that the task was first offered to an agent.

</td></tr><tr><td>

State

</td><td>

List that shows the status of the task:

-   Accepted
-   Cancelled
-   Pending Accept
-   Queued


</td></tr><tr><td>

Assignment rule

</td><td>

Rule that assigns cases that meet the matching rule criteria to a customer service agent.

</td></tr><tr><td>

Exceeded Queue Target Wait Time

</td><td>

Task that has waited longer than the target wait time of the queue.

</td></tr><tr><td>

Rejected

</td><td>

Task that was rejected by the agent.

</td></tr><tr><td>

Timed Out

</td><td>

Task that has exceeded the timeout specified in the assignment rule.

</td></tr><tr><td>

Assigned to

</td><td>

User that is assigned to the task.

</td></tr><tr><td>

Document ID

</td><td>

Document ID that is assigned to the task.

</td></tr><tr><td>

Previous Work Item

</td><td>

Reference to a previous work item for the same Document ID.

</td></tr><tr><td>

State changed on

</td><td>

Date that the task state was most recently changed.

</td></tr><tr><td>

Cancelled reason

</td><td>

Reason that the task was canceled:

-   Disqualified from service channel
-   Manually assigned
-   Time out
-   Transfer was cancelled or rejected


</td></tr><tr><td>

Is Dismissed

</td><td>

Whether the task has been dismissed.

</td></tr><tr><td>

Work Item Size

</td><td>

Amount of an agent's capacity that is used if this task is assigned.

</td></tr><tr><td>

Wait time

</td><td>

Length of time the task has waited in the queue before being assigned.

</td></tr><tr><td>

Assignment group

</td><td>

Group that is assigned to the task.

</td></tr><tr><td>

Document table

</td><td>

Document table that is assigned to the task.

</td></tr><tr><td>

Queue

</td><td>

Queue that is assigned to the task.

</td></tr></tbody>
</table>3.  Click **Submit** to create the task or **Update** to modify the task.


**Parent Topic:**[Using Advanced Work Assignment](../concept/using-awa.md)

