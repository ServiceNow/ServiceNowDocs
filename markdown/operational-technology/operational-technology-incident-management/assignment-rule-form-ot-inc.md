---
title: Assignment rule form
description: Assignment rules automatically assign an Operational Technology \(OT\) incident to a group or user according to one or more conditions in the assignment rule.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Incident Management, Operational Technology]
---

# Assignment rule form

Assignment rules automatically assign an Operational Technology \(OT\) incident to a group or user according to one or more conditions in the assignment rule.

The following table describes the field values for the Assignment rule form.

<table id="table_avd_2sh_fq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the assignment rule.

</td></tr><tr><td>

Active

</td><td>

Option to activate the assignment rule.

</td></tr><tr><td class="sub-head" colspan="2">

Applies to

</td></tr><tr><td>

Table

</td><td>

Table with the records that the assignment rule applies to.

**Note:** For assignment rules that are specific to OT incidents, set the Table field to **Operational Technology Incident \[sn\_ot\_incident\]**.

 The list shows only the tables and database views that are in the same scope as the assignment rule. If you select a custom table that extends the task table and to make sure that the assignment rule works properly, you must clear the instance cache by navigating to https://&lt;instance\_name&gt;.service-now.com/cache.do.

 **Important:** Clearing the system cache can affect the overall performance and may degrade the system response times. Don’t run cache flushes during business hours, and don’t trigger cache flushes to run automatically.

</td></tr><tr><td>

Conditions

</td><td>

Conditions under which the assignment rule applies.

</td></tr><tr><td class="sub-head" colspan="2">

Assign to

</td></tr><tr><td>

User

</td><td>

User that the event is assigned to.

</td></tr><tr><td>

Group

</td><td>

Group that the event is assigned to.

</td></tr><tr><td class="sub-head" colspan="2">

Script

</td></tr><tr><td>

Script

</td><td>

Script to specify the advanced assignment rule functionality. The current.variable\_pool set of variables is available.**Note:** Make sure that the input in the script is correct and that the input type matches the field type in the Assignment Rule script. For example, if the assignment rule script sets the value of an Integer field, and the value in the script is set to String, the assignment rule may yield unexpected results.

</td></tr><tr><td class="sub-head" colspan="2">

Optional fields

</td></tr><tr><td>

Match conditions

</td><td>

-   **Any**

If any of the conditions are met, the assignment rule applies.

-   **All**

If all the conditions are met, the assignment rule applies.


</td></tr><tr><td>

Execution Order

</td><td>

Order in which the assignment rule is processed. If the assignment rules conflict, a rule with a lower-order value takes precedence over a rule with a higher value. If the order values are set to the same number, the assignment rule with the first matching condition takes precedence over the others without the first matching condition. Only the first assignment rule with a matching condition runs against a record.

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Incident Management reference](oper-tech-incident-management-reference.md)

