---
title: Create a matching rule for case routing
description: Create a matching rule for a customer service case that identifies the case attributes as well as the agent resources.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure case routing and assignment, Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a matching rule for case routing

Create a matching rule for a customer service case that identifies the case attributes as well as the agent resources.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Routing and Assignment** &gt; **Matching Rules**.

2.  Click **New**.

3.  Fill in the fields on the Matching Rule form.

    This form contains the following sections:

    -   Basic rule information
    -   Applies to: use this section to create rule conditions
    -   Resource: use this section to create agent and agent group conditions
<table id="table_czw_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the matching rule.

</td></tr><tr><td>

Execution order

</td><td>

The order in which this matching rule is to be executed. Similar to business rules, matching rules are processed based on execution order, from the lowest to the highest.

</td></tr><tr><td>

Active

</td><td>

Enable this check box to activate the matching rule.

</td></tr><tr><td class="subhead" colspan="2">

Applies To

</td></tr><tr><td>

Table

</td><td>

The table that stores the task for which the matching rule is being created. The default is the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Conditions

</td><td>

Use the buttons in this field to build one or more conditions on the selected table. A condition is made up of a selected field, an operator, and a value. Add conditions using the **AND** and **OR** buttons. Delete conditions by clicking the **X** to the right of a condition.

</td></tr><tr><td class="subhead" colspan="2">

Resource

</td></tr><tr><td>

Matching

</td><td>

The type of resource matching method to use for this rule: Simple, Advanced, Scripted, Selection Criteria. Select **Simple** to assign a task to a specific user.

1.  Click the lookup icon next to the **Resource** field.
2.  Select a **Table name**.
3.  Select a **Document** from the table.
4.  Click **OK**.
 Select **Advanced** to create a specific set of resource conditions. Then use the condition builder in the **Resource** field to identify these conditions.

 Select **Scripted** to create a customized script for identifying resources, with the goal of returning a list of users that have the same skills as the task. The task under consideration is set in the context of the script. For example:

 ```
//current has the task record for which the rule is being executed.
var task = current;
var skills = task.getValue("skills");
var skillUtil = new global.SkillsUtils();
var skilledUsers = skillUtil.getAllSkilledUserIds(skills);
return skilledUsers;
```

</td></tr><tr><td>

Resource

</td><td>

This field changes depending on the resource matching type selected in the **Matching** field. For **Simple** matching, use this field to select a table and a user.

 For **Advanced** matching, use the condition builder in this field to build one or more conditions to identify a resource. These conditions can be based on user role, agent group, specific skills, work load, or agent availability.

</td></tr><tr><td>

Schedule based filtering

</td><td>

This field applies to **Advanced** matching. Enable this check box to filter resources that are in schedule \(work hours\) at the time of routing.

</td></tr><tr><td>

Script

</td><td>

For **Scripted** matching. use this field to create a customized script for identifying resources. An example script is included. The expected return from a customized script is an array of resource sys\_ids.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The rule appears in the Matching Rules list.

5.  Open the newly created rule from the Matching Rules list and add the desired matching criteria.

6.  From the **Select Criteria** related list, click **New**.

7.  Select a **Criterion**.

8.  In the **Use for** field, specify how you want the matching criterion to be used.

<table id="choicetable_wzv_ztm_sx"><tbody><tr><td id="d103198e355">

**Ranking and display**

</td><td>

Use the criterion to determine agent ranking and displays it in a column on the workbench.

</td></tr><tr><td id="d103198e364">

**Display only**

</td><td>

Displays the criterion in a column on the workbench but does not use it to determine agent ranking.

</td></tr><tr><td id="d103198e373">

**Ranking only**

</td><td>

Uses the criterion to determine agent ranking but does not display it on the workbench.

</td></tr></tbody>
</table>9.  Select a **Ranking Method**.

<table id="choicetable_ccn_j5m_sx"><tbody><tr><td id="d103198e394">

**More is better**

</td><td>

For example, more availability is better when determining the agent ranking.

</td></tr><tr><td id="d103198e403">

**Less is better**

</td><td>

For example, fewer assigned cases are better when determining agent ranking.

</td></tr></tbody>
</table>10. Click **Submit**.

    The criterion appears on the Matching Rule form in the **Select Criteria** related list.

11. From the **Select Criteria** related list, set a **Threshold** for the criterion.

    A threshold sets a minimum requirement for a criterion. If necessary, personalize the list and add the **Threshold** field.


