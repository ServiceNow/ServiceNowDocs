---
title: Associate a task plan template to a work schedule
description: Map a single or multiple task plan templates to a planned work schedule. Add conditions to identify the relevant templates for the planned work records.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-11-12"
reading_time_minutes: 1
breadcrumb: [Work plans, Planned Work Management, Work orders and tasks, Configure, Field Service Management]
---

# Associate a task plan template to a work schedule

Map a single or multiple task plan templates to a planned work schedule. Add conditions to identify the relevant templates for the planned work records.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

If you set the template type of a work plan to Task plan template, you can link its planned work schedules with task plan templates. For more information, see [Create a work plan](create-work-plan.md).

When the conditions specified in the planned work schedule template are met, tasks, cases, or incidents are created based on the defined task plan templates.

For example, to meet the monthly audit requirement of inspecting multiple stores of the same organization simultaneously, you need to create individual planned work schedules for each audit. Link each schedule to a different task plan template. Include relevant conditions in each planned work schedule template to ensure the correct template is applied when generating tasks specific to each audit.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open a plan from the list of work plans.

3.  In the Planned Work Schedules related list, select a schedule to which you want to associate a task template.

4.  In the Planned Work Schedule Task Templates related list, select **New**.

5.  On the form, fill in the fields.

<table id="table_vxv_csf_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template

</td><td>

Task plan template to be associated with the planned work schedule. For more information on the creation and usage of task plans, see [Task Plan Templates](https://www.servicenow.com/docs/access?context=task-plan-templates&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

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

Filter conditions to determine the task plan template to be used to tasks based on the planned schedule.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

Task plan templates are linked to schedules, and when generating tasks for a specific work plan, the corresponding template is used.

