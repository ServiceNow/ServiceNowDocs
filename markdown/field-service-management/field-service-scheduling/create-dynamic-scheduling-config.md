---
title: Configure dynamic scheduling
description: Dynamic Scheduling enables automatic task assignment to field agents based on predefined rules and configurations. This feature helps streamline task distribution by verifying the correct tasks are assigned to the most suitable agents, optimizing travel time, skill matching, and task priority.Task filters allow you to define criteria for selecting and assigning tasks to the most suitable agents using dynamic scheduling.The Dynamic Scheduling uses configurable matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.Dynamic scheduling uses task ordering rules to prioritize and arrange tasks effectively. These rules ensure tasks are handled in the right sequence, helping you streamline field service operations.Dynamic scheduling allows you to define unassignment constraints that prevent certain tasks from being unassigned, even when lower in priority. This feature ensures that critical tasks stay assigned, based on dependencies or urgency.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 21
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configure dynamic scheduling

Dynamic Scheduling enables automatic task assignment to field agents based on predefined rules and configurations. This feature helps streamline task distribution by verifying the correct tasks are assigned to the most suitable agents, optimizing travel time, skill matching, and task priority.

## Before you begin

-   Select dynamic scheduling as the preferred task assignment method. This verifies that tasks are automatically assigned to field agents based on predefined criteria and rules. For more information, see [task assignment method](../../planning-and-policy/task/t_ConfigureFieldService.md#AssignmentOptions).
-   Set up agent schedules so that dynamic scheduling systematically verifies optimal task allocation. For more information, see [Set up agent schedules for dynamic scheduling](../concept/agent-schedule-dynamic.md).
-   Review the properties and other installed components related to dynamic scheduling. Customize the settings to align with your organization's specific requirements. For more information, see [Review system properties and components for Dynamic Scheduling](../reference/dynamic-sched-system-properties.md).
-   Verify to configure travel time and distance calculation to determine how the system calculates an agent's estimated travel time and distance to a task location. You can choose between using the Google Maps API for real-time travel estimates or straight-line estimates based on the geolocation property settings.
    -   If the `Use Google Maps API for travel time estimates` geolocation property is enabled, choose between using the Google Maps API or straight-line estimates.
    -   If the `Use Google Maps API for travel time estimates` geolocation property is turned off, the system considers the Estimated Travel Duration field's value from the work order task.

Role required: admin

## About this task

By default, the `Dynamic Scheduling Config for Work Order` configuration is available with the Dynamic Scheduling plugin. You can modify the configuration as needed or use as a template to create your custom configuration.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  Update an existing work configuration or create one.

    This field only appears if you have the plugin installed. For more information, see [Configuring Field Service Work Configurations](../concept/configuring-work-configs.md).

3.  Select the task table that dynamic scheduling uses to assign tasks to agents.

    The default table is `Work Order Task [wm_task]`. Dynamic scheduling can have only one configuration for each task table.

4.  Select the **Un-assignment** check box to let dynamic scheduling unassign a previously assigned task and assign a higher-priority task based on task ordering rules.

    When this option isn’t selected, the **Un-Assignment Constraints** related list won’t be visible in the form.

5.  Select the **Default Agent Work Schedule**.

    Configure the order in which dynamic scheduling determines an agent’s work schedule - the agent's specific work schedule, schedule specified on the agent’s user record, the default agent work schedule selected in this configuration, or the default 8-5 weekday schedule.

6.  Set the **Consider Territory Membership** to either consider or ignore the agent's territory membership for assigning tasks.

    This field appears when the Field Service Territory Planning plugin is enabled.

7.  In the **Task Filters** related list, add a task filter or modify an existing task filter or add a new filter.

    Task filters help identify which tasks should be assigned using dynamic scheduling. Within the filter, you can set criteria to match tasks with the most suitable agents. For more information, see [Create a task filter for dynamic scheduling](create-dynamic-scheduling-config.md#).

8.  In the **Task Ordering Rules** related list, add a new task ordering rule or modify an existing rule.

    Task ordering rules help to determine the order of tasks. For more information, [Create a task ordering rule](create-dynamic-scheduling-config.md#).

9.  In the **Un-Assignment Constraints** related list, add or modify criteria for unassigning tasks.

    This enables the system to free up agents for higher-priority tasks when needed. For more information, see [Create a task unassignment constraint](create-dynamic-scheduling-config.md#).

10. Select **Update**.

11. Select **Validate config** to validate the dynamic scheduling configuration.

    An information message appears at the top of the Dynamic Scheduling Configuration form if the configuration is valid.


## Result

Dynamic scheduling automatically assigns tasks to field agents based on the defined rules and schedules.

**Related topics**  


[Example - configure dynamic scheduling to assign preferred technicians to tasks](excluded-preferred-agents.md)

[Example - configure dynamic scheduling to ignore excluded technicians](prevent-excluded-agents.md)

[Assigning work order tasks to agents using dynamic scheduling](../concept/using-dynamic-scheduling.md)

## Create a task filter for dynamic scheduling

Task filters allow you to define criteria for selecting and assigning tasks to the most suitable agents using dynamic scheduling.

### Before you begin

Role required: admin

### About this task

Task filters help you refine how tasks are assigned to the most suitable agents. You can use the default filters provided by the Dynamic Scheduling plugin or create custom filters tailored to your organization’s specific needs.

Dynamic Scheduling, when combined with Auto Assignment and Immediate Assignment, offers flexibility in task allocation. Tasks can be assigned instantly or at scheduled intervals, depending on your configuration.

The following table explains how Dynamic Scheduling behaves with different combinations of Auto Assignment and Immediate Assignment settings. These options let you balance automated task assignment with manual control.

|Auto assignment|Immediate assignment|Result|
|---------------|--------------------|------|
|Enabled|Enabled|Dynamic Scheduling runs instantly, automatically assigning tasks to field agents.|
|Enabled|Disabled|Dynamic Scheduling runs, adding tasks to a scheduled batch. Tasks are assigned to agents at regular intervals.|
|Disabled|Disabled|The dispatcher manually triggers Dynamic Scheduling, and tasks are sent back for confirmation before assignment.|

### Procedure

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

    For more information, see [Matching criteria for assigning tasks](create-dynamic-scheduling-config.md#).

5.  Click **Save**.


### Result

The task filter is ready for use in the dynamic scheduling process, optimizing task assignments based on your defined criteria and preferences. Dynamic scheduling uses the following formula to calculate the agent rank or score by multiplying each criterion's rating by its respective weight, dividing by the total weight of all criteria, and summing the results.

```
(Criteria_1_rating * Criteria_1_weight) / total_criterion_weight + 
(Criteria_2_rating * Criteria_2_weight) / total_criterion_weight + 
(Criteria_3_rating * Criteria_3_weight) / total_criterion_weight = agent_rank/score
```

### What to do next

[Create a task ordering rule](create-dynamic-scheduling-config.md#)

### Matching criteria for assigning tasks

The Dynamic Scheduling uses configurable matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.

Matching criterion are used by other ServiceNow applications. For example, the 'Assigned Cases' matching criteria applies to the Case \[sn\_customerservice\_case\] table and is used by Customer Service Management \(CSM\). Any criterion can be copied, renamed, and configured for use against other tables, such as the work order task table. Be sure to test any configuration changes thoroughly. There are three types of matching criteria:

-   Simple Match: creates one-to-one matching, such as matching the time zone of an agent with the time zone of a task location.
-   Aggregate: uses a simple query and returns an aggregate result. For an aggregate type, select a table and create a filter, and then select an aggregate field such as the **Assigned to** field. This type of query returns a set of users.
-   Scripted: uses a scripted query which returns a list of users.

**Note:** Workforce optimization schedule and personal events aren't supported when using matching criteria.

<table id="table_rv3_4fg_lwb"><thead><tr><th>

Criteria

</th><th>

Description

</th><th>

Type

</th><th>

Applies to \[Table\]

</th></tr></thead><tbody><tr><td>

Agents with most parts

</td><td>

Identify agents with the most number of required parts using dynamic scheduling.

</td><td>

Scripted

</td><td>

Task

</td></tr><tr><td>

Assigned Cases

</td><td>

Calculates the workload based on all the assigned cases \(all priorities P1, P2, P3, etc.\). The agent's overall rank decreases with more assigned cases. The more cases assigned, the lower the contribution to the agent's overall rank.

</td><td>

Aggregate

</td><td>

sn\_customerservice\_case

</td></tr><tr><td>

Availability Today

</td><td>

Determines availability based on the schedule, overlap timezone, and current time. Availability is calculated based on the agent's work schedule, and personal time off. The more availability an agent has, the higher the contribution to the agent's overall rank.

</td><td>

Scripted

</td><td>

Task

</td></tr><tr><td>

Consistent Assignment for SM tasks

</td><td>

Assigns work order tasks with the same parent work order to the same agent. Ensures assignment consistency across all matching agents.

</td><td>

Scripted

</td><td>

sm\_task

</td></tr><tr><td>

Current Distance From Task

</td><td>

Considers an agents distance from the task location.

</td><td>

Scripted

</td><td>

Task

</td></tr><tr><td>

Distance from Task

</td><td>

Evaluates the agent's distance from the task location.

</td><td>

Scripted

</td><td>

Task

</td></tr><tr><td>

Distance from task with radius exclusion

</td><td>

Ranks agents based on the nearest location to perform the job, excluding those outside the defined radius.

</td><td>

Scripted

</td><td>

Task

</td></tr><tr><td>

Filter out off-shift agents

</td><td>

Excludes agents who are not available based on schedule or having time-off events.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Ignore Excluded Technician

</td><td>

Prevents automatic assignment of excluded technicians to work order tasks associated with specific accounts. Excluded technicians won’t be assigned if the work order task is associated to an Account for which the technician has been excluded.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Ignore Rejected Technician

</td><td>

Avoids reassignment of tasks to technicians who have recently rejected the same task. The system property work.management.rejected.technician.duration determines the time period from when a technician rejected a task to when that task can be automatically reassigned to the same technician.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Last Assigned

</td><td>

Prioritizes agents based on their most recently assigned work to balance the workload. For the sake of balancing assigned work, prioritized the agent based on the last assigned work.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Matching Mandatory Parts For Dynamic Scheduling

</td><td>

Assigning only the agents with the mandatory parts. Ranks agents based on the availability of mandatory parts required for the job.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Matching Mandatory Skills For Dynamic Scheduling

</td><td>

Ranks agents based on the availability of mandatory skills and optional skills defined in Task Skills that are required for the task. The more skills that match, the higher the contribution to the agent's overall rank.**Note:** If using the mandatory skills feature, use the **Matching Skills - Mandatory Skills Support** criterion to match agents with the [mandatory skills](../../customer-service-management/concept/configure-mandatory-skills-feature.md) identified for a case.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Matching Skills

</td><td>

Evaluates availability based on the skills matching the task requirements. The agent's rank increases with more matching skills.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Matching Skills Level Gap For Dynamic Scheduling

</td><td>

Ranks agents based on the number of skills and skill levels, using the "less is better" method. Prioritize agents with the sufficient skill level over agents that are over-skilled for the task.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Prioritize Preferred Technicians

</td><td>

Assigns tasks based on technicians who are most preferred for working on a customer account.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Radius Exclusion

</td><td>

Ranks agents based on the defined radius, excluding those outside the radius.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Rank Preferred Technicians

</td><td>

Identifies technicians who are most preferred for working on a customer account using dynamic scheduling.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Timezone Overlap

</td><td>

Ranks agents based on their timezone overlap with the task location.

</td><td>

Scripted

</td><td>

task

</td></tr><tr><td>

Matching mandatory crew skills for dynamic scheduling**Note:** Needs Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) to be activated.

</td><td>

Match mandatory skills for a crew task to crews with agents that have those skills.

</td><td>

Scripted

</td><td>

wm\_crew

</td></tr><tr><td>

Crew skill level gap for dynamic scheduling**Note:** Needs Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) to be activated.

</td><td>

Match mandatory skill levels for a crew task, to crews with agents that have skills at the required level.

</td><td>

Scripted

</td><td>

wm\_crew

</td></tr><tr><td>

Crew Matching Skills**Note:** Needs Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) to be activated.

</td><td>

Match crews with the skills listed in the work order task, and assign the task to that crew.

</td><td>

Scripted

</td><td>

wm\_crew

</td></tr><tr><td>

Matching crew skills for task resource requirements**Note:** Needs Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) to be activated.

</td><td>

Match crews with the skills listed in the resource requirements, and assign the task with those resource requirements to that crew.

</td><td>

Scripted

</td><td>

wm\_crew

</td></tr><tr><td>

Crew Distance from Task**Note:** Needs Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) to be activated.

</td><td>

Evaluates the crew's distance from the task location.

</td><td>

Scripted

</td><td>

wm\_crew

</td></tr><tr><td>

Matching Agent Efficiency Criteria for Dynamic Scheduling**Note:** Needs Field Service Agent Efficiency plugin \(com.snc.fsm\_agent\_efficiency\) to be activated.

</td><td>

Assigns a work order task to an agent by matching the Agent Efficiency criteria specified in the work order task with the agent's efficiency criteria.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr></tbody>
</table>As part of selecting the matching criteria, you can specify the following settings for each individual criterion:

-   ranking and display usage
-   ranking method
-   ranking weight
-   threshold
-   active/inactive

#### Ranking and display usage

In the **Use for** field, specify how you want that matching criterion to be used:

-   Ranking and display: uses the criterion to determine agent ranking and displays it in a column on the workbench.
-   Display only: displays the criterion in a column on the workbench but does not use it to determine agent ranking.
-   Ranking only: uses the criterion to determine agent ranking but does not display it on the workbench.

#### Ranking method

There are two ranking methods:

-   More is better: for example, more availability is better when determining the agent ranking.
-   Less is better: for example, fewer assigned cases are better when determining agent ranking.

#### Weight

Each matching criterion has an assigned weight. By default, the matching criteria in the **Recommendation for Case Assignment** matching rule have an assigned weight of 10. You can assign a higher weight to the criteria that are more important.

#### Threshold

A threshold sets a minimum requirement for a criterion. For example, set the threshold of the Matching Skills criterion to 3 if you want to see only those agents who have at least three of the required skills for a task. For availability, set the threshold to the desired number of hours to display only those agents who have that minimum number of work hours available. You can set the threshold in the **Select Criteria** related list on the Matching Rule form. If necessary, personalize the list and add the **Threshold** column.

#### Active/Inactive

There can be several matching criteria associated with the matching rule that determines the assignment workbench configuration. Each individual criterion can be set to active or inactive. Changing this setting has an immediate impact on the agent ranking. You can make this change in the **Select Criteria** related list on the Matching Rule form. If necessary, personalize the list and add the **Active** column.

#### Calculating the agent ranking

Dynamic Scheduling adds the values of the matching criteria and their respective weights and uses these values to determine the overall agent ranking.

1.  Calculate a number for each criterion.
2.  Multiply that number by the criterion weight.
3.  Divide the result by the total of all criterion.
4.  Repeat for each criterion and add the results.

The following example shows how the ranking is determined for an agent with these matching criteria values:

-   Matching Skills with Mandatory Skills Support: 5/6
-   Availability Today: 7 hours
-   Assigned Cases: 2

Calculations:

-   **Matching Skills**: `2 / 3 = 0.666` \(with 3 being the maximum number of skills\)
-   **Availability Today**: `7 / 8 = 0.875` \(with 8 being the maximum number of hours\)
-   **Assigned Cases**: `2 / 26 = 0.0769` \(with 26 being the total number of tasks in the table\)
-   **Weight**: each matching criteria has an equal weight of 10

```
((0.666 x 10) / Total of criterion weight (10+10+10)) + ((0.875 x 10) / Total of criterion weight (10+10+10)) + ((0.0769 x 10) / Total of criterion weight (10+10+10))
```

```
(6.66 / 30) + (8.75 / 30) + (0.769 / 30)
```

```
0.222 + 0.291 + 0.0256 = 0.53
```

This calculation is performed for each agent in the assignment group. Agents are ranked based on the value of this calculation, with the highest number earning the highest ranking.

## Create a task ordering rule

Dynamic scheduling uses task ordering rules to prioritize and arrange tasks effectively. These rules ensure tasks are handled in the right sequence, helping you streamline field service operations.

### Before you begin

Role required: admin

### About this task

Task ordering rules let you control how tasks are prioritized during scheduling. By defining rules, you can ensure that the most critical tasks are handled first, and tasks are ordered based on your organization’s specific needs. Multiple rules can be created and applied in sequence, based on execution order, to give you maximum flexibility and precision.

How task ordering rules work:

-   Execution order: Rules are evaluated in order, with the rule having the lowest execution value taking precedence.
    -   For instance, you might create a rule that prioritizes tasks by urgency \(P1, P2, P3\).
    -   Another rule can be applied to organize tasks with the same priority by their SLA due date.
-   Task dependencies: Task dependencies can override task ordering rules to ensure proper task flow.

    -   If a predecessor task gets reassigned and a successor task is assigned, the predecessor task is scheduled before the successor task starts.
    -   If a predecessor task is unassigned, the successor task remains unassigned.
    -   If a predecessor task is assigned, the successor task waits until the predecessor task is completed.
    -   If a predecessor task has a lower priority, the successor task waits until the predecessor task is assigned.
    **Note:**

    Dynamic scheduling only supports Finish to Start advanced task dependency with no maximum or minimum lag time. Other types of task dependencies will be ignored.


Types of task ordering rules:

-   **Simple rule**
    -   Sorts tasks based on one selected field from the task table.
    -   Choose either ascending or descending sort order.
-   **Advanced rule**
    -   Sorts tasks based on selections from two unrelated tables.
    -   Requires a reference field to connect the task table and another table. For example, you can sort work order tasks based on SLAs stored in the Task SLA table.

Priority based ordering rules: Dynamic scheduling provides two priority based ordering rules.

-   Work order task priority: Uses the task's priority to determine task order, with a default execution order of 100.
-   Work order priority: Uses the overall work order's priority to determine task order, with a default execution order of 200.

**Note:** By default, task ordering rules are ignored during scheduling to prevent potential performance issues. If the number of tasks returned from the task filter condition is very large, applying task ordering could result in significant delays. You can manually enable task ordering rules if the task volumes will not impact performance.

Real-world use cases:

-   Healthcare: Prioritize equipment maintenance tasks based on the criticality of medical devices.
-   Manufacturing: Sort tasks by the cost of machine downtime per hour to reduce impact on production.
-   Retail: Use advanced rules to prioritize tasks by footfall, ensuring high-traffic stores are serviced first.
-   Utilities: Simple rules can prioritize emergency tasks, like power outages affecting critical infrastructure.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  In the **Task Ordering Rules** related list, click **New**.

3.  Fill in the fields on the Task Ordering Rule form, as necessary.

    |Field|Description|
    |-----|-----------|
    |Name|The task ordering rule name.|
    |Execution Order|Specify the order in which this rule should be evaluated. The rule with the lowest value will determine the initial task order.|
    |Dynamic Scheduling Config|Select the dynamic scheduling configuration to which this ordering rule applies.|
    |Advanced|Select to create an advanced task ordering rule from different tables.|
    |Sort Table|Choose the table containing the tasks to be sorted.|
    |Sort Field|Select the field that will determine the task order.|
    |Sort Order|Choose ascending \(A-Z\) or descending \(Z-A\) order.|
    |Task Field|Specify the field on which the tasks will be sorted.|
    |Task Table|For an advanced ordering rule, this field displays the table that contains the tasks to be sorted.|
    |Connecting Task Field|For advanced rules, select the field that links the tables together.|
    |Aggregate Function|For advanced rules, choose an aggregate function like MIN, MAX, COUNT, etc.|

4.  Click **Submit**.

    The task ordering rule is created.


### Result

Dynamic scheduling will use this rule to prioritize tasks based on the criteria you’ve defined, ensuring that high-priority tasks are scheduled appropriately.

### What to do next

[Create a task unassignment constraint](create-dynamic-scheduling-config.md#)

## Create a task unassignment constraint

Dynamic scheduling allows you to define unassignment constraints that prevent certain tasks from being unassigned, even when lower in priority. This feature ensures that critical tasks stay assigned, based on dependencies or urgency.

### Before you begin

Role required: admin

### About this task

Unassignment constraints help control when tasks can or cannot be unassigned, ensuring that essential tasks remain assigned. This prevents disruptions, especially when tasks have dependencies or are time-sensitive. For example, a task nearing its SLA breach or one that requires sourced parts should not be unassigned, regardless of its relative priority in the task ordering rules.

Dynamic scheduling offers three predefined unassignment constraints:

1.  Task with downstream: Prevents unassignment if the task has downstream tasks that depend on it.
2.  Would breach SLA in the next 5 hours: Prevents unassignment if the task's Service Level Agreement \(SLA\) is expiring within five hours.
3.  Part sourced: Prevents unassignment if one or more parts required for the task have already been sourced.

Enabling the unassignment option in Dynamic Scheduling configuration allows the system to unassign tasks in favor of more important tasks \(as determined by task ordering rules\). However, unassignment constraints can prevent specific tasks from being unassigned, even if the task is of lower priority. If a task is unassigned and has downstream tasks, the downstream tasks are also unassigned and added to the pending dispatch queue.

Real-world use cases:

-   Healthcare: Prevent unassignment of critical medical equipment maintenance tasks nearing an SLA breach.
-   Manufacturing: Block unassignment of tasks that have sourced parts, ensuring resources are used efficiently.
-   Utilities: Keep emergency repair tasks assigned when downstream dependencies are involved.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  In the **Un-Assignment Constraints** related list, click **New**.

3.  Click the lookup icon next to the **Constraint** field.

4.  In the Constraints list, click **New**.

5.  Fill in the fields on the Constraint form, as necessary.

<table id="table_gau_hat_ii"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The constraint name.

</td></tr><tr><td>

Task Table

</td><td>

Select the task table to which this constraint applies.

</td></tr><tr><td>

Type

</td><td>

Choose the type of constraint.-   **Simple**: define a simple constraint by selecting a table, a task field, and one or more filter conditions.
-   **Advanced**: define an advanced constraint by creating a script.


</td></tr><tr><td>

Constraint Table

</td><td>

Specify the table used to define the constraint on a task.

</td></tr><tr><td>

Task Field

</td><td>

Select the task field to which this constraint applies.

</td></tr><tr><td>

Constraint Condition

</td><td>

When this condition is true, it prevents task reassignment or unassignment.

</td></tr><tr><td>

Constraint Script

</td><td>

If using an advanced constraint, create a script to define the constraint details.

</td></tr></tbody>
</table>6.  Click **Submit**.

    The constraint is saved and returns you to the Un-Assignment Constraint form.

7.  Click **Submit**.

    The constraint is active and added to the configuration in the **Un-Assignment Constraints** related list.


### Result

This constraint will prevent task unassignment based on the specified conditions, ensuring that tasks are not unassigned even if they have lower importance according to the task ordering rules.

