---
title: Activate a Now Assist skill
description: Configure the triggers, settings, and display locations for Now Assist skills to enable generative AI capabilities across the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/configure-a-now-assist-skill.html
release: xanadu
topic_type: task
last_updated: "2024-11-18"
reading_time_minutes: 3
keywords: [Activate, Now Assist, skill, panel, ServiceNow AI Platform, admin, features]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Activate a Now Assist skill

Configure the triggers, settings, and display locations for Now Assist skills to enable generative AI capabilities across the ServiceNow AI Platform.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

After the skills have been turned on, they’re accessible across the ServiceNow AI Platform or on the Now Assist panel. These skills empower your agents to resolve cases more efficiently with record or chat summarization or resolution note generation. Turn on the skills that are most relevant to your use cases and business needs.

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

    You can select both in-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces.

        For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/activate-now-assist-panel.md).

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    Roles can be added by entering the name of the role in the User roles field. Existing roles can be removed by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many as you like.

    \[Omitted image "activate-skill-step-2.png"\] Alt text: Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.

9.  Review your choices and select **Activate** to complete the configuration.


## What to do next

Use the Now Assist applications and skills that you've activated:

-   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)
-   [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/build-workflows/now-assist-for-creator/now-assist-for-creator-landing.md)

-   **[Configure chat summarization in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/configure-chat-summarization-in-the-now-assist-admin-console.md)**  
Define the triggers, inputs, and display location for chat summarization by using the guided setup in the Now Assist Admin console.
-   **[Configure email reply recommendation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/configure-email-recommendation.md)**  
Configure the email recommendation Now Assist skill to enable agents to draft email replies based on contextual information.

**Parent Topic:**[Configuring Now Assist settings and features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/configuring-na-landing.md)

