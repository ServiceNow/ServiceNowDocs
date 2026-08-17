---
title: Activate a AI skill
description: Configure the triggers, settings, and display locations for AI skills to enable generative AI capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/configure-now-assist-skill-spm.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-04-14"
reading_time_minutes: 2
breadcrumb: [Use AI Admin Hub, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Activate a AI skill

Configure the triggers, settings, and display locations for AI skills to enable generative AI capabilities.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Activate the skills that are most relevant to your use cases and business needs. For a full list of available skills, see [AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md). After the skills have been activated, they’re accessible across the ServiceNow AI Platform based on the availability and display settings you choose.

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub**.

    If you’re already in the AI Admin Hub console, select the **AI Skills** tab.

2.  On the navigation panel, select **Technology** &gt; **SPM**.

3.  Select **Activate Skill** option on the required feature card.

4.  In the first step of the skill configuration, determine which inputs or triggers that you want to associate with the skill.

    Each skill configuration has steps that are shown in the guided setup. The exact steps may vary from skill to skill. A symbol next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    **Note:** Some configuration options are read-only until you change the scope of the application

5.  After you have configured the current step, select **Save and continue** to go to the next step.

6.  For some skills, the next step is to define the availability.

    You can select **Skill is always available** if you don't want to place any restrictions on the skill's availability. If you want to add conditions, select **Customize skill availability**. Selecting this option opens up a condition builder for you to select fields and values that determines whether someone can use the skill.

7.  In the next step of the skill configuration, select where you'd like to display the skill.

    Options may vary from skill to skill.

8.  Review your choices and select **Activate** to complete the configuration.


## What to do next

Use the AI applications and skills that you have activated.

-   **[Configure project insights generation skill in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/configure-project-insights-generation-skill.md)**  
Define the triggers, inputs, and display location for project insights generation skill.
-   **[Configure project status generation skill in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/configure-project-status-generation-skill.md)**  
Configure the project status generation AI skill to enable.

**Parent Topic:**[Use AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/using-na-admin-spm.md)

