---
title: Configure agent assignment rules
description: Set the Advanced Work Assignment criteria for assigning work items to agents. Choose the assignment rule that considers the agent with the most capacity or the agent who has gone the longest without work. Establish the settings for the auto-assign handling, reject handling, and skill handling related lists.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [auto assign, awa auto assign, auto assign handling, reject handling, skill handling]
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Configure agent assignment rules

Set the Advanced Work Assignment criteria for assigning work items to agents. Choose the assignment rule that considers the agent with the most capacity or the agent who has gone the longest without work. Establish the settings for the auto-assign handling, reject handling, and skill handling related lists.

## Before you begin

-   A basic understanding of the [Skills Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/skills-management/skills-management.md) feature is recommended.
-   If you want agent skills to be considered when work is routed to the appropriate agents, define the skills for your agents or groups. When you enable the skill handling options on the Assignment Rules form, AWA assigns the users in groups with the appropriate skills to corresponding work items.
-   You can use rules to identify skills and assign them to work items. For more information on defining and assigning skills for work items, see [Routing work items to agents based on skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/skills-management/skill-based-routing.md).

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the assignment rules settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up assignment rules**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Assignment Rules**.
2.  Choose a situation.

    -   To create a rule, select **New**.
    -   To change a rule, select the rule to be updated.
3.  On the Assignment Rule form, fill in the fields.

    For a description of the field values, see [Assignment Rule form](../reference/awa-assignment-rules.md).

4.  Select **Submit** for a new rule or **Update** if you're changing the rule.

    The assignment rule is added to or updated in the Assignment Rules \[awa\_assignment\_rule\] table.


