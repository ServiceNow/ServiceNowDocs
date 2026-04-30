---
title: Create a capacity assignment
description: Create the capacity assignment of work based on the selected source, such as agent schedules, tasks, or hours.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# Create a capacity assignment

Create the capacity assignment of work based on the selected source, such as agent schedules, tasks, or hours.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_manager, wm\_manager, sn\_fsm\_capacity\_mg.wm\_capacity\_write, sn\_fsm\_tp.fsm\_territory\_planner, wm\_admin, wm\_contractor\_manager\_int

## About this task

Work assignment rules:

-   If work capacity is based on the agent's schedule, tasks are assigned to agents in internal work groups.
-   If work capacity is based on the aggregated agent schedule, number of tasks or hours, tasks can be assigned to agents in both internal and external work groups.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Capacity Management** &gt; **Capacity Assignments**.

2.  Click **New**.

3.  On the form, fill the fields.

4.  <table id="table_cvk_srq_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capacity Definition

</td><td>

Name of the capacity definition based on which the capacity will be assigned. For more information, see [.](../task/create-capacity-definitions.md)

</td></tr><tr><td>

Type

</td><td>

Select the capacity type. -   Territory Internal Agents: Choose to assign work specifically to internal agents within a designated territory.
-   Territory Contractor Group: Choose to assign work to contractor groups within a territory. Ideal for managing external contractor teams within specified territories.
-   None: Select to have the flexibility to choose either assignment groups or contractor groups. When the Territory Planning plugin is installed, choosing "None" directs you to select contractor groups. Without the plugin, it allows you to proceed to the next step of choosing a group facilitating to decide based on your workflow.
**Note:** If the Territory Planning plugin is activated, Territory internal agents and contractor groups options appear in the field.

</td></tr><tr><td>

Group

</td><td>

Internal, external, or both types of work groups based on the source of the capacity definition. **Note:** The capacity definitions created for Agent Schedule can be assigned to internal groups only.

</td></tr><tr><td>

Territory

</td><td>

Select territory for the capacity assignment.**Note:** The **Territory** field appears when the **Territory Planning** plugin is activated.

</td></tr><tr><td>

Recurrence

</td><td>

Select any existing recurrence plan. Recurrence plans can be customized for specific territories or groups. This plan defines how often a capacity assignment repeats. It helps create a regular schedule for task allocation. For example:-   Assign tasks every weekday \(Monday to Friday\)
-   Allocate installation type tasks every weekend \(Saturday and Sunday\)
-   Set up capacity for the first Monday of every month


</td></tr><tr><td>

Active

</td><td>

Option for applying the assignment while calculating the capacity.

</td></tr><tr><td>

Effective from

</td><td>

Define the start date for the capacity assignment.

</td></tr><tr><td>

Effective to

</td><td>

Define the end date for the capacity assignment.This field is automatically set to the **Effective to** date if you enter a value in the **Repeat for** field.

</td></tr><tr><td>

Repeat for

</td><td>

Specify the duration \(e.g., 2 weeks, 3 months\) for which the recurrence is applied. You must consider the capacity definitions while assigning tasks.This field appears only when Tasks is selected in the **Capacity by** field in the Capacity Definitions form.

</td></tr><tr><td>

Time zone

</td><td>

Select the appropriate time zone for agents to ensure consistency across regions.

</td></tr></tbody>
</table>5.  Click **Submit**.


