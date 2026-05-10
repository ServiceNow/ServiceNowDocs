---
title: Create a similar tasks group
description: Identify similar or duplicate event tasks associated with an event and add them to a similar tasks group by grouping them in the Similar tasks groups tab. It helps you to streamline event task management and reduce duplication of efforts.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating similar tasks groups, Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a similar tasks group

Identify similar or duplicate event tasks associated with an event and add them to a similar tasks group by grouping them in the **Similar tasks groups** tab. It helps you to streamline event task management and reduce duplication of efforts.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

You can create a similar tasks group and add tasks to it only in the **Draft** state of the event.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select the event from the list.

2.  To create a similar event tasks group, use one of these options.

<table id="choicetable_xf2_jyr_shc"><thead><tr><th align="left" id="d234179e93">

Action

</th><th align="left" id="d234179e96">

Description

</th></tr></thead><tbody><tr><td id="d234179e102">

**Choose similar event tasks in the __Event tasks__ tab and select the __Create similar tasks group__ UI action.**

</td><td>

1.  In the Create similar tasks group, add a name for the group and select **Create**.
2.  Verify that the group is created and shows up in the Similar tasks groups list.
![Event tasks tab.](../image/event-tasks-from-event-task-tab.png)

</td></tr><tr><td id="d234179e132">

**Add event tasks from the __Similar tasks groups__ tab.**

</td><td>

Complete these steps: 1.  Select **New** in the **Similar tasks groups** tab and select **Save**.

![Event tasks tab in the group.](../image/event-tasks-from-grp.png)

2.  From the **Event tasks** tab in the group, select **Add**, choose applicable tasks from the tasks list, and select **Add**.
Applicable event tasks are added to the Similar tasks group.**Note:** When you select **Add** in the **Event tasks** tab, the modal displays only applicable event tasks, helping to prevent cyclic dependencies.

</td></tr></tbody>
</table>    To add events tasks with dependencies to the Similar tasks group, a cyclic dependency validation check is performed by the system. An event task and its dependent event task cannot be added to the same similar task group. For example, if you add task 4 into an event task group and task 5 is dependent on task 4, then task 5 cannot be added into the same group as task 4 as shown in the example.

    ![Cyclic check.](../image/event-task-cyclic-check.png)

    When an event starts, the system identifies the first executed event task as the original task. Other similar tasks are marked as duplicate tasks in the group.

    When an event starts, a task with dependencies remains in the **Pending** state until its dependencies are resolved. Once the dependencies, such as EVNTSK0010008 in the example, are closed, the task moves to the **On hold** state.

    **Note:** The **Original task** field in the Similar tasks group is automatically assigned when the event task begins execution and cannot be edited manually at any point.

3.  To remove an event task from the group, select **Unlink** in the Similar tasks group record.

    The event task is removed from the Similar tasks group.

4.  To delete the event task, select **Remove**.

    The event task is deleted from the event.


**Parent Topic:**[Creating similar tasks groups](../concept/identifying-running-dup-tasks-once.md)

