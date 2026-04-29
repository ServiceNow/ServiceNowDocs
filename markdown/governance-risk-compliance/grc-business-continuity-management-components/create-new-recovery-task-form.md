---
title: Create New Recovery task form
description: Use the Create New Recovery task form in the BCM Configurable Workspace to input the necessary details regarding the recovery task.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Add recovery tasks, Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create New Recovery task form

Use the Create New Recovery task form in the BCM Configurable Workspace to input the necessary details regarding the recovery task.

## Create New Recovery task form

For description of the field values, see the table.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Recovery task

</td></tr><tr><td>

Short description

</td><td>

Short description for the recovery task.

</td></tr><tr><td>

Planned order

</td><td>

Planned order of the recovery task. The sequence for the recovery task is automatically determined and populated in the Planned order field. This sequence is derived from the values in the Dependencies field, which outlines the task dependencies. For instance, if task 2 relies on task 1, then task 1 is assigned order 1, and task 2 is assigned order 2. In scenarios where a task depends on two other tasks, the task with the highest planned order among the dependencies is used. It's possible for two tasks to both have a planned order of 2 if each is dependent on task 1.

**Note:** To update the planned order of a recovery task, use the **Refresh task order** UI action.

</td></tr><tr><td>

Task ID

</td><td>

Unique number assigned to each task. It enables you to view the tasks in a particular sequence especially in a printed PDF.

</td></tr><tr><td>

Dependencies

</td><td>

Dependencies related to the recovery task.

</td></tr><tr><td>

Don’t include this task in time calculation option

</td><td>

Option to exclude specific event tasks from time calculations.

 When this flag is checked, the selected task is excluded from time calculations during an event. In the Crisis management app, checking this flag confirms that the task is not included in the **Actual time taken** and **Total effort** field updates for both the asset and the activated plan associated with the event.

 For scenarios with multiple tasks, you can exclude specific tasks from overall time calculations, effectively removing them from the total time estimate. This enables for more accurate time tracking by focusing only on relevant tasks. Any task that is excluded isn’t considered in the plan and asset time calculation.

</td></tr><tr><td>

Task classification

</td><td>

Classification of the recovery task. Available options are:-   **Manual**: Classify the recovery task as a manual task.
-   **Automated**: Classify the recovery task as an automated task. When you classify the recovery task as an automated task, the **Automated flow** field is displayed on the form. For a faster recovery, the recovery tasks can be automated.

</td></tr><tr><td>

Include task in

</td><td>

Option to include the recovery task in exercises, actual events, or both. With this flag, you can prevent test tasks from coming into the events. Available options are in the order of priority:

-   **Both actual events and exercises**
-   **Actual events only**
-   **Exercises only**

</td></tr><tr><td>

Plan

</td><td>

Plan associated with the recovery task. This field is auto-filled and is read-only.

</td></tr><tr><td>

Tag

</td><td>

Tag marked for the recovery task.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item associated with the recovery task.

</td></tr><tr><td>

Phase

</td><td>

Phase associated with the recovery task.

</td></tr><tr><td>

Tag assets

</td><td>

Option to associate all assets, no assets, or specific assets with a recovery task. The actual duration and effort recorded in the events are determined by how the assets are tagged as shown with these options:

-   **None**: Associate no assets from the plan with the recovery task.
-   **Specific assets**: Select this option to display the **Asset scope** field. It enables you to define the scope for the assets that are tagged within the plan.
-   **All**: Associate all assets from the plan with the recovery task.

 Once this configuration is established and the plan is activated during an event, the assets are tagged. The time and effort recorded in the events are determined by how the assets are tagged.

</td></tr><tr><td>

Asset scope

</td><td>

Field visible only when the **Specific assets** option is selected in the **Tag assets** field. You can select particular assets to associate with the recovery task. When an event task is generated from this recovery task, these chosen assets are shown as the associated assets in the event task. The assets linked to the recovery task from the plan are then replicated as the assets for the event tasks.

