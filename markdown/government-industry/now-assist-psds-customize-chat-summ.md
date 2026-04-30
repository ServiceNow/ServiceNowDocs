---
title: Configure chat summarization skill in Now Assist for Public Sector Digital Services \(PSDS\)
description: If you have the admin role, you can configure the Now Assist for Public Sector Digital Services \(PSDS\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Public Sector Digital Services Core UI.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Configure chat summarization skill in Now Assist for Public Sector Digital Services \(PSDS\)

If you have the admin role, you can configure the Now Assist for Public Sector Digital Services \(PSDS\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Public Sector Digital Services Core UI.

## Before you begin

Role required: admin

## About this task

Agents can utilize chat summarization, powered by Now LLM, to gain contextual understanding of support issues throughout a chat's lifecycle, even if it involves virtual agent interactions, transfers to live agents, or multiple hand-offs between agents.

In the Now Assist for PSDS Admin Console, admins can:

-   Define the trigger that determine when a summary is generated \(chat handoff, quick action, wrap-up\)
-   Define where to display \(CSM Workspace and/or Now Assist panel\)
-   Add/remove roles to control who can view the skill

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the dropdown, select **Customer** &gt; **PSDS**.

    ![Now Assist Panel showing NA skills and features in PSDS](../image/now-assist-psds-panel.png)

3.  On the Chat feature card, select **View Details**, then select **Chat Summarization** under Active Skills.

    By default, the chat summarization skill is activated for Now Assist for PSDS. If it is not active, select **Activate Skill** in the All available Chat skills section of the chat recommendation card.

4.  Select **Define Trigger**, the first step in the guided setup.

    By default, many of the options in the setup are configured for the most common use cases. You can use the **Back** button to navigate through the steps.

5.  Using the toggles, select what actions trigger the chat recommendation skill.

6.  Select whether you want the summary to be formatted with bullet points.

    By default, summaries are written with bullet points, but can be configured to appear in paragraph form by toggling this off.

7.  Go to **Choose Input** by selecting **Save and continue**.

8.  Select any additional data sources that you want the large language model \(LLM\) to take into account when generating the chat summary.

9.  Select any additional portals to allow chat summaries to be generated for conversations occurring on that portal.

    **Note:** If **Add Additional Data Sources** is toggled on, the admin **must** specify a portal and enable a specific channel in the Portals dropdown for the requester to be able to initiate the chat on that portal. Otherwise, the agent will receive an error message. By default, Government Service Portal \(GSP\) for PSDS is selected as the portal, and cannot be deselected.

10. Select **Save and continue**.

11. Go to **Select display**, and select where you would like to display the skill.

    You can select both in-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

        Select the down arrow to configure the user roles that can access the skill.

    Select the arrow near the toggle to select roles for who can access the skill. You can add roles by entering the name of the role in the **User roles** field. You can remove existing roles by selecting the **X** icon in the role bubble. You must have at least one role specified, but you can add as many roles as you like.

12. Review your choices and select **Activate** to complete the skill configuration.

    ![Review and activate step for Now Assist chat summarization.](../image/chat-summarization-activate-now-assist-psds.png)


## Result

Chat summarization is active and customized for the desired workflow.

## What to do next

Review the performance of the Now Assist for PSDS chat summarization skill on the Now Assist Admin console. Learn more about tracking your Now Assist usage at [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

