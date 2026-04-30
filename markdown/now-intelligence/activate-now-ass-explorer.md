---
title: Activate AI Data Explorer skills
description: Enable AI Data Explorer skills under Now Assist skills for Platform to give users AI-assisted, shared spaces to explore data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Activate AI Data Explorer skills

Enable AI Data Explorer skills under Now Assist skills for Platform to give users AI-assisted, shared spaces to explore data.

## Before you begin

Install the AI Data Explorer application from the ServiceNow® Store. The correct Workflow Data Fabric entitlement is required, along with Yokohama Patch 11 or higher.

The Query Generation skills "analytics query generation," "analytics insight generation," "analytics hidden insight generation," and "analytics follow-up generation" are required. These skills are active by default. For more information, see [Query Generation skills](enable-query-generation.md).

Role required: now\_assist\_explorer\_admin or higher

## About this task

Assign the now\_assist\_explorer\_user role, and activate the AI Data Explorer skills.

## Procedure

1.  Grant the now\_assist\_explorer\_user role to users who need to explore data with AI Data Explorer.

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

3.  In the product area pane, select **Data and Analytics** &gt; **Analytics**.

4.  In Now Assist skills for Analytics, search for the analytics exploration skill.

    ![Now Assist Skills tab of Now Assist Admin console, showing the skills for AI Data Explorer under Platform.](../image/nowass-expl-skills.png)

5.  Select **Activate skill**.

6.  Configure the analytics exploration skill.

    1.  In the **Record level analysis** page, you can activate record-level analysis and set which tables it applies to.

        For more information, see [Configure record level analysis in AI Data Explorer](../concept/record-level-analysis.md).

    2.  Select **Save and continue**.

    3.  In the **Define access** page, you can add roles who can create and edit explorations in AI Data Explorer.

        All AI Data Explorer and Query Generation skills should have one role in common. The default role for this skill, now\_assist\_explorer\_user, contains the default Query Generation role, sn\_query\_gen.user. Any changes you make must preserve the rights of the AI Data Explorer user to access Query Generation skills.

    4.  Select **Save and continue**.

    5.  In the **Review and activate** page, review the settings you made and either go back and change them or select **Activate**.

    **Note:** You can come back later and edit the settings for this or any other skill.

    ![Tile for the Analytics exploration skill showing the Edit button.](../image/ai-data-expl-edit-skill.png)

7.  To enable users to generate recommendations based on the findings in their exploration, turn on the exploration action recommendation skill.

    You can set the roles that can generate recommendations. The default role is now\_assist\_explorer\_user. This role contains sn\_query\_gen.user, granting necessary access to Query Generation.

8.  To enable users to generate summaries of explorations, turn on the exploration summarization skill.

    You can set the roles that can generate summaries. Again, the default role is now\_assist\_explorer\_user. This role contains sn\_query\_gen.user, granting necessary access to Query Generation.

9.  To enable users to use AI to help refine text that they write in explorations, activate the refine text in explorations skill.

    A dialog opens asking you where you want to display the refine text option.

    1.  In the **Select display** page, under **Choose where to display**, toggle **Display** on for **In-product desktop**.

    2.  You can set the roles that can use AI to refine texts in their explorations.

        Again, the default role is now\_assist\_explorer\_user. This role contains sn\_query\_gen.user, granting necessary access to Query Generation.

    3.  Select **Save and continue**.

    4.  Browse the review and select **Activate**.


**Parent Topic:**[Configure AI Data Explorer](configure-now-ass-explorer.md)

