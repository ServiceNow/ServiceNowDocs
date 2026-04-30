---
title: Add or modify a matching rule
description: You can add or modify a matching rule to assign HR cases to specific users or groups.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assignment and matching rules in HR, HR Service Delivery case assignment, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add or modify a matching rule

You can add or modify a matching rule to assign HR cases to specific users or groups.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Assignment Rules** &gt; **HR Matching Rules**.

2.  Complete or edit the form.

<table id="table_bgn_41w_r4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the HR matching rule.

</td></tr><tr id="ol_execution_order"><td>

Execution Order

</td><td>

Order in which the rule processes. Rules with lower-order numbers are processed first. If a rule is applied, the rules with a higher-order number are not processed.For example, a matching rule with order 100 states to assign the case to an agent with the specified skill.

 Matching rule with order 200 states to assign the case to the group **HR**.

 If a group has the specified skill, then it is assigned. If not, then the second rule runs and assigns it to **HR**.

</td></tr><tr><td>

Active

</td><td>

Check box that specifies the rule is in use.

</td></tr><tr><td class="sub-head" colspan="2">

Applies To

</td></tr><tr><td>

Table

</td><td>

Table with the records that the matching rule applies to. Default is the HR Task \[hr\_task\] table.

</td></tr><tr><td>

Conditions

</td><td>

Conditions in which the matching rule applies.**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td></tr><tr><td class="sub-head" colspan="2">

Resource

</td></tr><tr><td>

Matching

</td><td>

Indicates the option to match the rules. Default is Scripted.

</td></tr><tr><td>

Script

</td><td>

Script to define advanced matching rule functionality. Current.variable\_pool set of variables is available.**Note:** Two example scripts are provided as a comment. You can modify either script or use the information as a starting point for your own script. Remove the examples when you are finished.

</td></tr></tbody>
</table>3.  Submit the HR case.

4.  Reopen the case and check that the correct matching information was added.


**Parent Topic:**[Assignment and matching rules in HR](../concept/c_UseAssignmentRules-1.md)

