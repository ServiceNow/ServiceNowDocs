---
title: Activate an AI skill
description: Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-a-now-assist-skill.html
release: brazil
topic_type: task
last_updated: "2026-09-15"
reading_time_minutes: 3
keywords: [Activate, Now Assist, skill, panel, ServiceNow AI Platform, admin, features]
breadcrumb: [Using Now Assist Admin, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Activate an AI skill

Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the ServiceNow AI Platform.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin. For information about roles, see [AI Admin Hub roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/roles-installed-with-now-assist-admin.md) and [Roles and responsibilities for AI administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-roles-responsibilities-ai-admin.md).

## About this task

Activate the skills that are most relevant to your use cases and business needs. For a full list of available skills, see [Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md). After the skills have been activated, they’re accessible across the ServiceNow AI Platform based on the availability and display settings you choose.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

    If you’re already in AI Admin Hub, select the **AI Skills** tab.

2.  On the navigation panel, select a workflow, such as **Technology**.

    Each workflow contains feature sets.

3.  On the feature card that is associated with the skill you'd like to activate, select **View details**.

4.  In the All available skills section, select **Activate Skill**.

5.  In the first step of the skill configuration, determine which inputs or triggers you want to associate with the skill.

    Each skill configuration has steps that are shown in the guided setup. The exact steps vary from skill to skill. A symbol next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    \[Omitted image "activate-skill-step-1.png"\] Alt text: First step of the Now Assist incident summarization skill, which shows the input fields that the summary is based on.

    **Note:** Some configuration options are read only.

6.  After you've configured the current step, select **Save and continue** to go to the next step.

7.  Define the access controls by updating the roles withing **Define access**.

    Roles can be added by entering the name of the role in the User roles field. Existing roles can be removed by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many as you like.

8.  In the next step of the skill configuration, select where you'd like to display the skill.

    Options vary from skill to skill. Some options are only available for certain skills.

    -   **In-product desktop**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **ServiceNow Otto panel**: When selected, the AI skills are available in the ServiceNow Otto panel. If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md).
    -   **Core UI**: When selected, the AI skill will display as a UI action in the Core UI.
    \[Omitted image "activate-skill-step-2.png"\] Alt text: Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.

9.  Review your choices and select **Activate** to complete the configuration.


## What to do next

Use the ServiceNow Otto applications and skills that you've activated.

-   **[Configure chat summarization and chat reply recommendation skills in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-chat-summarization-in-the-now-assist-admin-console.md)**  
Define the triggers, inputs, and display location for chat summarization and chat reply recommendation by using the guided setup in the AI Admin Hub console. The activation steps are conceptually same for both the skills.
-   **[Configure email reply recommendation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-email-recommendation.md)**  
Configure the email recommendation Now Assist skill to enable agents to draft email replies based on contextual information.

**Parent Topic:**[Using Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/using-now-assist-admin_0.md)

