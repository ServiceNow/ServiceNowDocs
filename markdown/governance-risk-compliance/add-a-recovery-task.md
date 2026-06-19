---
title: Add recovery tasks
description: Add a recovery task as part of the planned recovery strategy. You can add one or more recovery tasks for a loss scenario and those recovery tasks are displayed in the loss scenario itself. Automate the recovery tasks in a plan for a faster recovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-a-recovery-task.html
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 10
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add recovery tasks

Add a recovery task as part of the planned recovery strategy. You can add one or more recovery tasks for a loss scenario and those recovery tasks are displayed in the loss scenario itself. Automate the recovery tasks in a plan for a faster recovery.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Beginning with the Xanadu release, cyclic dependencies in recovery tasks can be avoided to prevent repeated invocation of the same plan from other plans.

\[Omitted image "plan-record-tabs.png"\] Alt text: Plan record tabs.

For example, in the Recovery task of Cyclic plan example 1 invokes Cyclic plan example 2, Cyclic plan example 2 invokes Cyclic plan example 3 and then again Cyclic plan example 3 invokes Cyclic plan example 1. If you attempt to add a link between Cyclic plan example 2 and Cyclic plan example 3, it isn’t allowed. An error message, similar to the one shown in the example, prompts you to choose a different related plan to help prevent such issues from occurring in an event.

\[Omitted image "cyclic-plan-error-message.png"\] Alt text: Cyclic plan error message.

Similarly, if plans are activated beyond 10 levels or hierarchical links involving more than 10 levels of plans are created, an error message is displayed, suggesting the removal of the plan before saving the record.

\[Omitted image "cyclic-plan-levels.png"\] Alt text: Plan levels.

Starting from version 6.1.x of the Business Continuity Management application, the integration of recovery task automation into the business continuity planning process is introduced. This automation aims to enhance efficiency, save time, and minimize the risk of human errors. Users who have the necessary access to the recovery task can classify it as either manual or automated. These tasks are organized in a sequential manner with dependencies.

To automate a recovery task, administrators or application developers create an automation flow and associate it with the task. When the task moves to the **Open** state \(when the plan is activated as part of an exercise or an actual event\), the automated flow is triggered. However, there may be instances where the automated flow fails due to system errors. In such cases, the user with access to the recovery task can activate the manual task as a backup and assign it to a designated backup assignee. The backup assignee receives a system-generated email to complete the task flow. Plan users have the opportunity to practice business continuity plan exercises and make improvements based on the results obtained.

Tasks can also be added in bulk by applying a task template group using the **Add groups** toolbar control on the **Recovery tasks** tab. Select **Add groups**, choose one or more groups from the **Select task template groups** dialog, and select **Add**. Each task template in the group becomes a recovery task on the parent record. Use the parallel **Add tasks** control to add individual task templates without a group context.

The **Select task template groups** dialog is filtered by context:

-   From a plan, the dialog lists every group whose **Active** is true.
-   From a loss scenario, the dialog applies an additional filter so that only groups whose **Applicable to element definitions** is **All element definitions**, or whose **Element definitions** contains the element definition of the loss scenario, are listed.
-   From a recovery strategy, the same loss-scenario filter applies because a recovery strategy inherits its element definition from its parent loss scenario.

When you open **Add groups** or **Add tasks** from a list that is itself filtered \(for example, **Phase** = **Recovery validation**\), the active list filters are applied as default field values on the new tasks. A field that is already set on the source task template takes precedence over the list filter for that field.

\[Omitted image "select-task-templates-groups-list.png"\] Alt text: Select task template groups dialog listing available groups such as TG1 with their description and active status.

\[Omitted image "select-task-template-groups-with-filter.png"\] Alt text: Select task template groups dialog with the Filter panel showing Plan and Phase chips.

\[Omitted image "element-definition-filter-applied.png"\] Alt text: Select task template groups dialog opened from a loss scenario, showing the element definition filter.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, open the plan record and navigate to the Recovery tasks tab.

    When no recovery tasks exist, the tab shows an empty list with an Insert button.

3.  Navigate to the **Recovery tasks** tab and select **New**.

    The recovery tasks that are added at the business continuity plan level are displayed on the **Recovery tasks** tab. You can add a recovery task to the business continuity plan as shown in the example.

    You can use the order of the tasks calculated by the system based on their dependencies. A task that doesn’t have a dependency can be started first and it has the higher assigned order. Whenever you update or save the order of the tasks, the system recalculates and displays the order of all the tasks.

    If a plan has more than 500 tasks, the system doesn’t update the order of the tasks automatically. A manual intervention is required to set the order of the tasks. An informational message is displayed informing the users to select the **Update dependencies** UI action that is available in the plan and recovery task records.

    In a plan, while it’s possible to tag multiple assets, you can concentrate on particular assets for certain scenarios. Beginning with the Xanadu release, you can tag specific assets to a recovery task and calculate the time taken to recover each asset accurately during an event or exercise. The actual duration and total effort of the assets in the events are determined based on the tagging of the assets. You have these options in the **Tag assets** field for assigning assets to a recovery task:

    -   **None**
    -   **Specific**
    -   **All**
    For example, when you select **Specific assets** in the **Tag assets** field, the **Asset scope** field is set to visible, enabling you to specify which assets can be tagged with the selected recovery task.

    The assets tagged in the recovery task are then included in the impacted assets for the event task. Properly tagging assets with recovery tasks verifies precise calculations of the recovery times for each asset. Note that only assets associated with newly created event tasks are copied over.

    Beginning with the Xanadu and later releases, a new field called **Planned duration** has been added to the recovery task form. The **Planned duration** field replaces the **Completion deadline** field, which was a reference field used for time frames. The **Completion deadline** field is removed from the plan task records.

    The **Planned duration** field enables you to enter the anticipated time needed to complete the task. After the event and exercise have been carried out, you can revisit and modify the data in this field. It offers a detailed view of the task's progress and the time needed for its completion.

    The Create New Recovery task form is displayed.

    \[Omitted image "create-new-recovery-task.png"\] Alt text: Create New Recovery task form.

