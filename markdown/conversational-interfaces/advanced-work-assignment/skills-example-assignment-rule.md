---
title: Create an assignment rule that auto assigns agents' work
description: Create an assignment rule that routes cases according to skills.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tutorial: Automatically assign work to agents by skill, Configure agent assignment rules, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create an assignment rule that auto assigns agents' work

Create an assignment rule that routes cases according to skills.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the assignment rules settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up assignment rules**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Assignment Rules**.
2.  Select **New**.

3.  Enter the following information in the fields listed:

    -   **Name**: `Case Assignment Rule with Skills`
    -   **Assign by**: `Most Capacity`
    -   **Enable auto-assign work items**: Selected

        **Note:** Selecting this option automatically accepts chat interactions on behalf of agents. The **Display options** field appears and you can select either **Inbox card** or **Inbox card and workspace tab**.

    -   **Enable skills**: Selected
    -   **Evaluate skill level**: Cleared
    -   **Enforce mandatory skills**: Selected
4.  Select **Submit**.


**Parent Topic:**[Tutorial: Automatically assign work to agents by skill](../concept/skills-routing-tutorial.md)

