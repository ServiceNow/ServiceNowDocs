---
title: Create a capacity assignment override
description: Override the default capacity assignment rules to accommodate changes in the plan within a capacity definition. This allows you to update existing capacity assignments for different time intervals, capacity reservation rules, and recurring patterns without creating a new capacity definition.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create a capacity assignment override

Override the default capacity assignment rules to accommodate changes in the plan within a capacity definition. This allows you to update existing capacity assignments for different time intervals, capacity reservation rules, and recurring patterns without creating a new capacity definition.

## Before you begin

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager

## About this task

Consider the following points:

-   The highest ranked override record is considered when there is conflict in the date range.
-   Overrides must not conflict with existing recurrence plans for the same capacity definition.
-   Overrides must adhere to the base recurrence plan of the capacity assignment. For example: if the base recurrence plan is "Monday to Friday," an override for "Saturday" will trigger a validation error.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Assignments**.

2.  Open the capacity definition.

    1.  Select a capacity definition from the list.

    2.  Open the capacity assignment of a group by clicking the **Effective from** date link for a capacity definition group.

        For example, click the **Effective from** date link in the row of **NorCal Technicians** group.

3.  In the Capacity Assignment Overrides related list, click **New**.

4.  On the form, fill the fields.

<table id="table_r5s_fcv_rtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Effective from

</td><td>

Date from which the capacity assignment should be applied.

</td></tr><tr><td>

Effective to

</td><td>

Automatically populated based on the value in the **Repeat For** field.

</td></tr><tr><td>

Recurrence

</td><td>

Select any existing recurrence plan. Recurrence plans can be customized for specific territories, groups, or tasks. This plan defines how often a capacity assignment repeats. It helps create a regular schedule for task allocation. For example:-   Assign tasks every weekday \(Monday to Friday\)
-   Allocate installation type tasks every weekend \(Saturday and Sunday\)
-   Set up capacity for the first Monday of every month


</td></tr><tr><td>

Override by

</td><td>

Select the type of override. For example, capacity reservation, capacity value, or capacity definition.

</td></tr><tr><td>

Repeat for

</td><td>

Number of days, weeks, months, or years the override will remain active. Recurrence frequency is taken into account while assigning workloads.

</td></tr><tr><td>

Capacity Reservation

</td><td>

Name of the capacity reservation to be overridden.

</td></tr><tr><td>

Overridden capacity value

</td><td>

Number of hours or tasks to override in the existing capacity assignment. This value is determined by the selected frequency in the capacity definition.

</td></tr><tr><td>

Apply for all buckets

</td><td>

Enable this option to override capacity assignment rules for all capacity buckets within the selected capacity definition.

</td></tr><tr><td>

Applicable to bucket

</td><td>

Specify the name of the capacity bucket where the override rule will apply.

</td></tr><tr><td>

Rank

</td><td>

Determines the sequence to pick. The highest ranked override record of the given day is preferred.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The capacity assignment override record is created and applied to the selected capacity definition or buckets of selected capacity definition.

