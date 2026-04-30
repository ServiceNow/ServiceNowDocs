---
title: Configure Virtual Agent settings for Slack
description: Configure your Slack bots that are integrated with the Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Conversational Integration with Slack, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
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


