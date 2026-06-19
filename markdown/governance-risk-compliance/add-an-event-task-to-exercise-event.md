---
title: Monitor event tasks and create ad-hoc tasks
description: Monitor event task completion and create ad-hoc tasks as necessary in the exercise from the BCM Configurable Workspace. The tasks are then completed in a sequence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-an-event-task-to-exercise-event.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
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

For more information on editing of tasks, see [Structured workflows for Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md) and [Structured workflows for Crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select the exercise event.

2.  Select the **Event tasks** tab.

    **Note:** The **Event tasks** tab is displayed for the exercise events when the exercise method is **Functional**.

    When you add or update the plan to the exercise event, the related plans, assets, and tasks that are associated with the plan also get pulled into the event as shown in the example.\[Omitted image "event-tasks-w-phases.png"\] Alt text: Event tasks with phases.

    You can update the phase of the event task from the list view. You can also create an ad-hoc task and then associate a phase with that event task.

    You can edit the phase for an event task until it reaches the **Closed** state. Once the task is marked as **Closed complete**, **Closed failed**, or **Closed incomplete**, the phase field becomes read-only. This change verifies that phases remain editable during active task management but are locked once the task is finalized.

3.  To add event tasks in bulk from a task template group, on the **Event tasks** tab select **More Actions** &gt; **Add groups**.

    The **Select task template groups** dialog opens as a two-step wizard. In step 1, select one or more groups. In step 2, select the activated plan that the new event tasks should be associated with. Step 2 is skipped when you invoke **Add groups** from the **Event tasks** tab of an activated plan, because the activated plan is already known.

    The dialog filters groups by **Active** = true. Filters that are currently applied to the **Event tasks** list — for example, **Phase** = **Recovery validation** — are applied as default values on the created tasks. Phase values that are already set on a task template take precedence over the list filter.

    \[Omitted image "event-task-more-actions-menu.png"\] Alt text: Exercise event Event tasks tab More Actions menu showing Add groups, Add tasks, Export to Excel, and New ad-hoc task.

    \[Omitted image "exercise-event-select-task-template-groups-step-one.png"\] Alt text: Select task template groups wizard with step 1 active and step 2 upcoming.

    \[Omitted image "activated-plan-event-tasks-grouped.png"\] Alt text: Event tasks tab grouped by activated plan.

4.  To add individual task templates without a group, on the **Event tasks** tab select **More Actions** &gt; **Add tasks**.

    The **Select task templates** dialog uses the same two-step wizard and the same filter rules as **Add groups**.

    \[Omitted image "select-task-templates-dialog.png"\] Alt text: Select task templates dialog listing recovery task templates with Active status.

5.  After the bulk add completes, wait for the auto-refresh banner to dismiss, or select **Refresh** to refresh the **Event tasks** list manually.

    The **Event tasks** list does not auto-refresh row by row. Instead, the banner **The event tasks are updated. Select Refresh to see updated data. List will auto-refresh once all tasks are created.** is displayed while the system creates the tasks. About ten seconds after the last task is created, the list refreshes once. This avoids repeated refreshes on event tasks lists that contain a large number of rows. For more information, see [Event task creation progress in exercise and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-event-task-template-progress.md).

    \[Omitted image "event-tasks-auto-refresh-banner.png"\] Alt text: Yellow banner stating the event tasks are updated with a Refresh button.

    \[Omitted image "activated-plan-event-task-list.png"\] Alt text: Activated plan Event tasks tab showing tasks created from a task template group.

6.  To save a set of event tasks as a reusable task template group, select the tasks in the **Event tasks** list and then select **Save as group** &gt; **Save tasks**.

    To append them to an existing group, you can select **Save as group** &gt; **Add to group**. Event tasks are saved as task templates that can later be applied from an exercise event, a crisis event, an activated plan, a plan, a loss scenario, or a recovery strategy. The element definition associated with each event task is preserved on the resulting templates so element-definition filtering still applies when the group is reused.

    \[Omitted image "save-as-group-create-dialog.png"\] Alt text: Create task template group modal showing You selected 2 task\(s\) and the Group name field.

7.  To add an ad-hoc task to the event, select **New ad-hoc task**.

    **Note:** When you add an ad-hoc task to the exercise event that is in the **Work in progress** state and if the activated plan is in the **Work in progress** state, the tasks get moved to the **Open** state. If the activated plan is the **Pending** state, the task moves to the **Pending** state.

    For more information on the fields in the New Event Task form, see [Create Event Task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-event-task-form-uib-ws.md).

    **Note:** You cannot create an ad-hoc task for the activated plans that are in **Closed Complete** or **Closed Incomplete** state.

    The **Create New Event task** form is displayed.

    \[Omitted image "create-new-event-task.png"\] Alt text: Create New Event task form.

8.  To exclude specific tasks from time calculation, select the **Do not include in time calculation** option.

    The actual time taken is then calculated based on the minimum start time and maximum end time of included tasks, while the total effort is the sum of the effort for each task, excluding those with the check box checked.

9.  Enter the Planned start date in the event and select **Save**.

    When you enter the Planned start date in the exercises and events, the Planned start date and the Planned end date on the activated plan and on the event tasks are calculated based upon the **Planned duration** field.

    **Note:** If you have more than 500 tasks for an event or exercise, the planned times are not calculated automatically. A UI action named **Refresh tasks data** is shown. Select the UI action to refresh the Planned start date, Planned end date, and Order.

    \[Omitted image "refresh-tasks-data-in-events.png"\] Alt text: Refresh tasks data.

10. To indicate the achieved recovery level of the impacted asset of the task, update **Asset recovery level**.

    Previously, the assets were automatically marked as Recovered only when all plan tasks were completed, even those assets in later phases such as Return to Normal or Post-Incident Review. This approach delayed visibility into operational readiness. For example, an asset could be functionally available during the Recovery phase, but the system wouldn’t reflect the status until all tasks were done.

    Starting with BCM release 9.x.x and later, the asset recovery status has been enhanced to provide granular tracking. Completing specific tasks now automatically updates the corresponding event asset state.

    It is not mandatory that a flow may progress through the **Not Recovered** → **Partially Recovered** → **Recovered** states. If the related tasks are completed, an asset can be recovered directly. It is also not mandatory to add the **Partially Recovered** state; you can specify the recovery level of an asset directly based on task completion.

    The Asset recovery level column in the event task list view also features color coding, providing visual indicators for different recovery progress levels. Specifically, **Partially Recovered** is represented by an info color, and **Recovered** is represented by a success color, making it easier to track recovery status.

    \[Omitted image "event-task-list-view-color.png"\] Alt text: Event task list view.

    If you open the Hierarchical view \(Gantt chart\), it shows the background colors for the partial recovery and recovery levels.

    \[Omitted image "event-task-hier-gantt-view-color.png"\] Alt text: Hierarchical view.\[Omitted image "asset-reco-level-column-event-task.png"\] Alt text: Asset Recovery Level column in event task.

    Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables recovery coordinators to identify when dependent assets can safely start their recovery process.

11. To display actual execution dates alongside planned dates, select **Show actual dates** in the toolbar.

    When enabled, the **Actual start** and **Actual end** columns display the real dates recorded as tasks are progressed through state transitions. This view is useful for comparing planned vs. actual execution timing during an exercise review.

    Event tasks toolbar shows the Show actual dates, Export to Excel, Full page, and Gantt controls with the Actual start column visible in the task list.

12. Select **Save**.

    The event tasks are displayed in the **Event tasks** tab.


-   **[Create Event Task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-event-task-form-uib-ws.md)**  
Use the Create New Event Task form in BCM UIB Workspace to add details about an event task.

**Parent Topic:**[Structured workflows for Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md)

