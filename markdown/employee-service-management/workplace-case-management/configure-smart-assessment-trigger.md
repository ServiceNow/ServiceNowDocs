---
title: Configure Smart Assessment Trigger
description: Smart assessment triggers define the conditions when assessment templates are applied to workplace cases or tasks.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-01-28"
reading_time_minutes: 1
breadcrumb: [Smart Assessment for Workplace Case and Task, Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Smart Assessment Trigger

Smart assessment triggers define the conditions when assessment templates are applied to workplace cases or tasks.

## About this task

Smart assessment triggers automatically create assessment instances when specific conditions are met on workplace cases or tasks. Conditions can be based on state changes, field values, or other criteria. You can also specify whether the assessment is mandatory and apply filters to target specific cases.

## Before you begin

Role required: sn\_wsd\_case.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Smart Assessment Triggers**.

2.  On the Workplace Smart Assessment Triggers form, select **New** and fill in the form fields.

<table id="table_izy_zjd_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the smart assessment trigger record.

</td></tr><tr><td>

Description

</td><td>

Summary information about the assessment trigger condition record.

</td></tr><tr><td>

Table

</td><td>

The target table to run the trigger condition on. For example, Workplace case \[sn\_wsd\_case\_workplace\_case\].

</td></tr><tr><td>

Trigger condition

</td><td>

Conditions to set off the trigger:-   Add Filter Condition: Field where the trigger conditions are added.
-   Add OR Clause: Field to add an optional clause for the trigger condition.
For example, if you want to send an assessment whenever an incident closes, create the condition \[State\] \[changes to\] \[Work in Progress\]. These assessments automatically attach to cases and tasks based on configurable trigger conditions.

</td></tr><tr><td>

Mandatory

</td><td>

Check box that determines assessment must be completed before the case can be closed.**Note:** Template must be closed before the case can be moved to one of the states in the **Close before** field.

</td></tr><tr><td>

Close before

</td><td>

Option to specify the case state that cannot be reached until the assessment is closed. For example, if you specify Closed complete, the Workplace Agent cannot close complete the case until the smart assessment instance is closed.

</td></tr></tbody>
</table>3.  Select **Submit**.

    The record is added to the Workplace Smart Assessment Triggers record list.

4.  Open the assessment trigger record and in the **Workplace Smart Assessment Template Mappings** section, select **New**.

5.  In the **Smart assessment template** field, select the published smart assessment template that should be applied when trigger conditions are met.


**Parent Topic:**[Smart Assessment for Workplace Case and Task](smart-assessment-for-workplace-case-and-task.md)

