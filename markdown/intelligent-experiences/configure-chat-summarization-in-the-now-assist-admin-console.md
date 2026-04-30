---
title: Configure chat summarization and chat reply recommendation skills in the Now Assist Admin console
description: Define the triggers, inputs, and display location for chat summarization and chat reply recommendation by using the guided setup in the Now Assist Admin console. The activation steps are conceptually same for both the skills.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Configure, chat, summarization, Now Assist Admin, console, technology, trigger, skill, input]
breadcrumb: [Activate a Now Assist skill, Using Now Assist Admin, Now Assist, Enable AI experiences]
---

# Configure chat summarization and chat reply recommendation skills in the Now Assist Admin console

Define the triggers, inputs, and display location for chat summarization and chat reply recommendation by using the guided setup in the Now Assist Admin console. The activation steps are conceptually same for both the skills.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Features**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Features** tab.

2.  On the navigation panel, select a workflow that has chat recommendation, either **Technology** or **Customer**.

    Each workflow contains feature sets.

3.  On the Chat feature card, select **View details**.

4.  In the All available Chat skills section of the chat recommendation card, select **Activate Skill**.

5.  Go to **Define Trigger**, the first step in the guided setup.

    By default, many of the options in the setup are configured for the most common use cases. You might need to select the step in the guided setup navigation to go back and change the configurations in previous steps. You can also use **Back** to navigate through the steps.

6.  Using the toggles, select the actions trigger the chat recommendation skill.



    ![Triggers selected for Now Assist chat recommendation.](../image/na-chat-summarization-trigger.png)

7.  Using the toggles, select the actions trigger the chat summarization skill.

    ![Triggers selected for Now Assist chat summarization.](../../now-assist-skills/image/na-chat-summarization-trigger-summ.png "Define triggers for chat summarization")

8.  Select whether you want the summary to be formatted with bullet points.

    By default, the summaries are written with bullet points, but you can turn off this format so that the generated summary uses paragraphs instead.

9.  Go to **Define availability**, the next step, by selecting **Save and continue**.

10. Customize when and how the skill capability will exist and be available.

    ![Define availability for Now Assist chat recommendation](../image/na-chat-summarization-define-availability.png)

11. Select **Customize skill availability** if you want to define the skill to be available for a certain domain.

12. Go to **Choose Input**, the next step, by selecting **Save and continue**.

13. Select any additional data sources that you want the Large language model \(LLM\) to take into account when generating a recommendation.

14. Select a portal for the data source to allow chat summarization/recommendation to be generated for the conversation occurring on that portal.

    This is a mandatory step. The admin must specify a portal and enable a specific channel on **Choose Input** page, to enable the skill for chats sent in the selected portal/channel. Else the agent will receive an error message, "Chat summaries won't appear until your IT administrator completes all the required steps involved in the setup".

    ![Inputs selected for Now Assist chat recommendation.](../image/na-chat-summarization-input.png)

15. Select **Save and continue**.

16. Go to **Select display**, the last step, and select where you would like to display the skill.

    You can select both in-product, Now Assist panel, or both.

    **Note:** Chat recommendation is not available in the Now Assist panel.

    -   **In-product desktop**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. Select the down arrow to identify the roles that can use the skill. Select the arrow next to toggle, to select roles who can access the skill. You can add roles by entering the name of the role in the **User roles** field. You can remove existing roles by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many roles as you like.
    **Note:** You can use different roles for chat recommendation in different workflows. You can see which workflow you're configuring by checking the label next to the skill name at the top of the guided setup, such as "ITSM" or "HRSD."

    ![Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.](../image/na-chat-summarization-display.png)

17. Review your choices and complete the configuration by selecting **Activate**.

    ![Review and activate step for Now Assist chat summarization.](../image/na-chat-summarization-review.png)


## Result

Chat recommendation or reply recommendation for the workflow is active on the instance.

## What to do next

Analyze your skill performance and usage on the Now Assist Admin console to help determine the success of the skill. Learn more about tracking your Now Assist usage at [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Activate a Now Assist skill](configure-a-now-assist-skill.md)