4.  On the form, fill in the fields.

    For more information on the fields in the form, see [Create New Recovery task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-recovery-task-form.md).

5.  Assign a phase to the recovery task.

    The Phase column is available in both the list and form views of a recovery task.

    \[Omitted image "reco-task-phase-column.png"\] Alt text: Phase column.

    BCM administrators and managers can update recovery task phases using inline editing. BCM planners can also update phases, but only if they are the plan owners.

    Only active phases are available for selection in the Phase column as shown in the example.

    \[Omitted image "phase-column-recovery-task.png"\] Alt text: Phases for selection.

    The phases of a recovery task can also be updated by modifying the Phase field in the form itself.

    \[Omitted image "phase-field-in-recovery-task.png"\] Alt text: Phase field on the form.

6.  To exclude specific tasks from time calculation, select the **Do not include in time calculation** option.

    When creating a recovery task, you can select this check box to exclude it from calculations.

    This feature also applies at the asset level, enabling for accurate tracking of time and effort for relevant assets. By providing this flexibility, the feature enhances the accuracy of time and effort calculations.

7.  Verify the achieved recovery level of the impacted assets of a task in the **Asset recovery level** field.

    In events, the **Asset recovery level** field indicates the achieved recovery level of the impacted assets of that event task, once all tasks with that recovery level \(for example, all tasks with Partially recovered state\) are completed.

    Previously, the assets were automatically marked as Recovered only when all event tasks were completed, even if those assets were in later phases such as Return to normal or Post-incident review. This approach delayed visibility into operational readiness. For example, even if an asset was functionally available during the Recovery phase, the system didn't reflect the status until all tasks were done.

    Starting with BCM release 9.x.x and later, the asset recovery status has been enhanced to provide granular tracking. Completing specific tasks now automatically updates the corresponding event asset state, progressing from **Not Recovered** → **Partially Recovered** → **Recovered**.

    Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables recovery coordinators to identify when dependent assets can safely start their recovery process.

    In plans, the Asset recovery level column features color coding, offering visual cues for various recovery progress levels. Specifically, "partially recovered" is denoted by an info color, while "recovered" is indicated by a success color, making it easier to track recovery status at a glance.

    \[Omitted image "asset-reco-level-column.png"\] Alt text: Asset Recovery Level column.

    **Note:**

    The current demo data has an issue where both **Include task in** and **Tag asset** fields are empty. To resolve this, you have to add tasks to **Include task in** manually and select assets for the **Tag asset** field. Without these, event tasks won't be created and assets won't be marked as impacted.

    If you haven't selected **Include task in**, your event task won't be created. If you don't select **Tag asset**, your asset won't be marked as an impacted asset.

    This issue doesn't apply to newly created plans or old plans; it is applicable only for the current demo data.

8.  Select a **Plan loss scenario** to scope the task to a specific disruption context, such as Loss of Datacenters.

    Scoping a task to a loss scenario ensures that only tasks relevant to the active scenario are surfaced when the plan is exercised under that scenario type. The **Plan loss scenario** and **Task group** columns are visible on the **Recovery tasks** tab of the loss scenario record.

    \[Omitted image "qi-insert-action.png"\] Alt text: Recovery tasks tab on a loss scenario record showing the Task group and Plan loss scenario columns alongside Planned duration.

9.  In the **Assignment details** section, verify or update the **All assets from plan** field to specify the asset scope for this task.

    The field defaults to all assets defined in the plan. Narrow the scope when the task applies only to a subset of the plan's assets.

    \[Omitted image "qi-create-reco-task-panel.png"\] Alt text: Quick recovery task panel showing the All assets from plan field in the Assignment details section alongside the Planned duration fields.

10. Enter the estimated completion time in the **Planned duration** fields: **Hours**, **Minutes**, and **Seconds**.

    Planned duration values are used in Gantt chart rendering and scheduling calculations. Enter 0 in all fields if the duration is not yet known.

11. Select **Save**.

    The updated recovery tasks are now displayed in the UI.


## Result

From the **Recovery tasks** tab toolbar, select one or more rows and use the **Save as group** split button to make the selected tasks reusable:

-   **Save as group** creates a new task template group from the selected tasks. Open the **Create task template group** modal, enter a **Group name**, and select **Create**. Group names are unique; if you enter a name that is already in use the modal displays an inline error and prevents creation.
-   **Save as group** &gt; **Add to group** appends the selected tasks to an existing task template group. Dependencies between the selected tasks are preserved.
-   **Save as group** &gt; **Save tasks** \(single row selected\) saves the individual task as a task template, without any group context and without inter-task dependencies.

\[Omitted image "save-as-group-button-tooltip.png"\] Alt text: Save as task templates group tooltip on the Save as group split button.

\[Omitted image "save-as-group-create-dialog.png"\] Alt text: Create task template group modal showing the You selected 2 task\(s\) confirmation and the Group name field.

\[Omitted image "save-as-group-confirmation-banner.png"\] Alt text: Banner confirming the selected recovery tasks were added as task templates in the selected task template group.

\[Omitted image "qi-save-tasks.png"\] Alt text: Recovery tasks tab toolbar showing the Save as group dropdown expanded with Save tasks and Add to group options.

-   **[Create New Recovery task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-recovery-task-form.md)**  
Use the Create New Recovery task form in the BCM Configurable Workspace to input the necessary details regarding the recovery task.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

