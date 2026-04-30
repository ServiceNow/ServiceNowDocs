---
title: Configure Virtual Agent settings for Slack
description: Configure your Slack bots that are integrated with the Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure Virtual Agent settings for Slack

Configure your Slack bots that are integrated with the Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, click **View All**.

3.  On the Channels and integrations page, in the Slack tile, click **Manage**.

4.  Select the **Settings** tab.

5.  Slide the **Enable Notification for all users** toggle switch to disable notifications for the linked users.

    **Note:**

    -   The **Enable Notification for all users** toggle switch is selected by default.
    -   The **Automatically Link ServiceNow user profiles** toggle switch is selected by default and disabled for any further change. This option links all the active ServiceNow accounts automatically to the associated Microsoft Teams bot.
6.  Set up the **Global Messaging Settings**.

    **Note:** Any changes made to these settings will reflect in all the channels.

    -   **System Messages**: Customize the default system messages displayed during Virtual Agent conversations.

        For more information about changing or updating a system message, see [Change system messages](../../conversational-interfaces/task/ac-change-system-messages.md).

    -   **Contextual Actions**: Customize the supported actions per user command inputs.

        For more information about updating a contextual action, see [Contextual actions for custom chat integrations](../reference/contextual-actions.md#).


-   **[Configure branding for your Virtual Agent bot in Slack](slack-branding-overview.md)**  
You have the flexibility to customize the default ServiceNow branding for your Slack Virtual Agent. You can change the production bot's name and icon.
-   **[Configure branding for your self-configured bot](slack-brand-self-configured.md)**  
Configure your self-configured Slack app's branding. You have the flexibility to customize the default ServiceNow branding for the Slack self-configured bot name and icon.
-   **[Pre-link Virtual Agent requesters before integration with Slack](prelink-va-users-integ-slack.md)**  
Pre-link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Slack. Batch pre-linking enables your Virtual Agent users immediately to chat with a virtual agent and receive notifications without going through the initial authentication linking process.
-   **[Configure promoted topics for Conversational Integration with Slack](configure-slack-promoted-topics.md)**  
Configure promoted topics to push out important, common topics for users' quick consumption during a conversation with the Slack bot. You can configure up to six different promoted topics to be displayed on the Slack channel greeting message.

**Parent Topic:**[Conversational Integration with Slack](mssg-slack.md)

