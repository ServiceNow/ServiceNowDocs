---
title: Create Skill Determination rules to assign skills to work items
description: Create Skill Determination rules to identify skills required by agents to work on work items and automatically associate them to those work items.
locale: en-US
release: australia
product: Skills Management
classification: skills-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Routing work items to agents based on skills, Using Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create Skill Determination rules to assign skills to work items

Create Skill Determination rules to identify skills required by agents to work on work items and automatically associate them to those work items.

## Before you begin

Role required: skill\_admin or admin

## About this task

You can automatically add a skill to a case based on the product associated with the case if you enable the Product to Skill mapping table \(Skill Required for Model Maintenance \[cmn\_m2m\_skill\_model\]\).

A skill determination rule is created for every new skill required for a work item.

-   If a skill is no longer required for a work item, deactivate or remove the rule applied for the work item.
-   If two rules have the same skill associated with one work item and one rule evaluates the skill as mandatory and the other rule evaluates it as optional, then the rule that evaluates the skill as mandatory is always used.

The table describes the types of Skill Determination rules you could create.

<table id="table_nwc_spz_k1c"><thead><tr><th>

Rule Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Simple**

</td><td>

Adds skills to work items based on a set of conditions used to evaluate the source table.

</td></tr><tr><td>

**Lookup**

</td><td>

Adds skills to work items based on selections from two different tables connected using one or more reference fields.

</td></tr><tr><td>

**Advanced**

</td><td>

Adds skills to work items using a script.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Skills** &gt; **Skill Determination Rules**.

2.  Click **New**.

3.  In the **Name** field, enter a name for the rule.

4.  Select the **Active** check box to enable the rule to assign skills to work items.

5.  From the **Source table** drop-down menu, select the work item source table for this rule.

6.  Using the condition builder, select the conditions to evaluate the work item.

7.  Create the rule.

<table id="choicetable_vx5_gc1_wgb"><thead><tr><th align="left" id="d181131e204">

Rule type

</th><th align="left" id="d181131e207">

Steps

</th></tr></thead><tbody><tr><td id="d181131e213">

**Create a simple rule**

</td><td>

1.  From the **Type** drop-down menu, select **Simple**.
2.  In the **Skills** table, add each skill required for the selected work item.
3.  If a skill is optional for selected work item, in the **Mandatory** field, select **False**.
4.  In the **Skill Level** field, add a level for the skill. You must configure the form to display this field.

For information about defining skill levels, see [Define a skill level type](../../skills-management/task/define-skill-level-type.md).

</td></tr><tr><td id="d181131e265">

**Create a lookup rule**

</td><td>

1.  From the **Type** drop-down menu, select **Lookup**.
2.  From the **Lookup table** drop-down menu, select the reference table to connect to the source table.

The **Skills Field** that connects the source and reference tables is automatically populated.

3.  If this skill is mandatory, select the **Mandatory** check box.
4.  From the **Skill Level Field** drop-down menu, select a level for this skill.
5.  Click **Save**.
6.  In the **Field Mappings** related list, click **New**.
7.  From the **Source table field** drop-down menu, select an attribute to map to the reference table.
8.  From the **Lookup table field** drop-down menu, select an attribute to map to the source table.


</td></tr><tr><td id="d181131e337">

**Create an advanced rule**

</td><td>

1.  From the **Type** drop-down menu, select **Advanced**.
2.  In the **Script** window, enter a script.


</td></tr></tbody>
</table>8.  Click **Submit**.


**Parent Topic:**[Routing work items to agents based on skills](../../skills-management/concept/skill-based-routing.md)