</td></tr><tr><td>

Asset recovery level

</td><td>

Option to enable clearer visual indicators for different levels of recovery progress for the asset. Available options are:

-   **None**: The selected recovery or event task is not recovered.
-   **Partially recovered**: The event asset is partially recovered after completing the associated recovery task.
-   **Recovered**: The event asset is fully recovered after completing the associated recovery task.

Color coding in the Asset Recovery Level column provides clearer visual indicators for different recovery progress levels.

![Asset Recovery Level column.](../image/asset-reco-level-column.png)The Asset recovery level column is introduced in both recovery tasks and event tasks. You can select the "Recovery Level" of asset. It will be updated once all tasks with similar recovery level are completed.

The "Asset Recovery Level" column has been added to both recovery tasks and event tasks, enabling you to select the recovery level for an asset. Once all associated tasks with the same recovery level are completed, the asset's state is auto-updated.

The existing recovery process required all steps to be completed before an asset could be marked as recovered. This functionality remains supported. Additionally, a new capability has been introduced, allowing you to mark an asset as "Partially recovered" after completing critical tasks. This enhancement provides better visibility into the recovery process, enabling teams to address smaller, ad-hoc tasks later.

For example, if a recovery process involves three steps, you can consider an asset recovered after completing step two, and defer step three to a later time. This provides greater flexibility in managing your recovery processes.

</td></tr><tr><td class="sub-head" colspan="2">

Key timeline

</td></tr><tr><td>

Planned duration

</td><td>

Planned duration of the recovery task shown in Days, Hours, Minutes, and Seconds. This field is crucial for determining several aspects: -   Establishing the planned start and end times during execution.
-   Calculating any delays that occur during execution.

 The default setting for this field is 00:00:00:00. The **Completion deadline** field, which was a reference field used previously for indicating time frames, is now removed from the plan task records.

</td></tr><tr><td class="sub-head" colspan="2">

Related plan

</td></tr><tr><td>

Activate a related plan

</td><td>

Option to activate a related plan for the recovery task.

 The enhanced application software checks for cyclic dependencies among the recovery tasks, as these can lead to errors during execution. If a cyclic dependency is detected in a task, an error message is displayed, helping prevent further actions on that task. If the dependency level of the tasks is more than 10, you can’t save the recovery task record.

 You can also record the estimated duration of a recovery task and view the sequence of the recovery tasks in the plan, which are organized based on their dependencies.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment details

</td></tr><tr><td>

Owner

</td><td>

Assigned owner for the recovery task.

</td></tr><tr><td>

Additional assignees

</td><td>

Additional assignees listed for the recovery task.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr><td>

Recovery team

</td><td>

Recovery team that the recovery task is assigned to.

</td></tr><tr><td class="sub-head" colspan="2">

Plan details

</td></tr><tr><td>

Documentation

</td><td>

Documentation section defined in the business continuity plan.

</td></tr><tr><td>

Description

</td><td>

Description of the recovery plan.

</td></tr><tr><td>

Recovery strategy

</td><td>

Recovery strategy defined on the **Recovery strategy** tab.

</td></tr><tr><td>

Flow variables \(Automated flow\)

</td><td>

Automated flows that are available under the Task automation category. The automated flow gets triggered when the task moves to the **Open** state \(when the plan is activated as part of an exercise or an actual event\). You can add the required flow variables and then populate the automated flow.

</td></tr><tr><td>

Variables

</td><td>

Variables added to the flow. This field is displayed only after you save the automated flow.

</td></tr><tr><td>

Backup assignee group

</td><td>

Group that the backup assignee belongs to.

</td></tr><tr><td>

Backup assignee

</td><td>

Assignees that are used as a backup if the automated task fails during the execution.

</td></tr></tbody>
</table>**Parent Topic:**[Add recovery tasks](../task/add-a-recovery-task.md)

