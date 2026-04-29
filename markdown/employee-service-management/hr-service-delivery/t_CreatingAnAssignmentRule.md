---
title: Add or modify an HR assignment rule
description: Assignment rules are used to assign the HR group when it is not assigned from the catalog item template. You can create HR assignment rules as needed.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assignment and matching rules in HR, HR Service Delivery case assignment, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add or modify an HR assignment rule

Assignment rules are used to assign the HR group when it is not assigned from the catalog item template. You can create HR assignment rules as needed.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Assignment Rules** &gt; **HR Assignment Rules**.

2.  Click **New**.

3.  Complete the form.

<table id="table_bgn_41w_r4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the HR assignment rule.

</td></tr><tr id="ol_execution_order"><td>

Execution Order

</td><td>

Order in which the rule processes. Rules with lower-order numbers process first.For example:

-   The first HR assignment rule has an execution order of 100.
-   A second HR assignment rule has an execution order of 200.
-   If a group has members that fit the conditions defined in the first HR assignment rule, it assigns an agent with the least amount of assigned cases.
-   If the first HR assignment rule cannot find an agent to assign, the second HR assignment rule runs.


</td></tr><tr><td>

Application

</td><td>

Indicates core application scope the assignment rule applies to.

</td></tr><tr><td>

Active

</td><td>

Check box that specifies the rule is in use.

</td></tr><tr><td class="sub-head" colspan="2">

Applies To

</td></tr><tr><td>

Table

</td><td>

Table with the records that the assignment rule applies to. Default is the HR Task \[hr\_task\] table.

</td></tr><tr><td>

Conditions

</td><td>

Conditions in which the assignment rule applies.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td class="sub-head" colspan="2">

Assign To

</td></tr><tr><td>

User

</td><td>

User to assign to the case when this rule is applied.

</td></tr><tr><td>

Group

</td><td>

Group to assign to the case when this rule is applied.

</td></tr><tr><td class="sub-head" colspan="2">

Script

</td></tr><tr><td>

Script

</td><td>

Script to define advanced assignment rule functionality. Current.variable\_pool set of variables is available.**Note:** Two example scripts are provided as a comment. You can modify either script or use the information as a starting point for your own script. Remove the examples when you are finished.

</td></tr></tbody>
</table>4.  Click **Update**.


## What to do next

After creating the assignment rule, you can test it to verify that it works.

**Parent Topic:**[Assignment and matching rules in HR](../concept/c_UseAssignmentRules-1.md)

**Related topics**  


[HR Administration](../concept/c_AdministerHRServiceManagement.md)

