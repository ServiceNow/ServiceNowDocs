---
title: State changes for event tasks in groups
description: The original and duplicate event tasks in the Similar tasks group move through different states until the original task is closed.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating similar tasks groups, Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# State changes for event tasks in groups

The original and duplicate event tasks in the Similar tasks group move through different states until the original task is closed.

The state transitions of the original and duplicate event tasks are explained in the table.

<table id="table_uvn_s3x_zfc"><thead><tr><th>

Description

</th><th>

Task state

</th></tr></thead><tbody><tr><td>

An event contains similar tasks grouped together.

</td><td>

The event from the list where similar event tasks are grouped together is shown in the example.

![Similar tasks group.](../image/event-started-for-sim-task-grp.png)

</td></tr><tr><td>

State the **Original task** field before starting the event.

</td><td>

Before starting the event, the **Original task** field in the Similar tasks group is empty and in the read-only state.

![Original task empty.](../image/event-task-ori-task-empty.png)

</td></tr><tr><td>

After an event is started, the original task is auto-assigned.

</td><td>

The first task of the event, such as t4 \(EVNTSK0010020\) of group 2 in the example, becomes the original task of the Similar tasks group. The example shows that task 4 \(t4\) does not have any dependency.

![Original task Open.](../image/event-ori-task-open.png)![Original task updated.](../image/event-starts-ori-task-updated.png)

</td></tr><tr><td>

States of original and duplicate tasks

</td><td>

The original task is updated to the **On hold** state and the duplicate task is in the **Pending** state.

![On hold state.](../image/event-sim-task-grp-refreshed.png)For context, the worknote for the original task is updated such that the task has been moved to **On hold** because it was grouped by the similar task groups.

![Worknote.](../image/event-ori-task-worknote-updated.png)

</td></tr><tr><td>

The dependencies in the similar tasks group are closed.

</td><td>

Task 4 is dependent on task 3, task 3 is dependent on task 2, and task 2 is dependent on task 1. Therefore, it is closed first.

![Original task Open.](../image/event-ori-task-open.png)

</td></tr><tr><td>

After closing t1, t2 moves to the **Open** state.

</td><td>

The task, t2, is open.

</td></tr><tr><td>

After closing t2, t3 moves to the **On hold** state.

</td><td>

The task, t3, is on hold.

</td></tr><tr><td>

Since all tasks in the group are On hold, the original task \(t4\) moves to the **Open** state.

</td><td>

The task, t4, is open.

</td></tr><tr><td>

Final step. After closing the original task, the duplicate task moves to the **Closed duplicate** state automatically.

</td><td>

The duplicate task \(t3\) moves to the **Closed duplicate** state automatically.

![Closed duplicate.](../image/event-closed-dup-task.png)

</td></tr></tbody>
</table>You can unlink an event task from the similar tasks group by selecting the **Unlink similar tasks group** UI action in the event task.

You can re-trigger an original task as a manual task and complete its workflow like a regular event task by selecting the **Re-trigger as a manual task** UI action in the event task. It moves the original task to the **Open** state, but its duplicate task stays in the **Closed duplicate** state.

**Parent Topic:**[Creating similar tasks groups](identifying-running-dup-tasks-once.md)

