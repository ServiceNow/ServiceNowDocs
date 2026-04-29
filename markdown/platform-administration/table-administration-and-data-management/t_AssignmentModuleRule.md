---
title: Create an assignment rule
description: Automatically assign a record according to one or more conditions in an assignment rule. Assignment rules are designed to run at the time you open a record.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assignment rules, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an assignment rule

Automatically assign a record according to one or more conditions in an assignment rule. Assignment rules are designed to run at the time you open a record.

## Before you begin

Role required: assignment\_rule\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Assignment**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_avd_2sh_fq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The descriptive name for the assignment rule.

</td></tr><tr><td>

Active

</td><td>

Option to activate the assignment rule.

</td></tr><tr><td class="sub-head" colspan="2">

Applies to

</td></tr><tr><td>

Table

</td><td>

The table with the records that the assignment rule applies to.

 The list shows only tables and database views that are in the same scope as the assignment rule. If you select a custom table that extends the task table, and for the assignment rule to work properly, you must clear the instance cache by navigating to https://&lt;instance\_name&gt;.service-now.com/cache.do.

 **Important:** Clearing the system cache can affect overall performance, and degrade system response times. Do not run cache flushes during business hours, and do not trigger cache flushes automatically.

</td></tr><tr><td>

Conditions

</td><td>

The conditions under which the assignment rule applies.

</td></tr><tr><td class="sub-head" colspan="2">

Assign to

</td></tr><tr><td>

User

</td><td>

The user the event is assigned to.

</td></tr><tr><td>

Group

</td><td>

The group the event is assigned to.

</td></tr><tr><td class="sub-head" colspan="2">

Script

</td></tr><tr><td>

Script

</td><td>

A script to specify advanced assignment rule functionality. The current.variable\_pool set of variables is available.**Note:** Make sure the input in the script is correct, and that the input type matches the field type in the Assignment Rule script. For example, if the assignment rule script sets the value of an Integer field, and the value in the script is set to String, the assignment rule may yield unexpected results.

</td></tr><tr><td class="sub-head" colspan="2">

Optional fields

</td></tr><tr><td>

Match conditions

</td><td>

-   **Any**

If any of the conditions are met, assignment rule applies.

-   **All**

If all the conditions are met, assignment rule applies.

</td></tr><tr><td>

Execution Order

</td><td>

The order in which the assignment rule is processed. If assignment rules conflict, a rule with a lower-order value takes precedence over a rule with a higher value. If the order values are set to the same number, the assignment rule with the first matching condition takes precedence over the others. Only the first assignment rule with a matching condition runs against a record.

</td></tr></tbody>
</table>
## Condition editor

In this example, the condition statement automatically assigns any incident opened in the Network category to the system administrator in the Network assignment group.

![Applies To](../image/Assignment.png "Applies To")

![Assign To](../image/assignment-assign-to.png "Assign To")

**Parent Topic:**[Defining assignment rules](../concept/c_DefineAssignmentRules.md)

**Related topics**  


[Assignment rules module](../concept/c_AssignmentRulesModule.md)

[Data lookup rules](../concept/c_DataLookupRules.md)

[Precedence between data lookup, assignment, and business rules](../concept/c_PrecBetweenAssignmentAndBusRules.md)

[Workflow assignments](../concept/c_WorkflowAssignments.md)

[Baseline assignment rules example](../reference/r_BaselineAssignmentRulesExample.md)

[Create an assignment data lookup rule](t_DataLookupRule.md)

