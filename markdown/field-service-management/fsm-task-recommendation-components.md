---
title: Intelligent Task Recommendations components
description: Several types of components are installed with the Intelligent Task Recommendations components feature, including tables and business rules.Intelligent Task Recommendations uses the following properties.There are two types of recommendation criteria, filter constraints and ranking criteria. The system provides a set of predefined criteria.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Intelligent Task Recommendations components

Several types of components are installed with the Intelligent Task Recommendations components feature, including tables and business rules.

Intelligent Task Recommendations adds the Task Recommendations Administration menu to the application navigator. The feature adds the following modules:

-   Task Recommendation Policies
-   Task Recommendation Applicabilities
-   Recommendation Criteria
-   Task Recommendation Properties

## Tables

Field Service Management Intelligent Task Recommendations adds the following tables.

<table id="table_dv4_3wc_xpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Recommendation Policy Related Criteria \[task\_rec\_m2m\_recommend\_policy\_criteria\]

</td><td>

Stores the related criteria records for task recommendation policies.

</td></tr><tr><td>

Task Recommendation Applicability\[task\_rec\_recommendation\_applicability\]

</td><td>

Stores the application records along with their default task recommendation policies.

</td></tr><tr><td>

Recommendation Criteria\[task\_rec\_recommendation\_criteria\]

</td><td>

Stores the task recommendation criteria records.

</td></tr><tr><td>

Task Recommendation Policy\[task\_rec\_recommendation\_policy\]

</td><td>

Stores the task recommendation policy records.

</td></tr></tbody>
</table>## Business Rules

Field Service Management Intelligent Task Recommendations adds the following business rules.

<table id="table_exh_y1d_xpb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Validate order and weight

</td><td>

Task Recommendation Policy Related Criteria\[task\_rec\_m2m\_recommend\_policy\_criteria\]

</td><td>

Ensures the order of filter constraints and the weight and order of ranking criteria for a task recommendation policy. This value must be a positive integer number.

</td></tr><tr><td>

Validate table for policy and criteria

</td><td>

Task Recommendation Policy Related Criteria\[task\_rec\_m2m\_recommend\_policy\_criteria\]

</td><td>

Validates that the same tables are selected in the **Prefetched table** field of a recommendation criteria and in the **Table** field of a task recommendation policy.

</td></tr><tr><td>

Validate delete of recommendation policy

</td><td>

Task Recommendation Policy \[task\_rec\_recommendation\_policy\]

</td><td>

Prevents the deletion of a policy if the policy is specified in the **Default task recommendation policy** field of the Task Recommendation Applicability form.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

## Intelligent Task Recommendations system properties

Intelligent Task Recommendations uses the following properties.

These properties are located at **Field Service** &gt; **Task Recommendations Administration** &gt; **Task Recommendation Properties**.

<table id="table_yyy_wdd_xpb"><thead><tr><th>

Property

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

sn\_task\_recommend.max\_return\_tasks

</td><td>

Sets the maximum number of tasks to be returned to the dispatcher.-   Type: Integer
-   Default value: **5**

</td></tr><tr><td>

sn\_fsm\_task\_rec.task\_recomm\_geo\_routing\_travel\_calculation\_method

</td><td>

Uses Google Maps API, Beans.AI, or straight-line estimates to calculate the estimated agent travel time. Calculates the distance to task locations based on the route taken by the agent. -   Type: Choice list
-   Default value: Use Google Maps API

</td></tr><tr><td>

sn\_fsm\_task\_rec.task\_recomm\_use\_geo\_history

</td><td>

Enables the system to look up the agent location using the geo history table.-   Type: true/false
-   Default value: **true**

</td></tr><tr><td>

sn\_task\_recommend.logging\_level

</td><td>

Controls the logging level displayed for Field Service Management while recommending tasks.-   Type: Choice list
-   Default value: **Error**

</td></tr></tbody>
</table>## Predefined recommendation criteria

There are two types of recommendation criteria, filter constraints and ranking criteria. The system provides a set of predefined criteria.

### Recommendation criteria

The following are a few built-in recommendation criteria for Intelligent Task Recommendation. When configuring intelligent task recommendation settings, you can use one or more of these criteria in your task recommendation policies.

<table id="table_vht_tvc_cqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Exclude rejected technicians

</td><td>

Filters tasks that have been rejected by the agents in the specified time period. The default value is 24 hours.

 You can configure the time value using the **work.management.rejected.technician.duration** property.

</td></tr><tr><td>

Exclude tasks agent cannot travel to

</td><td>

Filters out tasks that the agent cannot travel to in the selected time window.

</td></tr><tr><td>

Must have mandatory parts

</td><td>

Filters out tasks for which the defined mandatory parts are not available with the agent.

</td></tr><tr><td>

Must have mandatory skills

</td><td>

Filters out tasks for which the defined mandatory skills are not possessed by the agent.

</td></tr><tr><td>

Filter Tasks on Agent Efficiency Criteria

</td><td>

Filters out the tasks that match with the agent's efficiency.**Note:** Requires the activation of the Field Service Agent Efficiency plugin \(com.snc.fsm\_agent\_efficiency\).

</td></tr></tbody>
</table><table id="table_lwz_mnc_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Distance from task

</td><td>

Rates tasks based on the travel distance. Rates whether the time needed by an agent to travel from the agent's current location to the task location is within the selected time window.

</td></tr><tr><td>

Matching parts

</td><td>

Rates tasks based on whether the agent has the matching parts required to complete the task.Mandatory parts are not honored in the ranking criteria. To filter out tasks for which the agent does not have the mandatory parts, you must add the **Must have mandatory parts** **** filter constraint.

</td></tr><tr><td>

Matching skills

</td><td>

Rates tasks based on whether the agent has the skills required to complete the task.Mandatory skills are not honored in the ranking criteria. To filter out tasks for which the agent does not have the mandatory skills, you must add the **Must have mandatory skills** filter constraint.

</td></tr><tr><td>

Rank Tasks On Agent Efficiency Criteria

</td><td>

Ranks the tasks that are pending to be dispatched, based on the Agent Efficiency Criteria.**Note:** Requires the activation of the Field Service Agent Efficiency plugin \(com.snc.fsm\_agent\_efficiency\).

</td></tr></tbody>
</table>