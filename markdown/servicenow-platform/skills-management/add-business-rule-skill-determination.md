---
title: Add a business rule for skill determination
description: Set up or enable business rules for agents to manage cases, chat interactions, or work order tasks. These business rules trigger Skill Determination rules, ensuring that the required skills are assigned to relevant work items so agents are properly equipped to handle these responsibilities efficiently.
locale: en-US
release: xanadu
product: Skills Management
classification: skills-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Routing work items to agents based on skills, Using Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a business rule for skill determination

Set up or enable business rules for agents to manage cases, chat interactions, or work order tasks. These business rules trigger Skill Determination rules, ensuring that the required skills are assigned to relevant work items so agents are properly equipped to handle these responsibilities efficiently.

## Before you begin

Role required: admin

Enable the Skill Determination \[com.snc.skill\_determination\] plugin.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    **Note:** If you want to use the skill determination rules available by default, make sure the **Active** field for that rule is set to **true**. For example, if you want to use the **Skill determination for interaction** business rule, make sure that the rule is active.

2.  Select **New**.

3.  Add details for the business rule.

<table id="table_ods_w41_l1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the business rule.

</td></tr><tr><td>

Table

</td><td>

Select the table on which you want to run this business rule for skill determination.

</td></tr><tr><td>

Advanced

</td><td>

1.  Enable the **Advanced** check box.
2.  Select the **Advanced** tab.
3.  In the **Script** field, enter the following code:

    ```
(function executeRule(current, previous /*null when async*/ ) {
    var skillUtils = new sn_skill_rule.SkillDeterminationUtils();
    var skills = skillUtils.determineWorkItemSkills(current);
    skillUtils.assignSkillsToWorkItem(skills, current);
})(current, previous);
    ```

**Note:** This script uses the SkillDeterminationUtils utility to identify which skills are needed for the current work item \(such as an incident or task\) and then assigns those skills to it automatically. This helps ensure that the work item has the correct skill requirements based on its details.

4.  In the **When to run** tab, set when you want the business rule to execute. For more information, see [Create a business rule](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).


</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Routing work items to agents based on skills](../concept/skill-based-routing.md)

