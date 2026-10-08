---
title: Activate an AI skill
description: Activate AI skills by configuring settings such as display locations. After the skills have been activated, they can be used across the ServiceNow AI Platform based on the availability and display settings you choose.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-a-now-assist-skill.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 5
keywords: [Activate, Now Assist, skill, panel, ServiceNow AI Platform, admin, features]
breadcrumb: [Using AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Activate an AI skill

Activate AI skills by configuring settings such as display locations. After the skills have been activated, they can be used across the ServiceNow AI Platform based on the availability and display settings you choose.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin. For information about roles, see [AI Admin Hub roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/roles-installed-with-now-assist-admin.md) and [Roles and responsibilities for AI administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-roles-responsibilities-ai-admin.md).

## About this task

Activate the skills that are most relevant to your use cases and business needs. For a full list of available skills, see [Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md).

From the Brazil Patch 1 release, one-step activation is available for default skills using default settings. With this streamlined activation method, the only decision you must make is where to display your skill. If you need granular or custom configuration, the multi-step guided setup wizard is available from Advanced setup. One-step activation isn't available with Next Experience in this release, or with copied or custom skills.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

    If you’re already in AI Admin Hub, select the **AI Skills** tab.

2.  On the navigation panel, select a workflow where your skill is classified, such as **Technology** or **Customer**.

    To review a list of available skills and their classifications, see [Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md). \[Omitted image "activate-skill-step-1.png"\] Alt text: On the AI Skills tab of AI Admin Hub, the Technology workflow is expanded in the navigation panel. Two example cards for AI skills are visible in the work pane.

3.  On the card for the skill you'd like to activate, select **Activate Skill**.

    You can choose between one-step activation or Advanced setup on the modal window.

4.  One-step activation: Choose the locations in your instance where you want the skill to be available using the toggle switches, and then select **Activate**.

    Your skill is activated and displayed in your instance.

    \[Omitted image "activate-skill-step-one-step.png"\] Alt text: Modal window for one-step activation of skills in AI Admin Hub. Two example locations where the skill could be displayed are shown. There is an Advanced setup button for the guided setup.

5.  Advanced setup: Open a multi-step guided wizard by selecting **Advanced setup**.

    |Step|Description|
    |----|-----------|
    |Choose inputs|Choose the table and fields that are used as inputs to the skill. Depending on the skill, inputs may be read-only \(so they can't be customized\).|
    |Define availability|Customize how and when the skill capability will exist and be available. You can choose to make the skill always available. To customize the skill availability, set conditions using the condition builder.|
    |Define access|Define access by selecting ACLs and role restrictions.|
    |Select display|Choose where to display your skill. Slide the toggle to on to enable a display location.|
    |Review and activate|Complete your skill by reviewing the details you have set.|

    Each skill configuration has steps that are shown in the guided setup. The exact steps vary from skill to skill. A symbol next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to proceed to the next step. Return to a previous step by selecting **Back**.

    **Note:** Some configuration options are read only.

6.  Choose inputs: Choose the table and fields that are used as inputs to the skill \(depending on the skill, inputs may be read-only, so they can't be customized\).

7.  Define availability: Customize how and when the skill capability will exist and be available.

    |Options for Define Availability|Description|
    |-------------------------------|-----------|
    |**Skill is always available**|The skill is available without conditions.|
    |**Customize skill availability**|The skill is available only when conditions are met. Select appropriate conditions from the condition builder. Example: `[Actual start] [On] [Today]`.|

8.  Define access: Configure the access controls by updating ACLs and roles.

    Roles can be added by entering the name of the role in the User roles field. Existing roles can be removed by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many as you like.

9.  Select display: select the instance location where you'd like to display the skill.

    Options vary from skill to skill. Some options are only available for certain skills.

    -   **In-product desktop**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **ServiceNow Otto panel**: When selected, the AI skills are available in the ServiceNow Otto panel. If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md).
    -   **Core UI**: When selected, the AI skill will display as a UI action in the Core UI.
    \[Omitted image "activate-skill-step-2.png"\] Alt text: Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.

10. Review and activate: Review your the details of your configuration, then select **Activate** to complete.


## What to do next

Use the ServiceNow Otto applications and skills that you've activated.

-   **[Configure chat summarization and chat reply recommendation skills in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-chat-summarization-in-the-now-assist-admin-console.md)**  
Define the triggers, inputs, and display location for chat summarization and chat reply recommendation by using the guided setup in the AI Admin Hub console. The activation steps are conceptually same for both the skills.
-   **[Configure email reply recommendation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-email-recommendation.md)**  
Configure the email recommendation Now Assist skill to enable agents to draft email replies based on contextual information.

**Parent Topic:**[Using AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/using-now-assist-admin_0.md)

