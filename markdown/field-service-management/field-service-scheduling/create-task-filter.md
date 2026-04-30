---
title: Create a task filter for dynamic scheduling
description: Task filters allow you to define criteria for selecting and assigning tasks to the most suitable agents using dynamic scheduling.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Configure dynamic scheduling, Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a task filter for dynamic scheduling

Task filters allow you to define criteria for selecting and assigning tasks to the most suitable agents using dynamic scheduling.

## Before you begin

Role required: admin

## About this task

Task filters help you refine how tasks are assigned to the most suitable agents. You can use the default filters provided by the Dynamic Scheduling plugin or create custom filters tailored to your organization’s specific needs.

Dynamic Scheduling, when combined with Auto Assignment and Immediate Assignment, offers flexibility in task allocation. Tasks can be assigned instantly or at scheduled intervals, depending on your configuration.

The following table explains how Dynamic Scheduling behaves with different combinations of Auto Assignment and Immediate Assignment settings. These options let you balance automated task assignment with manual control.

|Auto assignment|Immediate assignment|Result|
|---------------|--------------------|------|
|Enabled|Enabled|Dynamic Scheduling runs instantly, automatically assigning tasks to field agents.|
|Enabled|Disabled|Dynamic Scheduling runs, adding tasks to a scheduled batch. Tasks are assigned to agents at regular intervals.|
|Disabled|Disabled|The dispatcher manually triggers Dynamic Scheduling, and tasks are sent back for confirmation before assignment.|

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  In the **Task Filters** related list, click **New**.

3.  Fill in the fields on the Task Filter form.

<table id="table_czw_non_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the task filter.

</td></tr><tr><td>

Active

</td><td>

Select to activate the task filter.

</td></tr><tr><td>

Execution Order

</td><td>

Set the priority for the filter. Filters with lower execution order values are applied first, creating the initial task list. Higher values further refine the list. For example, filters for maintenance tasks have a lower order than filters for pending dispatch or appointment tasks.

</td></tr><tr><td>

Table

</td><td>

Select the task table \(e.g., Work Order Task\) that this filter will apply to.

</td></tr><tr><td>

Conditions

</td><td>

Specify the conditions that will identify which tasks to include in the filter.

</td></tr><tr><td>

Resource Type

</td><td>

Choose whether the tasks should be assigned to individual users or crews. Select User \[sys\_user\] for individual agents or Crew \[wm\_crew\] for teams.

</td></tr><tr><td>

Auto Assign

</td><td>

Select to automatically assign tasks. The **Auto Assignment Frequency** field appears when this field is selected.

</td></tr><tr><td>

Auto Assignment Frequency

</td><td>

Choose the auto assignment frequency:-   Immediate: Tasks are assigned as soon as they are ready.
-   Interval: Tasks are assigned at regular intervals that you define.
If you select **Interval**, the **Auto Assignment Interval** field appears.

</td></tr><tr><td>

Auto Assignment Interval

</td><td>

Set the interval \(in minutes\) for how often tasks should be auto-assigned. The task filter with a higher Execution Order value must have an interval greater than a task filter with a lower Execution Order value.

</td></tr></tbody>
</table>4.  In the **Select Criteria** related list, choose the criteria that will be used to evaluate and identify suitable agents for each task.

    1.  Assign a weight to each criterion based on its importance.

        **Note:** By default, each matching criterion has an assigned weight of 10. You can assign a higher weight to the criteria that are more important or assign a lower weight to the criteria that are less important.

    2.  Select a ranking method for the selected matching criteria.

        **Note:** Use **More is Better** for agent availability as more availability is preferred. Use **Less is Better** when selecting an agent based on the number of assigned tasks as fewer tasks are preferred

    For more information, see [Matching criteria for task filters](../concept/task-assignment-matching-criteria.md).

5.  Click **Save**.


## Result

The task filter is ready for use in the dynamic scheduling process, optimizing task assignments based on your defined criteria and preferences. Dynamic scheduling uses the following formula to calculate the agent rank or score by multiplying each criterion's rating by its respective weight, dividing by the total weight of all criteria, and summing the results.

```
(Criteria_1_rating * Criteria_1_weight) / total_criterion_weight + 
(Criteria_2_rating * Criteria_2_weight) / total_criterion_weight + 
(Criteria_3_rating * Criteria_3_weight) / total_criterion_weight = agent_rank/score
```

## What to do next

[Create a task ordering rule](create-task-ordering-rule.md)

