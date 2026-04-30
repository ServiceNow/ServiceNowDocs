---
title: Query Generation skills
description: Query Generation skills enable users to ask questions in Now Assist in Platform Analytics applications and receive answers.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-21"
reading_time_minutes: 1
breadcrumb: [Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Query Generation skills

Query Generation skills enable users to ask questions in Now Assist in Platform Analytics applications and receive answers.

## Before you begin

Query Generation is included in Generative AI Controller, which is included with Now Assist applications from the ServiceNow® Store. Yokohama Patch 7 or later is required.

Role required: admin

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Application Manager** and verify that the Generative AI Controller plugin is activated.

    It is likely to already be active, especially if you installed and activated a Now Assist application and plugin that has Now Assist for Platform as a dependency.

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

3.  In the product area pane, select **Data and analytics** &gt; **Analytics**.

4.  Browse for the analytics query generation skill.

    ![Analytics query generation skill tile.](../image/querygen-activate-qg-skill-new.png)

5.  To deactivate a skill, select **Deactivate skill**.

    Features that require the skill, such as AI Data Explorer, will no longer function.

6.  To change the roles that can access a skill, open it for editing.

    ![Opening a skill card to edit the settings.](../image/open-skill-edit.png)

    **Warning:** Be careful when selecting the roles that can access a skill. The default role is sn\_query\_gen.user, which the default roles for other Now Assist in Platform Analytics skills contain. Users of these other skills must be able to access Query Generation skills.


**Parent Topic:**[Configuring Query Generation](../concept/configuring-query-generation.md)

