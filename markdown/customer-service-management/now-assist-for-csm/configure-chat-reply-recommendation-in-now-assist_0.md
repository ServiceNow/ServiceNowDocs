---
title: Configure chat recommendation
description: Use the guided setup in the Now Assist Admin console to configure chat recommendation by defining triggers, specifying inputs, setting the display location, and activating the feature.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure chat recommendation

Use the guided setup in the Now Assist Admin console to configure chat recommendation by defining triggers, specifying inputs, setting the display location, and activating the feature.

Configure chat recommendation skill 

## Before you begin

Role required: admin

Using the chat recommendation skill, you have the options to:

-   Generate a recommended reply based on the context of the conversation.
-   Refine the recommendation by elaborating or shortening the response.

## Procedure

1.  Navigate to **All &gt; Now Assist Admin &gt; Skills**.

    If you’re already in the Now Assist Admin, select the Now Assist Skills tab.

2.  On the navigation panel, select **Customer**.

    Each workflow contains feature sets.

3.  Select **CSM** as the product.

4.  Select **Activate Skill** for the Chat Recommendation skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

5.  Go to **Define Triggers**, the first step in the guided setup.

    By default, many of the options in the setup are configured for the most common use cases. You might need to select the step in the guided setup navigation to go back and change the configurations in previous steps. You can also use Back to navigate through the steps.

6.  Using the toggles, select the actions trigger for the Chat Recommendation skill.

7.  Select **Choose Input** and review the portal and channel selections that determines where data is pulled from.

    **Note:** You cannot modify or deselect default skill input data sources.

8.  Select any additional data sources that you want the Large Language Model \(LLM\) to take into account when generating a recommendation.

9.  Select a portal for the data source to allow chat recommendation to be generated for the conversation occurring on that portal.

    This is a mandatory step. The admin must specify a portal and enable a specific channel on the Choose Input page to enable the skill for chats sent in the selected portal or channel. Otherwise, the agent will receive an error message: “Chat summaries won’t appear until your IT administrator completes all the required steps involved in the setup".

10. Select **Define Availability** to customize how and when the skill capability will exist and be available.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
11. Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

12. Go to **Select display**, the last step, and select where you would like to display the skill.

    You can select both in-product, Now Assist panel, or both.

    **Note:** Chat recommendation is not available in the Now Assist panel.

    -   **In-product desktop**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. Select the down arrow to identify the roles that can use the skill. Select the arrow next to toggle, to select roles who can access the skill. You can add roles by entering the name of the role in the **User roles** field. You can remove existing roles by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many roles as you like.
13. Review your choices and complete the configuration by selecting **Activate**.


## Result

Chat recommendation for the workflow is active on the instance.

