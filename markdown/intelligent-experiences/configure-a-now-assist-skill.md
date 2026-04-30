---
title: Activate a Now Assist skill
description: Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the ServiceNow AI Platform.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Activate, Now Assist, skill, panel, ServiceNow AI Platform, admin, features]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Activate a Now Assist skill

Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the ServiceNow AI Platform.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

Activate the skills that are most relevant to your use cases and business needs. For a full list of available skills, see [Now Assist skills](../../now-assist-skills/concept/now-assist-skills.md). After the skills have been activated, they’re accessible across the ServiceNow AI Platform based on the availability and display settings you choose.

Note that the activation procedure discussed in this topic are essentially for out-of-box [Now Assist skills](../../now-assist-skills/concept/now-assist-skills.md). The activation process of custom skills in Now Assist Admin console is driven by the approval mandate set in AICT by the AI steward. As Now Assist Admin and AI control tower are integrated, a particular custom skill is blocked or unblocked for activation on Now Assist Admin console based on AICT mandate \(on or off\). The custom skill cannot be activated on Now Assist Admin when the states are 'need review', 'in review' or 'rejected' in AICT.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Now Assist Skills**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Skills** tab.

2.  On the navigation panel, select a workflow, such as **Technology**.

    Each workflow contains skills sets.

3.  Toggle between the list and grid layout for optimum view experience.

    **Note:** The skill details are presented at the forefront of the interface, enabling you to view all the details without needing to click or navigate away.

4.  Select **Activate skill**.

5.  In the first step of the skill configuration, determine which inputs or triggers that you want to associate with the skill.

    Each skill configuration has steps that are shown in the guided setup. The exact steps vary from skill to skill. A symbol next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    ![First step of the Now Assist incident summarization skill, which shows the input fields that the summary is based on.](../../now-assist-platform/images/activate-skill-step-1.png)

    **Note:** Some configuration options are read only.

6.  After you've configured the current step, select **Save and continue** to go to the next step.

7.  For some skills, the next step is to define the availability.

    You can select **Skill is always available** if you do not want to place any restrictions on when the skill is available for use. If you want to add conditions, select **Customize skill availability**. Selecting this option opens up a condition builder for you to select fields and values that determines whether someone can use the skill.

    ![Case summarization Define Availability step with customize skill availability selected and the Location field value set to 111w 18th Street, Plano,TX as a required condition.](../image/now-assist-define-availability.png)

8.  In the next step of the skill configuration, select where you'd like to display the skill.

    Options vary from skill to skill. Some options are only available for certain skills.

    -   **In-product desktop**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.
    -   **Core UI**: When selected, the Now Assist skill will display as a UI action in the Core UI.
    ![Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.](../../now-assist-platform/images/activate-skill-step-2.png)

9.  For Now Assist custom skills, find additional display option of **Conversational experiences**.

    When selected, the Now Assist custom skill will also be available in Conversational experiences.

10. Select a **Conversational experiences** for the custom skill.

    You can choose from Now Assist panel, Virtual Agent or both.

11. Select **Virtual Assistants**.

    Now Assist Virtual Agent is selected by default.

12. Select the down arrow next to **Display** toggle to select the roles that can use the skill.

13. Enter the name of the role to add roles in the User roles field.

    You must have at least one role specified, but you can add as many as you like.

14. Select the X icon in the role bubble to remove an existing roles.

    If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](activate-now-assist-panel.md).

15. Review your choices and select **Activate** to complete the configuration.


## What to do next

Use the Now Assist applications and skills that you've activated.

-   **[Configure chat summarization and chat reply recommendation skills in the Now Assist Admin console](configure-chat-summarization-in-the-now-assist-admin-console.md)**  
Define the triggers, inputs, and display location for chat summarization and chat reply recommendation by using the guided setup in the Now Assist Admin console. The activation steps are conceptually same for both the skills.
-   **[Configure email reply recommendation in the Now Assist Admin console](configure-email-recommendation.md)**  
Configure the email recommendation Now Assist skill to enable agents to draft email replies based on contextual information.

**Parent Topic:**[Configuring Now Assist settings and features](../concept/configuring-na-landing.md)

