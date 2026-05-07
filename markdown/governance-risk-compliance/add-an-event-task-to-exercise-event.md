---
title: Monitor event tasks and create ad-hoc tasks
description: Monitor event task completion and create ad-hoc tasks as necessary in the exercise from the BCM Configurable Workspace. The tasks are then completed in a sequence.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Monitor event tasks and create ad-hoc tasks

Monitor event task completion and create ad-hoc tasks as necessary in the exercise from the BCM Configurable Workspace. The tasks are then completed in a sequence.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

Starting with version 6.1.x of the Business Continuity Management application, these enhancements are supported for managing the tasks.

-   Perform edits and change the state of tasks, making the process more efficient.
-   Reduce the time spent on managing the tasks individually.
-   Improve efficiency for the users who perform the exercises or events offline in tools such as Microsoft Excel. This enhancement helps streamline the transition from offline to online task management.
-   Edit the **State** field of the event task if you have the BCM manager role, BCM planner role, or if you are the user assigned to the event.
-   The **Retrigger as manual** UI action is used only for the automated tasks.

When the plan gets activated as part of an exercise or an actual event, the automated flow gets triggered.

The edit enhancement offers flexibility for managing the event tasks. The BCM manager, BCM planner, or user assigned to the event can manage the tasks efficiently by performing these tasks:

-   Edit several fields such as the **Assignment** field.
-   Edit multiple recovery tasks in the **Task status**, **Actual start**, **Actual end**, **Assigned to**, **Assigned group**, and **Additional assignee** fields in the recovery tasks list at one go.
-   Open a closed task for editing that was closed by mistake. For this scenario, the **Closed failed** task state is added to the tasks. Moving a task to the **Closed failed** state brings an entire exercise to a stop unless the program manager \(sn\_bcm.program\_manager\) unblocks the task and moves it to the **Closed complete** state.

For more information on editing of tasks, see [Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md) and [Structured workflows for crisis events](../concept/perform-tasks-to-manage-crisis-events.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select the exercise event.

2.  Select the **Event tasks** tab.

    **Note:** The **Event tasks** tab is displayed for the exercise events when the exercise method is **Functional**.

    When you add or update the plan to the exercise event, the related plans, assets, and tasks that are associated with the plan also get pulled into the event as shown in the example.![Event tasks with phases.](../image/event-tasks-w-phases.png)

    You can update the phase of the event task from the list view. You can also create an ad-hoc task and then associate a phase with that event task.

    You can edit the phase for an event task until it reaches the **Closed** state. Once the task is marked as **Closed complete**, **Closed failed**, or **Closed incomplete**, the phase field becomes read-only. This change verifies that phases remain editable during active task management but are locked once the task is finalized.

3.  To add an ad-hoc task to the event, select **New ad-hoc task**.

    **Note:** When you add an ad-hoc task to the exercise event that is in the **Work in progress** state and if the activated plan is in the **Work in progress** state, the tasks get moved to the **Open** state. If the activated plan is the **Pending** state, the task moves to the **Pending** state.

    For more information on the fields in the New Event Task form, see [Create New Event Task form](../reference/create-new-event-task-form-uib-ws.md).

    **Note:** You cannot create an ad-hoc task for the activated plans that are in **Closed Complete** or **Closed Incomplete** state.

    The **Create New Event task** form is displayed.

    ![Create New Event task form.](../image/create-new-event-task.png)

4.  To exclude specific tasks from time calculation, select the **Do not include in time calculation** option.

    The actual time taken is then calculated based on the minimum start time and maximum end time of included tasks, while the total effort is the sum of the effort for each task, excluding those with the check box checked.

5.  Enter the Planned start date in the event and select **Save**.

    When you enter the Planned start date in the exercises and events, the Planned start date and the Planned end date on the activated plan and on the event tasks are calculated based upon the **Planned duration** field.

    **Note:** If you have more than 500 tasks for an event or exercise, the planned times are not calculated automatically. A UI action named **Refresh tasks data** is shown. Select the UI action to refresh the Planned start date, Planned end date, and Order.

    ![Refresh tasks data.](../image/refresh-tasks-data-in-events.png)

6.  To indicate the achieved recovery level of the impacted asset of the task, update **Asset recovery level**.

    Previously, the assets were automatically marked as Recovered only when all plan tasks were completed, even those assets in later phases such as Return to Normal or Post-Incident Review. This approach delayed visibility into operational readiness. For example, an asset could be functionally available during the Recovery phase, but the system wouldn’t reflect the status until all tasks were done.

    Starting with BCM release 9.x.x and later, the asset recovery status has been enhanced to provide granular tracking. Completing specific tasks now automatically updates the corresponding event asset state.

    It is not mandatory that a flow may progress through the **Not Recovered** → **Partially Recovered** → **Recovered** states. If the related tasks are completed, an asset can be recovered directly. It is also not mandatory to add the **Partially Recovered** state; you can specify the recovery level of an asset directly based on task completion

    The Asset recovery level column in the event task list view also features color coding, providing visual indicators for different recovery progress levels. Specifically, **Partially Recovered** is represented by an info color, and **Recovered** is represented by a success color, making it easier to track recovery status.

    ![Event task list view.](../image/event-task-list-view-color.png)

    If you open the Hierarchical view \(Gantt chart\), it shows the background colors for the partial recovery and recovery levels.

    ![Hierarchical view.](../image/event-task-hier-gantt-view-color.png)![Asset Recovery Level column in event task.](../image/asset-reco-level-column-event-task.png)

    Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables recovery coordinators to identify when dependent assets can safely start their recovery process.

7.  Select **Save**.

    The event tasks are displayed in the **Event tasks** tab.


-   **[Create New Event Task form](../reference/create-new-event-task-form-uib-ws.md)**  
Use the Create New Event Task form in BCM UIB Workspace to add details about an event task.

**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

