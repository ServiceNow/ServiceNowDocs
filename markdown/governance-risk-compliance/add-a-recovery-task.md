---
title: Add recovery tasks
description: Add a recovery task as part of the planned recovery strategy. You can add one or more recovery tasks for a loss scenario and those recovery tasks are displayed in the loss scenario itself. Automate the recovery tasks in a plan for a faster recovery.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 7
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add recovery tasks

Add a recovery task as part of the planned recovery strategy. You can add one or more recovery tasks for a loss scenario and those recovery tasks are displayed in the loss scenario itself. Automate the recovery tasks in a plan for a faster recovery.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Beginning with the Xanadu release, cyclic dependencies in recovery tasks can be avoided to prevent repeated invocation of the same plan from other plans.

![Plan record tabs.](../image/plan-record-tabs.png)

For example, in the Recovery task of Cyclic plan example 1 invokes Cyclic plan example 2, Cyclic plan example 2 invokes Cyclic plan example 3 and then again Cyclic plan example 3 invokes Cyclic plan example 1. If you attempt to add a link bet Cyclic plan example 2 and Cyclic plan example 3, it isn’t allowed. An error message, similar to the one shown in the example, prompts you to choose a different related plan to help prevent such issues from occurring in an event.

![Cyclic plan error message.](../image/cyclic-plan-error-message.png)

Similarly, if plans are activated beyond 10 levels or hierarchical links involving more than 10 levels of plans are created, an error message is displayed, suggesting the removal of the plan before saving the record.

![Plan levels.](../image/cyclic-plan-levels.png)

Starting from version 6.1.x of the Business Continuity Management application, the integration of recovery task automation into the business continuity planning process is introduced. This automation aims to enhance efficiency, save time, and minimize the risk of human errors. Users who have the necessary access to the recovery task can classify it as either manual or automated. These tasks are organized in a sequential manner with dependencies.

To automate a recovery task, administrators or application developers create an automation flow and associate it with the task. When the task moves to the **Open** state \(when the plan is activated as part of an exercise or an actual event\), the automated flow is triggered. However, there may be instances where the automated flow fails due to system errors. In such cases, the user with access to the recovery task can activate the manual task as a backup and assign it to a designated backup assignee. The backup assignee receives a system-generated email to complete the task flow. Plan users have the opportunity to practice business continuity plan exercises and make improvements based on the results obtained.

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
    For example, when you select **Specific assets** in the **Tag assets** field, the **Asset scope** field the Asset scope field becomes visible, enabling you to specify which assets can be tagged with the selected recovery task.

    The assets tagged in the recovery task are then included in the impacted assets for the event task. Properly tagging assets with recovery tasks verifies precise calculations of the recovery times for each asset. Note that only assets associated with newly created event tasks are copied over.

    Beginning with the Xanadu and later releases, a new field called **Planned duration** has been added to the recovery task form. The **Planned duration** field replaces the **Completion deadline** field, which was a reference field used for time frames. The **Completion deadline** field is removed from the plan task records.

    The **Planned duration** field enables you to enter the anticipated time needed to complete the task. After the event and exercise have been carried out, you can revisit and modify the data in this field. It offers a detailed view of the task's progress and the time needed for its completion.

    The Create New Recovery task form is displayed.

    ![Create New Recovery task form.](../image/create-new-recovery-task.png)

4.  On the form, fill in the fields.

    For more information on the fields in the form, see [Create New Recovery task form](../reference/create-new-recovery-task-form.md).

5.  Assign a phase to the recovery task.

    The Phase column is available in both the list and form views of a recovery task.

    ![Phase column.](../image/reco-task-phase-column.png)

    BCM administrators and managers can update recovery task phases using inline editing. BCM planners can also update phases, but only if they are the plan owners.

    Only active phases are available for selection in the Phase column as shown in the example.

    ![Phases for selection.](../image/phase-column-recovery-task.png)

    The phases of a recovery task can also be updated by modifying the Phase field in the form itself.

    ![Phase field on the form.](../image/phase-field-in-recovery-task.png)

6.  To exclude specific tasks from time calculation, select the **Do not include in time calculation** option.

    When creating a recovery task, you can select this check box to exclude it from calculations.

    This feature also applies at the asset level, enabling for accurate tracking of time and effort for relevant assets. By providing this flexibility, the feature enhances the accuracy of time and effort calculations.

7.  Verify the achieved recovery level of the impacted assets of a task in the **Asset recovery level** field.

    In events, the **Asset recovery level** field indicates the achieved recovery level of the impacted assets of that event task, once all tasks with that recovery level \(for example, all tasks with Partially recovered state\) are completed.

    Previously, the assets were automatically marked as Recovered only when all event tasks were completed, even if those assets were in later phases such as Return to normal or Post-incident review. This approach delayed visibility into operational readiness. For example, even if an asset was functionally available during the Recovery phase, the system didn't reflect the status until all tasks were done.

    Starting with BCM release 9.x.x and later, the asset recovery status has been enhanced to provide granular tracking. Completing specific tasks now automatically updates the corresponding event asset state, progressing from **Not Recovered** → **Partially Recovered** → **Recovered**.

    Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables recovery coordinators to identify when dependent assets can safely start their recovery process.

    In plans, the Asset recovery level column features color coding, offering visual cues for various recovery progress levels. Specifically, "partially recovered" is denoted by an info color, while "recovered" is indicated by a success color, making it easier to track recovery status at a glance.

    ![Asset Recovery Level column.](../image/asset-reco-level-column.png)

    **Note:**

    The current demo data has an issue where both **Include task in** and **Tag asset** fields are empty. To resolve this, you have to add tasks to **Include task in** manually and select assets for the **Tag asset** field. Without these, event tasks won't be created and assets won't be marked as impacted.

    If you haven't selected **Include task in**, your event task won't be created. If you don't select **Tag asset**, your asset won't be marked as an impacted asset.

    This issue doesn't apply to newly created plans or old plans; it is applicable only for the current demo data.

8.  Select **Save**.

    The updated recovery tasks are now displayed in the UI.


-   **[Create New Recovery task form](../reference/create-new-recovery-task-form.md)**  
Use the Create New Recovery task form in the BCM Configurable Workspace to input the necessary details regarding the recovery task.

**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

