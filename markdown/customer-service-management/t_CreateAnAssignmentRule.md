---
title: Create an assignment rule for case routing
description: Create a rule that assigns those cases that meet the matching rule criteria to a customer service agent.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure case routing and assignment, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create an assignment rule for case routing

Create a rule that assigns those cases that meet the matching rule criteria to a customer service agent.

## Before you begin

Role required: admin

## Procedure

1.  Open the desired matching rule.

2.  Select the **Create assignment rule** related link.

    You can also create an assignment rule by navigating to **Routing and Assignment** &gt; **Assignment Rule** and selecting **New**.

3.  Fill in the fields on the Assignment Rule form.

<table id="table_czw_ftc_acm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the assignment rule.

</td></tr><tr><td>

Application

</td><td>

The name of the application to which this assignment rule belongs. The default application is **Global**.

</td></tr><tr><td>

Order

</td><td>

The order in which this assignment rule is executed. Similar to business rules, assignment rules are processed based on execution order, from the lowest to the highest.

</td></tr><tr><td>

Active

</td><td>

Enable this check box to activate the matching rule. Only active assignment rules take effect.

</td></tr><tr><td class="subhead" colspan="2">

Applies To

</td></tr><tr><td>

Table

</td><td>

The table that stores the task for which the assignment rule is being created. This list shows only those tables and database views that are in the same scope as the assignment rule. If you select a custom table that extends the task table, you must clear the instance cache by navigating to `https://<instance_name>.service-now.com/cache.do` for the assignment rule to work.

**Warning:** Clearing the system cache can affect overall performance, and degrade system response times. Don’t run cache flushes during business hours, and don’t trigger cache flushes automatically.

</td></tr><tr><td>

Conditions

</td><td>

The conditions in which the assignment rule applies.Use the buttons in this field to build one or more conditions on the selected table. A condition is made up of a selected field, an operator, and a value. Add conditions using the **AND** and **OR** buttons. Delete conditions by selecting the **X** icon.

</td></tr><tr><td class="subhead" colspan="2">

Assign To

</td></tr><tr><td>

User

</td><td>

User to be assigned to the task.

</td></tr><tr><td>

Group

</td><td>

The assignment group to be assigned to the task.

</td></tr><tr><td class="subhead" colspan="2">

Script

</td></tr><tr><td>

Script

</td><td>

A script to determine advanced assignment rule functionality. Scripts provide access to current.variable\_pool variables.

</td></tr></tbody>
</table>4.  Select **Update**.


**Related topics**  


[Define assignment rules](https://www.servicenow.com/docs/access?context=c_DefineAssignmentRules&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

