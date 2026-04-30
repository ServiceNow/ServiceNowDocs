---
title: Configure promoted topics for Conversational Integration with Microsoft Teams
description: Configure promoted topics to push out important, common topics for users' quick consumption during a conversation with the Microsoft Teams bot. You can configure up to six different promoted topics to be displayed on the Microsoft Teams channel greeting message.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Promoted, topics, Virtual Agent, Conversational Integration, Microsoft Teams, MSTeams, bot]
breadcrumb: [Configure VA for Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure promoted topics for Conversational Integration with Microsoft Teams

Configure promoted topics to push out important, common topics for users' quick consumption during a conversation with the Microsoft Teams bot. You can configure up to six different promoted topics to be displayed on the Microsoft Teams channel greeting message.

## Before you begin

Role required: admin or va\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

2.  In **Virtual Agent settings** under **Custom greetings and setup**, select **View All**.

    The promoted topics that you have previously configured will reside in the default chat experience. For more information, see [Configure a Virtual Agent chat experience](configure-default-chat-experience.md). If default chat experience is the only row that you have on your instance, then you observe that the promoted topics will be applied to chat widget, Microsoft Teams, and Slack \(unless you configure something unique for Microsoft Teams as instructed below.\)

    If you want to set up unique promoted topics for Microsoft Teams that have to be different from the chat widget, follow the procedure below.

3.  In the Custom Greetings &amp; Setup page, select **New**.

4.  On the form, fill in the fields.

<table id="table_ekz_gnx_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the chat experience. For example, Microsoft Teams chat experience.

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

Condition that defines the condition mode for the chat experience.Set up a simple condition with **\[devicetype\] \[is\] \[teams\]**.

 **Note:** If you set up **\[devicetype\] \[is\] \[teams\]** in the Condition pop up with a higher order than the default chat experience, then Microsoft Teams picks up the setup topics and promoted topics defined in this experience.

This change will not affect chat widget, which is still going to inherit the setup topics and promoted topics defined in the default chat experience.

</td></tr></tbody>
</table>5.  Select **Create custom experience**.

6.  Add promoted topics in the Microsoft Teams chat experience form that you created.

    1.  On the Microsoft Teams form, select the **Promoted Topics** tab, and select **Add topic**.

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
</table>        **Note:** Similar to chat widget, you can configure a maximum of six promoted topics for the Microsoft Teams channel.

    3.  Selecto **Save.**


## What to do next

Start a conversation with the Microsoft Teams bot and you should be able to see the promoted topics after the greeting message that you have setup for the Microsoft Teams channel.

In you have not configured the promoted topics for Microsoft Teams, then the promoted topics from the default chat experience are displayed.

**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

