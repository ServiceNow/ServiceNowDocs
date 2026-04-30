---
title: Manage skills using Workforce Optimization for Field Service
description: Add or update skills for an agent. You can approve predicted skills if the skill is necessary for the agent to complete assigned tasks. You can also reject a skill if it doesn't apply to the agent.
locale: en-US
release: zurich
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Coaching, Workforce Optimization, Workforce, Use, Field Service Management]
---

# Manage skills using Workforce Optimization for Field Service

Add or update skills for an agent. You can approve predicted skills if the skill is necessary for the agent to complete assigned tasks. You can also reject a skill if it doesn't apply to the agent.

## Before you begin

Role required: admin

## About this task

The Predictive Intelligence application for skills displays the recommended skills on each agent's profile. The application uses sample cases that the agent has worked on to recommend skills for an agent.

You can view skills for all users grouped by assignment group and the overall skill coverage for each group.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../../workforce-optimization-for-customer-service-configurable/image/coaching-new.png)\) icon.

3.  Click the **Skills** tab.

    You can view the list of all assigned skills and the skill level for each agent on your team. For more information on skills and skills levels, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    You can also filter the skill matrix based on users, groups, skill type, skill level, or skill category. Reset the filter if you want to view the skills for all users.

4.  Add a skill or skill level.

<table id="choicetable_ufk_1hx_nlb"><thead><tr><th align="left" id="d38247e123">

To

</th><th align="left" id="d38247e126">

Do this

</th></tr></thead><tbody><tr><td id="d38247e132">

**Add a skill**

</td><td>

1.  In the skill matrix, click **Add** for the skill that you want to add to the agent.
2.  Select the **Skill Level** field and choose a level for the skill.
3.  Click **OK**.
The skill gets automatically added to the agent.

</td></tr><tr><td id="d38247e162">

**Update a skill level**

</td><td>

1.  In the skill matrix, select a skill level for an agent.
2.  Select the skill level that you want to add for the agent.
3.  Click **OK**.


</td></tr></tbody>
</table>5.  Approve or reject a skill that is recommended by Predictive Intelligence.

    1.  In the skill matrix, click **Recommended** to approve and recommend a skill for the user.
    2.  In the **Details** tab, review the request for skill approval, the sample case resolutions that were used to predict the skill, and the activity stream.
    -   To approve a skill, click **Approve**. The skill is added to the agent and the lowest level for the skill is automatically associated with the added skill. The state for the request changes to **Approved** and the skill is added to the agent.
    -   To reject a skill, click **Reject**. The state for the request changes to **Rejected**. Predictive Intelligence does not recommend the skill for the user again and the field changes to **Add**.
    -   Click the More Options \(![More options icon.](../../workforce-optimization-for-customer-service-configurable/image/ellipsis-new.png)\) icon and select **Save**.
    The application assigns the skill to the user. If the assigned skill does not have a skill level, the application adds the basic skill level to the user.


