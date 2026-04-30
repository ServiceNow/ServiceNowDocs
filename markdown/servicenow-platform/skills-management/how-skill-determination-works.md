---
title: Learn how Skill Determination works
description: Use Skill Determination to add skills to incoming work items so that agents with those skills can work on it.
locale: en-US
release: zurich
product: Skills Management
classification: skills-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Routing work items to agents based on skills, Using Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Learn how Skill Determination works

Use Skill Determination to add skills to incoming work items so that agents with those skills can work on it.

Skill Determination uses two rules:

-   Skill Determination rule—set what skills you want to add to incoming work items.
-   Business rule for Skill determination—set criteria for when a business rule must execute.

    When executed, it runs on the source table defined in the Skill Determination rule, triggers the corresponding Skill Determination rule, and adds the skills that are in the Skill Determination rule record to the incoming work item.


The flow chart shows a visual representation of the Skill Determination flow.

![Infographic for skill determination flow](../images/skill-determination.png)

<table id="table_y2q_s1z_k1c"><thead><tr><th>

Step

</th><th>

Skill Determination Flow

</th></tr></thead><tbody><tr><td>

1.

</td><td>

A user has an issue with their VPN connection and has created an incident with the short description 'VPN not working'.

 The incident needs agents with **Router, Switch,** and **Network** skills to work on the task.

</td></tr><tr><td>

2.

</td><td>

A business rule has been created on the incident table that's set to trigger when an incident is created.

</td></tr><tr><td>

3.

</td><td>

The business rule looks up all Skill Determination rules where the incident table is set as the source table. The business rule then triggers the Skill Determination rule that has one of the conditions set as the **\[Short description\] \[contains\] \[VPN\]**.The Skill Determination rule has the skills **Router, Switch,** and **Network** skills in the Skills related list. When triggered, these skills are added to the incident with the short description 'VPN not working'.

</td></tr></tbody>
</table>**Parent Topic:**[Routing work items to agents based on skills](skill-based-routing.md)

