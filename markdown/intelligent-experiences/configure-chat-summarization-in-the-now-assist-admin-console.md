---
title: Configure chat summarization in the Now Assist Admin console
description: Define the triggers, inputs, and display location for chat summarization by using the guided setup in the Now Assist Admin console.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-11-18"
reading_time_minutes: 3
keywords: [Configure, chat, summarization, Now Assist Admin, console, technology, trigger, skill, input]
breadcrumb: [Activate a Now Assist skill, Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Configure chat summarization in the Now Assist Admin console

Define the triggers, inputs, and display location for chat summarization by using the guided setup in the Now Assist Admin console.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Features**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Features** tab.

2.  On the navigation panel, select a workflow that has chat summarization, either **Technology** or **Customer**.

    Each workflow contains feature sets.

3.  On the Chat feature card, select **View details**.

4.  In the All available Chat skills section of the chat summarization card, select **Activate Skill**.

5.  Go to **Define Trigger**, the first step in the guided setup.

    By default, many of the options in the setup are configured for the most common use cases. You might need to select the step in the guided setup navigation to go back and change the configurations in previous steps. You can also use the **Back** button to navigate through the steps.

6.  Using the toggles, select what actions trigger the chat summarization skill.

    ![Triggers selected for Now Assist chat summarization.](../image/na-chat-summarization-trigger.png)

7.  Select whether you want the summary to be formatted with bullet points.

    By default, the summaries are written with bullet points, but you can turn off this format so that the generated summary uses paragraphs instead.

8.  Go to **Choose Input**, the next step, by selecting **Save and continue**.

9.  Select any additional data sources that you want the large language model \(LLM\) to take into account when generating a summary.

    By default, the summary takes the information from the conversation as the source of the input data.

    Selecting a portal as a data source also allows users to trigger chat summarization from the portal. If you do not select a portal, then chat summarization will not be accessible to users on that portal. Similarly, channels must be enabled as data sources before they are accessible to users.

    ![Inputs selected for Now Assist chat summarization.](../image/na-chat-summarization-input-channels.png)

10. Select **Save and continue**.

11. Go to **Select display**, the last step, and select where you would like to display the skill.

    You can select both in-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](activate-now-assist-panel.md).

        Select the down arrow to identify the roles that can use the skill.

    Select the arrow near the toggle to select roles for who can access the skill. You can add roles by entering the name of the role in the **User roles** field. You can remove existing roles by selecting the X icon in the role bubble. You must have at least one role specified, but you can add as many roles as you like.

    **Note:** You can use different roles for chat summarization in different workflows. You can see which workflow you're configuring by checking the label next to the skill name at the top of the guided setup, such as "ITSM" or "HRSD."

    ![Select display step of the Now Assist incident summarization skill configuration prompts you to define where the skill is displayed, either in-product, in the Now Assist panel, or both.](../image/na-chat-summarization-display.png)

12. Review your choices and complete the configuration by selecting **Activate**.

    ![Review and activate step for Now Assist chat summarization.](../image/na-chat-summarization-review.png)


## Result

Chat summarization for the workflow is active on the instance.

## What to do next

Analyze your skill performance on the Now Assist Admin console to help determine the success of the skill. Learn more about tracking your Now Assist usage at [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Activate a Now Assist skill](configure-a-now-assist-skill.md)

