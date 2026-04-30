---
title: Configure promoted topics for Conversational Integration with Slack
description: Configure promoted topics to push out important, common topics for users' quick consumption during a conversation with the Slack bot. You can configure up to six different promoted topics to be displayed on the Slack channel greeting message.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-06"
reading_time_minutes: 2
keywords: [Virtual Agent, Slack, Conversational Integration, bot, configure, promoted, topics, Conversational Interfaces, Custom greetings]
breadcrumb: [Conversational Integration with Slack, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure promoted topics for Conversational Integration with Slack

Configure promoted topics to push out important, common topics for users' quick consumption during a conversation with the Slack bot. You can configure up to six different promoted topics to be displayed on the Slack channel greeting message.

## Before you begin

Role required: admin or va\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  On the Virtual Agent settings page, navigate to the Custom greetings and setup and select **View All**.

    The promoted topics that you have previously configured reside in the default chat experience. For more information, see [Configure a Virtual Agent chat experience](configure-default-chat-experience.md). If default chat experience is the only row that you have on your instance, then you observe that the promoted topics will be applied to chat widget, Microsoft Teams, and Slack \(unless you configure something unique for Slack as instructed below.\)

    If you want to set up unique promoted topics for Slack that have to be different from the chat widget, follow the procedure below.

3.  On the Custom Greetings &amp; Setup page, select **New**.

4.  On the form, fill in the fields.

<table id="table_ekz_gnx_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the chat experience. For example, Slack chat experience.

</td></tr><tr><td>

Description

</td><td>

Description of the chat experience.

</td></tr><tr><td>

Active

</td><td>

Enable or disable the chat experience.

</td></tr><tr><td>

Order

</td><td>

Order for the promoted topics to appear on the chat.

</td></tr><tr><td>

Domain

</td><td>

Application scope of the chat experience.

</td></tr><tr><td>

Condition Mode

</td><td>

Situation where your user gets this chat experience.Available Conditions Modes:

-   **Advanced**
-   **Simple**


</td></tr><tr><td>

Condition

</td><td>

Condition that defines the condition mode for the chat experience.Set up a simple condition with **\[devicetype\] \[is\] \[slack\]**.

 **Note:** If you set up **\[devicetype\] \[is\] \[teams\]** in the Condition pop up with a higher order than the default chat experience, then Slack picks up the setup topics and promoted topics defined in this experience.

This change will not affect chat widget, which is still going to inherit the setup topics and promoted topics defined in the default chat experience.

</td></tr></tbody>
</table>5.  Select **Create custom experience**.

6.  Add promoted topics in the Slack chat experience form that you created.

    Review the character length of your promoted topics before adding them for Slack. When the text in the topic gets closer to ~30 characters, the text may get truncated. For more information, see [Slack document](https://api.slack.com/reference/block-kit/block-elements#button).

    1.  On the Slack chat experience form, select the **Promoted Topics** tab and select **Add topic**.

    2.  On the form, fill in the fields.

<table id="table_gkr_sqx_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Topic

</td><td>

Name of the topic being chosen.Use the Search icon to choose a topic.

</td></tr><tr><td>

Order

</td><td>

Provide the order for the topic chosen.

</td></tr></tbody>
</table>        **Note:** Similar to the chat widget, you can configure a maximum of six promoted topics for the Slack channel.

    3.  Select **Save.**


## What to do next

Start a conversation with the Slack bot and you should be able to see the promoted topics after the greeting message that you have setup for the Slack channel.

In you have not configured the promoted topics for Slack, then the promoted topics from the default chat experience are displayed.

