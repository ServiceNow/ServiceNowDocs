---
title: Configure Virtual Agent for Microsoft Teams
description: Configure your Microsoft Teams bots that are integrated with Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure Virtual Agent for Microsoft Teams

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

-   **[Configure branding for your ServiceNow Virtual Agent bot in Microsoft Teams](configure-msteams-branding.md)**  
Enable users to configure branding for the published Microsoft Teams bot app, the ServiceNow® Virtual Agent. Users are provided with the flexibility to customize the default ServiceNow branding for the Microsoft Teams production bot name and icon.
-   **[Configure link authentication and opening experience in Microsoft Teams](link-opening-authentication-msteams.md)**  
Link authentication and opening experience in Microsoft Teams provides a seamless experience for end users to interact with ServiceNow links when you use Virtual Agent on Microsoft Teams.
-   **[Installing Microsoft Teams for all Virtual Agent users](prelink-va-users-integ-msteams.md)**  
Pre-link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Microsoft Teams. Batch pre-linking enables your Virtual Agent users to immediately chat with a virtual agent and receive notifications without going through the initial authentication linking process.
-   **[Activate Now Assist in Virtual Agent for Microsoft Teams](activate-na-va-msteams.md)**  
Add Now Assist in Virtual Agent to your Microsoft Teams and Microsoft Copilot bot.
-   **[Customize auto-linking for Conversational Integration with Microsoft Teams](customize-autolink-msteams.md)**  
Customize auto-linking for user profiles by defining the email Id of the user in any custom table rather than just the User \[sys\_user\] table.
-   **[Configure promoted topics for Conversational Integration with Microsoft Teams](configure-teams-promoted-topics.md)**  
Configure promoted topics to push out important, common topics for users' quick consumption during a conversation with the Microsoft Teams bot. You can configure up to six different promoted topics to be displayed on the Microsoft Teams channel greeting message.
-   **[Configure Microsoft Teams Message Extension](configure-msteams-msg-extension.md)**  
Configure Microsoft Teams Message Extension to enable users to use AI Search to find content \(Knowledge articles and catalog items\), and share information in a one-on-one or group chat. For the base system Virtual Agent integration with Microsoft Teams, this feature is enabled by default.
-   **[Configure Microsoft Azure Conditional Access for Microsoft Teams tenant](msteams-setup-conditional-access.md)**  
You must configure conditional access in Microsoft Azure to restrict users from accessing the production applications. Conditional access helps you from accidentally overriding your production integration with a custom or personal instance integration.
-   **[Set up your language preferences for the Virtual Agent integration with Microsoft Teams](va-integration-msteams-localization.md)**  
Set language preferences so that Virtual Agent is in the same language as the user's preferred Microsoft Teams language.
-   **[Localize the bot messages](localize-bot-messg.md)**  
Localize the bot messages to receive them in a language of your choice during your conversations with the bot.

**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams](../concept/teams-conv-integration.md)

