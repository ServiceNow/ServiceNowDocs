---
title: Create a capacity definition
description: Allocate work to different types of tasks based on the reserved capacity percentage and defined source of capacity for a territory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/workforce-optimization-for-field-service/create-capacity-definitions.html
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# Create a capacity definition

Allocate work to different types of tasks based on the reserved capacity percentage and defined source of capacity for a territory.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_manager, wm\_manager, sn\_fsm\_capacity\_mg.wm\_capacity\_write, sn\_fsm\_tp.fsm\_territory\_planner, wm\_admin, wm\_contractor\_manager\_int

## About this task

You can define capacity and frequency of work to be performed based on the selected source of capacity, such as number of hours, tasks, or agent's schedule. Capacity can be defined for a day, week, month, or an year. The different sources of capacity are:

-   **Aggregated Agent Schedule**: The capacity available each day for task assignments depends on the total available duration of all the agents. When capacity is defined for a reservation rule, the reservation is applied on the total duration of the availability of all the agents. The aggregated agent schedule applies every day until a specified cut-off date or number of days. Beyond the cut-off date or days, when the agent schedule information is unavailable, the defined capacity applies, and tasks are assigned as per the predicted capacity.

    **Note:**

    The **Aggregated Agent Schedule** doesn’t apply on the day when capacity is defined \(Day 0\). It always applies from the following day \(Day 1\) after the capacity is defined until the cut-off day or date.

    For example, 10 agents available for 10 hours each day provides 100 hours of total capacity per day until the cut-off date.

    With a reservation rule that reserves 20% for installation tasks and 60% for break-fix tasks, 20 hours are reserved for installation tasks, 60 hours for break-fix tasks, and the remaining 20 hours for any other tasks.

    Beyond the cut-off date, tasks are assigned based on the defined capacity.

-   **Hours**: The total number of hours per day available in the specified territory, for completing single-day tasks. You can also specify a reservation rule for the capacity definition.

    For example, define the capacity as 10 hours per day with a reservation rule that reserves 40% for break-fix tasks and 30% for installation tasks. A total of 10 hours can be assigned each day: 4 hours for break-fix tasks, 3 hours for installation tasks, and 3 hours for other tasks. When no reservation rule is defined, the full daily capacity is available for any tasks.

-   **Tasks**: The total number of single-day tasks that can be completed each day within a specific territory. You can also specify a reservation rule for the capacity definition.

    For example, if you define the capacity as 10 tasks per day for a reservation rule that reserves 50% of capacity for breakfix tasks, 5 tasks per day are reserved for break-fix tasks, and the other 5 tasks are reserved for any other tasks. When the capacity is not defined for any reservation rule, all the 10 tasks can be assigned to any type of tasks.

-   **Agent Schedule**: The capacity available for task assignments for each day depends on the schedule of the agents available on that day. When you specify reservation rule, the capacity is reserved as per the rule for each agent.

    For example, with 10 agents each having a daily capacity of 10 hours, capacity is reserved based on each agent's schedule. With a reservation rule that reserves 20% for installation tasks and 60% for break-fix tasks, each agent has 2 hours reserved for installation tasks and 6 hours for break-fix tasks. The remaining 2 hours per agent are reserved for any other tasks.

    **Note:**

    New users using Zurich release version, can’t define capacity by **Agent Schedule**.

    For existing users defining capacity by **Agent Schedule**, ServiceNow® recommends transitioning to alternative available methods for defining capacity.


## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Definitions**.

2.  Click **New**.

3.  On the form, fill the fields.

<table id="table_dbt_xqp_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the capacity definition.

</td></tr><tr><td>

Description

</td><td>

A brief information about the capacity definition.

</td></tr><tr><td>

Set capacity by buckets

</td><td>

Option to set work capacity at the bucket level, such as morning, noon, or evening. Appointment slots remain available throughout the day until the capacity is reached.

 -   This option is available only when Tasks or Hours is selected from the **Capacity by** field.
-   This option is available only when Daily is selected from the **Frequency** field.


</td></tr><tr><td>

Capacity by

</td><td>

Source of the capacity definition. Capacity can be defined by the Aggregated Agent Schedule, Tasks, Hours, and Agent Schedule.

</td></tr><tr><td>

Capacity

</td><td>

Capacity of work to be performed, such as the number of tasks or number of hours. This value is based on an agent's per-day capacity.Capacity is applicable only when the capacity is defined by **Tasks** or **Hours**. When capacity is defined by **Aggregated Agent Schedule**, the capacity specified will be the base defined capacity beyond the schedule cut-off date or days.

</td></tr><tr><td>

Frequency

</td><td>

Specific intervals at which the work should be performed, such as daily, weekly, monthly, or yearly. This value is based on the total capacity of the assigned work group.-   Frequency applicable only when capacity is defined by tasks, hours, or aggregated agent schedule.
-   Frequency is automatically set to **Daily** if the capacity is set by buckets or defined by aggregated agent schedule.


</td></tr><tr><td>

Allocation Schedule

</td><td>

The name of the allocation schedule to be associated with the capacity definition. This ensures that the appropriate amount of capacity is allocated for work order tasks up to the last available appointment booking slot.

 This field appears only when the **Set capacity by buckets** option is cleared or when you define capacity by aggregated agent schedule.

</td></tr><tr><td>

Reservation name

</td><td>

Name of the capacity reservation rule that applies to the capacity definition. The available capacity is reserved for various work order tasks as per the reservation rule.This field appears only when the Set capacity by buckets option is cleared. For more information, see [Capacity reservation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/workforce-optimization-for-field-service/capacity-reservations.md).

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The capacity definition is created and the work is allocated to each task attribute based on its reserved capacity.

