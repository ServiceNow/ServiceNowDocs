---
title: Virtual Agent integration with messaging apps
description: Enable users to run Virtual Agent bot conversations in supported third-party messaging apps. Use the Conversational Integration apps for Slack, Microsoft Teams, and Workplace that are available from the ServiceNow Store to configure these messaging apps on your ServiceNow instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent integration with messaging apps

Enable users to run Virtual Agent bot conversations in supported third-party messaging apps. Use the Conversational Integration apps for Slack, Microsoft Teams, and Workplace that are available from the ServiceNow Store to configure these messaging apps on your ServiceNow instance.

**Note:** Conversational Integration apps for Slack, Microsoft Teams, and Workplace, other consumer apps and voice apps are not supported for on-prem instances.

## Admin setup

Use the Virtual Agent Conversational Integration apps to configure the messaging applications for your instance. Perform these basic installation steps to set up the Virtual Agent bot.

1.  Install the Conversational Integration messaging apps, that are pre-built with ServiceNow Virtual Agent from the ServiceNow Store and then associate the app with your own ServiceNow instance.

    For details, see [Integrating Virtual Agent with enterprise messaging apps](../task/integ-va-enterprise-apps.md).

2.  Install the Conversational Integration apps for Slack, Microsoft Teams, and Workplace, LINE, Twilio, WhatsApp, Facebook Messenger, Alexa, Google Assistant, Google Business Messages, Amazon Connect, on your ServiceNow instance once they become available for installation after installing from the ServiceNow Store.

    ![Channels and integrations in the Conversational Interfaces general settings portal.](../images/channels-and-integrations.png "Channels and integrations")

3.  If needed, configure the system messages that users see in Virtual Agent conversations. You can also customize the common commands used in these messaging integrations.

## Conversational interface in messaging integrations

The Virtual Agent interface for the Conversational Integration apps \(Slack, Microsoft Teams, and Workplace\) is similar to the web-based interface. However, there are some differences, such as commands used and how certain interface controls are displayed in these third-party messaging apps.

-   **Common commands in messaging integrations**

    |Command|Description|
    |-------|-----------|
    |`Hi`|Begin a new conversation or end a conversation.|
    |`agent`|Begin a new conversation or request a transfer to a live agent.|
    |`bye`|Leave a live chat conversation at any time, for example before engaging with a live agent, during a live chat, or when live chat is about to end.|
    |`help`|Displays a short list of useful commands.|
    |`logout`|Unlink your ServiceNow account from a messaging integration.|
    |`notification or notifications`|Subscribe to or unsubscribe from notifications.|
    |`restart`|End the current conversation and begin a new one.|

    After you install the integration, you can customize these commands by using the **Configure** button for the installed teams/communities in the channel specific pages.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.
    2.  In **General Settings** under **Channels and integrations**, click **View All**.
    3.  On the Channels and integrations page, you can see the number of integrated channels and available channels for installation on your instance.
    4.  Click the **Manage** button in the specific channel and navigate to the Settings tab.
    5.  Click the **view settings** button against Contextual Actions.
    6.  Select the command record to be changed and update as needed.
-   **Configuring Virtual Agent system messaging in the Conversational Integration apps**

    You can modify the default messages displayed to your users in Virtual Agent and Agent Chat conversations. For details on customizing them, see [Change Virtual Agent and Agent Chat system messages](../../conversational-interfaces/task/ac-change-system-messages.md).

-   **Rendering of input controls and bot responses in conversations**

    Input controls in Virtual Agent Designer, such as the Carousel render differently in bot conversations in messaging apps than in the web-based interface. For example, the Date Time picker control in Workplace presents buttons for users to select a date and time. Similarly, certain bot response controls, such as the Image response and Multi-response controls, also render differently in third-party messaging apps. For details on these differences, see the descriptions of the Virtual Agent Designer [input controls](../reference/va-user-inputs.md), [bot responses](../reference/va-bot-responses.md), and [utilities](../reference/va-utilities.md).

-   **Attachments**

    In live agent conversations, users and agents can upload and exchange any type of attachment file when prompted.


## Now Assist support

|Existing channel integrations|Supports Now Assist|Supports synthesized response|
|-----------------------------|-------------------|-----------------------------|
|Microsoft Teams/Copilot|Yes|Yes|
|Slack|Yes|Yes|
|WhatsApp|Yes|No|
|SMS/Twilio|Yes|No|
|IVR with Amazon Connect|Yes|No|
|AWS end user messaging|Yes|No|
|Workplace by Facebook|No|No|
|Facebook Messenger|No|No|
|Apple Business Chat|No|No|
|LINE|No|No|
|IBM Watson Assistant|No|No|
|Alexa|No|No|

