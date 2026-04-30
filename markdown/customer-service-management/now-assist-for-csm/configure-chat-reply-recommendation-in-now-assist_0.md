---
title: Configure chat recommendation
description: Configure chat recommendation by defining triggers, specifying inputs, setting the display location, and activating the feature.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure chat recommendation

Configure chat recommendation by defining triggers, specifying inputs, setting the display location, and activating the feature.

Configure chat recommendation skill 

## Before you begin

Role required: admin

Using the chat recommendation skill, you have the options to:

-   Generate a recommended reply based on the context of the conversation.
-   Refine the recommendation by elaborating or shortening the response.

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt;Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Chat reply generation** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Define Triggers** and switch the toggle to choose how and when the summarization is configured.

5.  Select **Choose Input** and review the portal and channel selections that determines where data is pulled from.

    **Note:** You cannot modify or deselect default skill input data sources.

6.  Select any additional data sources that you want the Large Language Model \(LLM\) to take into account when generating a recommendation.

7.  Select a portal for the data source to allow chat recommendation to be generated for the conversation occurring on that portal.

    This is a mandatory step. The admin must specify a portal and enable a specific channel on the Choose Input page to enable the skill for chats sent in the selected portal or channel. Otherwise, the agent will receive an error message: “Chat summaries won’t appear until your IT administrator completes all the required steps involved in the setup".

8.  Select **Define Availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
9.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default roles sn\_customerservice\_agent and sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

10. Toggle **Display** to determine if chat recommendation appears in In-product desktop, displaying Now Assist skills on forms and workspaces.

11. After selecting **Review and Activate** to examine changes, select **Done** to close the Chat reply generation settings.

12. Select **Activate** to turn on the skill for agents and complete configuration.


## Result

Chat recommendation for the workflow is active on the instance.

