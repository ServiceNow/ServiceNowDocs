---
title: Configure call summarization
description: Configure Call Summarization to automatically generate summaries of agent-customer calls within the Active Chat window to capture key details for better agent follow-up and record keeping.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure call summarization

Configure Call Summarization to automatically generate summaries of agent-customer calls within the Active Chat window to capture key details for better agent follow-up and record keeping.

## Before you begin

Role required: admin

Call summarization is generated from the information that you enter in the following fields:

-   Conversation Transcript
-   Short Description \(automatically populated at the end of call\)
-   Chat Summary \(automatically populated at the end of call\)
-   Integration setup:

    **Note:** Verify that your telephony or call center system is integrated with ServiceNow if call data needs to be captured directly. For more information, see [Interaction Controls Component \(ICC\) for voice calls](../concept/contact-center-integration-with-icc.md) and [Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](../concept/interaction-controls-component-icc-callback-integration-features.md).Additionally, set your status as **Available** in CSM Configurable Workspace to be able to receive call requests from customers.


Any modifications to the names or labels of these fields can result in issues with summarization generation.

**Note:** You cannot modify a skill's input data source in base system. However, you can [clone the skill](../concept/clone-the-now-assist-for-csm-skills.md#) in Now Assist Skill Kit.

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Now Assist Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Call Summarization** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Define Triggers** and switch the toggles to choose how and when the summarization is configured.

    |Trigger|Description|
    |-------|-----------|
    |Live Agent to Live Agent handoff|Call summary that is generated when the call handoff is done from a live agent to a live agent.|
    |Call wrap-up|Call summary that is generated when the live agent or the user ends the chat. The **Chat summary** field is updated for the interaction.|
    |Short description|**Short description** field that is updated for the interaction when the live agent or the user ends the call.|
    |Task creation|**Short description** and **Description** fields that are auto-populated on the task record when a task is created from an interaction.|

    You can also select toggle a property that controls how a call summary is displayed.

    |Property|Description|
    |--------|-----------|
    |Bulleted list|Call summary as an unordered list.|

5.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role- sn\_customerservice\_agent or sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you must manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still must manually select it in **Select Display** to make it active.

6.  Select **Display** to determine where the resolution notes appear.

    -   Select In-product desktop to display Now Assist skills on forms and workspaces.
    -   Select Now Assist panel to display Now Assist skills in the Now Assist panel.
7.  After selecting **Review and Activate** to examine changes, select **Done** to close the Call Summarization generation settings.

8.  Select **Activate** to turn on the skill for agents and complete the configuration.


