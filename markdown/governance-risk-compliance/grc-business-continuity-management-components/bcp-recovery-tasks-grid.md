---
title: Create, update, and group recovery tasks
description: Create tasks in a plan to recover your business from various disaster situations. Prioritize the tasks by determining the critical assets that have to be recovered and estimate the time by which the task must be completed.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create, update, and group recovery tasks

Create tasks in a plan to recover your business from various disaster situations. Prioritize the tasks by determining the critical assets that have to be recovered and estimate the time by which the task must be completed.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Assign the task to a group, identifying an owner, to execute the processes and procedures of a recovery. The task has details of the item to be recovered and the time by which it should be accomplished.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Recovery Tasks** tab of the plan.

    The **Recovery Tasks** tab displays all the data in editable lists. You can prioritize the tasks by sorting, grouping, and filtering each column of data the way you want.

6.  To create a recovery task, click **New**.

    1.  On the form, fill in the fields.

<table id="table_pbg_fgn_n4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task ID

</td><td>

Number assigned to each task. Indicates the position of the task with respect to other tasks in the grid.Enables you to view the tasks in a particular sequence especially in a printed PDF.

</td></tr><tr><td>

Scope

</td><td>

Asset that the task recovers. If field is empty, the task recovers asset at the plan level. Otherwise, it recovers the recovery task scope.

</td></tr><tr><td>

Recovery team

</td><td>

Team to which the recovery task is assigned.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr id="refer-related-plan-bcp"><td>

Refer a different plan

</td><td>

Option to indicate that the recovery task is not an individual task, but refers to a separate plan with its own set of tasks.If the check box is clear then the recovery task is executed normally as per the task ID sequence at the time of exercise.

</td></tr><tr><td>

Select plan

</td><td>

Plan from the list in the **Related Plans** tab. If the task has a referred related plan within, then the tasks of the referred plan are executed before the execution continues sequentially with the rest of the recovery tasks in the main plan.Field appears only if the **Refer a different plan** check box is enabled.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr><td>

Dependencies

</td><td>

Tasks dependent on the asset and plan, ruling out cyclic dependency.

</td></tr><tr><td>

Documentation

</td><td>

Details about the execution of the plan.

</td></tr><tr><td>

Recovery strategy

</td><td>

Objective to recover an asset identified in a plan.

</td></tr><tr><td>

Completion deadline

</td><td>

Time by which the recovery task must be completed.

</td></tr><tr><td>

Configuration item

</td><td>

Item or asset that is recovered in this task.

</td></tr><tr><td>

Description

</td><td>

Brief note about the recovery task.

</td></tr></tbody>
</table>        **Note:** You can create a recovery task at the recovery strategy level and also at the plan level.

    2.  Click **Create**.

    -   **Recovery task grid**

        All recovery tasks that you have created for the plan appear in a grid. You can group the recovery tasks based on the fields in the recovery task table. Grouping helps you to group the recovery tasks the way you want, focus, and manage the task groups.

        **Note:** To group by a field, you must set up the group criteria value as a BCM admin by selecting the **Group recovery tasks** option and a value in the **Group by** field of the plan template before creating the plan.

    -   **Dependencies**

        The dependencies column displays recovery tasks that match the asset scope level and the plan level. However, If it is at scope level, then it displays recovery tasks that match the scope level and also tasks that do not have a scope.

        If it is at the Plan level, then the recovery tasks that match only at the plan level are displayed. Considering that the plan level recovery task does not have any scope.

        If there is a cyclic dependency between tasks, then those recovery tasks are not displayed in the **Dependencies** column.

    -   **Task group**

        Groups the tasks based on the **Group by** field in the plan template.

7.  To edit the data in a cell, double-click and click again in the cell.

8.  To apply grouping and filter, click the vertical ellipsis icon.

    -   **Sort**

        You can sort the data at each column level. The first click in the column header sorts the data of the column in ascending order \(![Ascending icon](../image/AscendingIcon.png)\). The next click makes the sort descending \(![Descending icon](../image/DescendingIcon.png)\). Another click removes the sort.

    -   **Filter**

        Apply column filter to filter data that have simple text. For example, you can filter tasks with short descriptions that talk about safety.

        Use the simple number filter to filter time critical data. For example, you can apply the filter to the **Completion deadline** column to filter the tasks that have to be completed within an hour of a business disruption.

        ![Group and filter tasks](../image/GroupFilter.png "Group and filter tasks")

9.  To remove the filter, click the **Clear** button.

10. To delete one or more recovery tasks, select the record or records and click the **Remove** button.


**Parent Topic:**[Structured workflows for Business Continuity Planning](../concept/business-continuity-planning-overview.md)

