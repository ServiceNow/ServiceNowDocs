---
title: Create New Event Task form
description: Use the Create New Event Task form in BCM UIB Workspace to add details about an event task.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Monitor event tasks and create ad-hoc tasks, Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create New Event Task form

Use the Create New Event Task form in BCM UIB Workspace to add details about an event task.

## Create New Event Task form

For description of the field values, see the table.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Details tab

</td></tr><tr><td>

Task ID

</td><td>

ID for the event task. Defaults to the next number of existing event tasks for the plan.

</td></tr><tr><td>

Short description

</td><td>

Brief note about the event task.

</td></tr><tr><td>

Impacted assets

</td><td>

Assets that are impacted for the event task.

</td></tr><tr><td>

Task classification

</td><td>

Classification for the event task. Options are: **Manual** and **Automatic**. When you create an ad-hoc task manually, the task classification defaults to Manual.

</td></tr><tr><td>

Planned start

</td><td>

Planned start date of the event task.

</td></tr><tr><td>

Phase

</td><td>

Active phase to be associated with the event task. You can associate these phases with an event task:

-   **Preparation**
-   **Recovery**
-   **Recovery validation**
-   **Return to normal**
-   **Return to normal validation**
-   **Post-incident review**

You can use the **Group by Phase** option in the Phases column to organize event tasks by a specific phase and its order, making it easier to filter and manage related tasks.

![Phase order.](../image/event-task-phase-order.png)When you order the event tasks by the phase order, you can view the event tasks in a sequence in which they are executed.

![Sequence.](../image/event-task-phase-order-sequence.png)

</td></tr><tr><td>

Do not include this task in time calculation option

</td><td>

Option to exclude specific event tasks from time calculations. For scenarios with multiple tasks, you can exclude specific tasks from overall time calculations, effectively removing them from the total time estimate. This allows for more accurate time tracking by focusing only on relevant tasks. Any task that is excluded is not considered in the plan and asset time calculation.

</td></tr><tr><td>

State

</td><td>

State of the event. It defaults to the **Pending** state.

</td></tr><tr><td>

Activated plan

</td><td>

Activated plan for the event task.

</td></tr><tr><td>

Dependencies

</td><td>

Dependencies for the tasks. For tasks copied from the plan level, dependencies are copied from the plan recovery task. Dependencies cannot be added for ad-hoc tasks.**Note:**

Beginning with the Australia release, you can now manually add a dependency for the event task or select an event task from the list in the **Dependencies** field. Only applicable event tasks are shown in this field.

![Dependency.](../image/event-task-dependency-field.png)

</td></tr><tr><td>

Planned end

</td><td>

Planned end for the event task.

</td></tr><tr><td>

Asset recovery level

</td><td>

Option to enable clearer visual indicators for different levels of recovery progress for the asset. Available options are:

-   **None**
-   **Partially recovered**
-   **Recovered**

 The 'Asset recovery level' column is now available in both recovery and event tasks. You can manually update this column to indicate that all tasks associated with a specified asset recovery level must be completed to achieve that level.

 Color coding on the Asset Recovery Level column enables clearer visual indicators for different levels of recovery progress.

 Previously, all steps in a recovery process had to be completed before marking an asset as recovered. Now, you can mark an asset as partially recovered after completing critical steps, and address smaller, ad-hoc tasks later.

 For example, if a recovery process involves three steps, you can consider an asset recovered after completing step two, and defer step three to a later time. This provides greater flexibility in managing your recovery processes.

 For more information on enhanced event asset management, see [Event assets](../concept/event-assets.md).

</td></tr><tr><td>

Planned duration

</td><td>

Planned duration of the event task in days, hours, minutes, and seconds. When you enter the Planned start date, the Planned end date on the activated plan and on the event tasks is calculated based upon the **Planned duration** field.**Note:** If you have more than 500 tasks for an event or exercise, the planned times are not calculated automatically. A UI action named **Refresh tasks data** is shown. Select the UI action to refresh the Planned start date, Planned end date, and Order.

 The progress of this calculation can be tracked using the View Progress button in the **Event task** form.

</td></tr><tr><td>

Actual start

</td><td>

Start date and time for the event task.

</td></tr><tr><td>

Actual end

</td><td>

End date and time for the event task.

</td></tr><tr><td>

Actual time taken

</td><td>

Actual time taken for the event task.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment details

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the event task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User or users from the Assignment group. If the **Assignment group** field is empty, then select any user.

</td></tr><tr><td>

Additional assignee list

</td><td>

Additional users that are assigned to the event task.

</td></tr><tr><td class="sub-head" colspan="2">

Similar tasks group

</td></tr><tr><td>

Similar tasks group

</td><td>

Similar tasks group that the event task can be assigned to. Only eligible event tasks are displayed in the group.

</td></tr><tr><td>

Original task

</td><td>

Original task assigned by the system. When an event starts, the system identifies the first executed event task as the original task. Other similar tasks are modified as duplicate tasks in the group. When a task gets added into the similar tasks group, the system marks it in the **On hold** state. Tasks with dependencies can be managed such that only one task with dependencies is added to the group, and once dependencies are resolved, duplicate tasks are closed when the original task is completed. You cannot edit the **Original task** field at any time. It is auto-assigned only after the event task starts executing.

</td></tr></tbody>
</table>**Parent Topic:**[Monitor event tasks and create ad-hoc tasks](../task/add-an-event-task-to-exercise-event.md)

