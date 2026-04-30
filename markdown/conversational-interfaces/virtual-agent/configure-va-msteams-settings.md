---
title: Configure Virtual Agent settings for Microsoft Teams
description: Configure your Microsoft Teams bots that are integrated with Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure Virtual Agent settings for Microsoft Teams

Configure your Microsoft Teams bots that are integrated with Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

3.  On the Channels and integrations page, in the Microsoft Teams tile, select **Manage**.

4.  Select the **Settings** tab.

5.  In the Enable Link Authentication section, configure the different link opening experiences using Smart Links.

    For more information about enabling link authentication for your Microsoft Teams bots, see [Configure link authentication and opening experience in Microsoft Teams](link-opening-authentication-msteams.md).

6.  Swipe to the left the **Enable Notification for all users** toggle button to disable notifications for the linked users.

    **Note:** The **Enable Notification for all users** toggle button is selected by default.

    The **Automatically Link ServiceNow user profiles** toggle button is selected by default and disabled for any further change. This option links all the active ServiceNow accounts automatically to the associated Microsoft Teams bot.

7.  Set up the **Global Messaging Settings**.

    **Note:** Any changes made to these settings will reflect in all the channels.

    -   **System Messages**: Customize the default system messages displayed during Virtual Agent conversations.

        For more information about changing or updating a system message, see [Change system messages](../../conversational-interfaces/task/ac-change-system-messages.md).

    -   **Contextual Actions**: Customize the supported actions per user command inputs.

        For more information about updating a contextual action, see [Contextual actions for custom chat integrations](../reference/contextual-actions.md#).


## What to do next

The Virtual Agent bot and Microsoft Teams tenant are now integrated for use on your ServiceNow instance. Your messaging users are automatically linked to their ServiceNow accounts.

-   Notify your users that the Virtual Agent bot for Microsoft Teams is available for use.
-   To improve the live agent experience for your users, you can activate the display of the estimated wait time for live chat support. When a user asks to chat with a live agent, a card shows the approximate wait time to talk with an agent, and gives the user the option to cancel the chat. For details on activating this feature, see [Configure Agent Chat](../../conversational-interfaces/task/ac-configure-agent-chat.md).

