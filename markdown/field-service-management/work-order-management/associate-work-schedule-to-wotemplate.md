---
title: Associate a work order template to a work schedule
description: Map a single or multiple work order templates to a planned work schedule. Add conditions to identify the relevant templates for the planned work records.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring work plans, Configuring Planned Work Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Associate a work order template to a work schedule

Map a single or multiple work order templates to a planned work schedule. Add conditions to identify the relevant templates for the planned work records.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin and model\_manager

## About this task

For example, to fulfill the maintenance requirement of two MRI machines from different brands, at the same time. You must create a schedule for these machines and then map it to different work order templates. Add conditions so that the schedule can identify the appropriate template to generate work orders that are specific to each MRI machine.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open a plan from the list of work plans.

3.  In the Planned Work Schedules related list, select a schedule to which you want to associate a work order template.

4.  In the Planned Work Schedule Templates related list, select **New**.

5.  On the form, fill in the fields.

<table id="table_vxv_csf_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Work order template to be associated with the planned work schedule.

</td></tr><tr><td>

Schedule

</td><td>

Planned work schedule to which you’re adding the template.This field is automatically set to the selected planned work schedule.

</td></tr><tr><td>

Table

</td><td>

Table that is associated with the corresponding work plan of this planned schedule.This field is automatically set to the table name selected for the work plan.

</td></tr><tr><td>

Condition

</td><td>

Filter conditions to determine the work order template to be used to create work orders based on the planned schedule.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

Work orders created by the scheduled jobs running on the associated work schedule contain the selected template.

