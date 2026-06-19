---
title: Activate a Now Assist skill
description: Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/configure-a-now-assist-skill.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Activate, Now Assist, skill, panel, ServiceNow AI Platform, admin, features]
breadcrumb: [Using Now Assist Admin, Now Assist, Enable AI experiences]
---

# Activate a Now Assist skill

Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the ServiceNow AI Platform.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Activate the skills that are most relevant to your use cases and business needs. For a full list of available skills, see [Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md). After the skills have been activated, they’re accessible across the ServiceNow AI Platform based on the availability and display settings you choose.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Features**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Features** tab.

2.  On the navigation panel, select a workflow, such as **Technology**.

    Each workflow contains feature sets.

3.  On the feature card that is associated with the skill you'd like to activate, select **View details**.

4.  In the All available skills section, select **Activate Skill**.

5.  In the first step of the skill configuration, determine which inputs or triggers that you want to associate with the skill.

    Each skill configuration has steps that are shown in the guided setup. The exact steps vary from skill to skill. A symbol next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    \[Omitted image "activate-skill-step-1.png"\] Alt text: First step of the Now Assist incident summarization skill, which shows the input fields that the summary is based on.

    **Note:** Some configuration options are read only.

6.  After you've configured the current step, select **Save and continue** to go to the next step.

7.  For some skills, the next step is to define the availability.

    You can select **Skill is always available** if you do not want to place any restrictions on when the skill is available for use. If you want to add conditions, select **Customize skill availability**. Selecting this option opens up a condition builder for you to select fields and values that determines whether someone can use the skill.

    \[Omitted image "now-assist-define-availability.png"\] Alt text: Case summarization Define Availability step with customize skill availability selected and the Location field value set to 111w 18th Street, Plano,TX as a required condition.

8.  In the next step of the skill configuration, select where you'd like to display the skill.

    Options vary from skill to skill. Some options are only available for certain skills.

    -   **In-product desktop**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-now-assist-panel.md).
    -   **Core UI**: When selected, the Now Assist skill will display as a UI action in the Core UI.
    Select the down arrow next to the Display toggle to select the roles that can use the skill. Roles can be added by entering the name of the role in the User roles field. Existing roles can be removed by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many as you like.

    \[Omitted image "activate-skill-step-2.png"\] Alt text: Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.

9.  Review your choices and select **Activate** to complete the configuration.


## What to do next

Use the Now Assist applications and skills that you've activated.

-   **[Configure chat summarization and chat reply recommendation skills in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-chat-summarization-in-the-now-assist-admin-console.md)**  
Define the triggers, inputs, and display location for chat summarization and chat reply recommendation by using the guided setup in the Now Assist Admin console. The activation steps are conceptually same for both the skills.
-   **[Configure email reply recommendation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-email-recommendation.md)**  
Configure the email recommendation Now Assist skill to enable agents to draft email replies based on contextual information.

**Parent Topic:**[Using Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/using-now-assist-admin_0.md)

