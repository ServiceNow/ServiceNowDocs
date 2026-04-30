---
title: Override capacity assignment for a changed work schedule
description: Change the default capacity assignment rules for any change in plan within a capacity definition. So that you can update the capacity assignments for the existing capacity definition rule at different time intervals and for different capacity buckets rather than creating a new capacity definition.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Override capacity assignment for a changed work schedule

Change the default capacity assignment rules for any change in plan within a capacity definition. So that you can update the capacity assignments for the existing capacity definition rule at different time intervals and for different capacity buckets rather than creating a new capacity definition.

## Before you begin

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Assignments**.

2.  Open a Capacity Definition from the list.

3.  Open the capacity assignment of a group by clicking the **Effective from** date link for a capacity definition group.

    For example, click the **Effective from** date link in the row of **NorCal Technicians** group.

4.  In the Capacity Assignment Overrides related list, click **New**.

5.  On the form, fill the fields.

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

This field is populated based on the value mentioned in the Repeat for field.

</td></tr><tr><td>

Repeat for

</td><td>

Number of days or hours for which the overridden capacity assignment is applicable to the work group. The frequency mentioned in the capacity definitions is taken into account while assigning the workload capacity.

</td></tr><tr><td>

Capacity Assignment

</td><td>

Name of capacity assignment to be overridden.This field is auto-populated based on the capacity definition for which the capacity assignment is to be modified. For example, Norcal technicians capacity.

</td></tr><tr><td>

Overridden capacity value

</td><td>

Number of days or hours to override the existing Value to be overridden for capacity assignment. This value is measured based on the selected frequency in the capacity definition.

</td></tr><tr><td>

Apply for all buckets

</td><td>

An option to override the capacity assignment rule for all the capacity buckets of the selected capacity definition.

</td></tr><tr><td>

Applicable to bucket

</td><td>

Name of the capacity bucket that needs to be overridden with the changed capacity assignment rule.

</td></tr></tbody>
</table>6.  Click **Submit**.


## Result

The capacity assignment overrides is created and applied to the capacity buckets of selected capacity definition.

