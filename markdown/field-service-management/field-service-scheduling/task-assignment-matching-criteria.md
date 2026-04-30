---
title: Matching criteria for task filters
description: The Dynamic Scheduling uses matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Create a task filter for dynamic scheduling, Configure dynamic scheduling, Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Matching criteria for task filters

The Dynamic Scheduling uses matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.

Matching criterion is used by other ServiceNow applications. For example, the 'Assigned Cases' matching criteria applies to the Case \[sn\_customerservice\_case\] table and is used by Customer Service Management \(CSM\). Any criterion can be copied, renamed, and configured for use against other tables, such as the work order task table. Be sure to test any configuration changes thoroughly. There are three types of matching criteria:

-   Simple Match: Creates one-to-one matching, such as matching the time zone of an agent with the time zone of a task location.
-   Aggregate: Uses a simple query and returns an aggregate result. For an aggregate type, select a table and create a filter, and then select an aggregate field such as the **Assigned to** field. This type of query returns a set of users.
-   Scripted: Uses a scripted query which returns a list of users.

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

Calculates the workload based on all the assigned cases \(all priorities P1, P2, P3, and so on\). The agent's overall rank decreases with more assigned cases. The more cases assigned, the lower the contribution to the agent's overall rank.

</td><td>

Aggregate

</td><td>

sn\_customerservice\_case

</td></tr><tr><td>

Availability Today

</td><td>

Determines availability based on the schedule, overlap time zone, and current time. Availability is calculated based on the agent's work schedule, and personal time off. The more availability that an agent has, the higher the contribution to the agent's overall rank.

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

Excludes agents who aren’t available based on schedule or having time-off events.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Ignore Excluded Technician

</td><td>

Prevents automatic assignment of excluded technicians to work order tasks associated with specific accounts. Excluded technicians aren't assigned if the work order task is associated with an Account for which the technician has been excluded.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Ignore Rejected Technician

</td><td>

Avoids reassignment of tasks to technicians who have recently rejected the same task. The system property `work.management.rejected.technician.duration` determines the time period from when a technician rejects a task until it can be automatically reassigned to the same technician.

</td><td>

Scripted

</td><td>

wm\_task

</td></tr><tr><td>

Last Assigned

</td><td>

Prioritizes agents based on their most recently assigned work to balance the workload. For the sake of balancing assigned work, prioritizes the agent based on the last assigned work.

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

Ranks agents based on their time zone overlap with the task location.

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

Match mandatory skill levels for a crew task to crews with agents that have skills at the required level.

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

</td></tr></tbody>
</table>## Configuring matching criteria for Dynamic Scheduling

When selecting the matching criteria, you can configure individual fields for each criterion using the Personalize List Columns icon. Here are a few fields that you can adjust:

-   **Ranking and display usage**

    In the **Use for** field, specify how you want that matching criterion to be used:

    -   Ranking and display: Uses the criterion to determine agent ranking and displays it in a column on the workbench.
    -   Display only: Displays the criterion in a column on the workbench but doesn’t use it to determine agent ranking.
    -   Ranking only: Uses the criterion to determine agent ranking but doesn’t display it on the workbench.
-   **Ranking method**

    There are two ranking methods:

    -   More is better: For example, more availability is better when determining the agent ranking.
    -   Less is better: For example, fewer assigned cases are better when determining agent ranking.
-   **Weight**

    Each matching criterion has an assigned weight. By default, the matching criteria in the **Recommendation for Case Assignment** matching rule have an assigned weight of 10. You can assign a higher weight to the criteria that are more important.

-   **Threshold**

    A threshold sets a minimum requirement for a criterion. For example, set the threshold of the Matching Skills criterion to 3 if you want to see only those agents who have at least three of the required skills for a task. For availability, set the threshold to the desired number of hours to display only those agents who have that minimum number of work hours available. You can set the threshold in the **Select Criteria** related list on the Matching Rule form. If necessary, personalize the list and add the **Threshold** column.

-   **Active/Inactive**

    There can be several matching criteria associated with the matching rule that determines the assignment workbench configuration. Each individual criterion can be set to active or inactive. Changing this setting has an immediate impact on the agent ranking. You can make this change in the **Select Criteria** related list on the Matching Rule form. If necessary, personalize the list and add the **Active** column.

-   **Calculating the agent ranking**

    Dynamic Scheduling adds the values of the matching criteria and their respective weights and uses these values to determine the overall agent ranking.

    1.  Calculate a number for each criterion.
    2.  Multiply that number by the criterion weight.
    3.  Divide the result by the total of all criterion.
    4.  Repeat for each criterion and add the results.

## Calculate agent rank

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

