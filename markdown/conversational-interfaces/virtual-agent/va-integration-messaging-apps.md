---
title: Integrating Virtual Agent with messaging apps
description: Enable users to run Virtual Agent bot conversations in supported third-party messaging apps. Use the Conversational Integration apps for Slack, Microsoft Teams, and Workplace that are available from the ServiceNow Store to configure these messaging apps on your ServiceNow instance.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with messaging apps

Enable users to run Virtual Agent bot conversations in supported third-party messaging apps. Use the Conversational Integration apps for Slack, Microsoft Teams, and Workplace that are available from the ServiceNow Store to configure these messaging apps on your ServiceNow instance.

**Note:** Conversational Integration apps for Slack, Microsoft Teams, and Workplace, other consumer apps and voice apps are not supported for on-prem instances.

## Admin setup

Use the Virtual Agent Conversational Integration apps to configure the messaging applications for your instance. Perform these basic installation steps to set up the Virtual Agent bot.

1.  Install the Conversational Integration messaging apps, that are pre-built with ServiceNow Virtual Agent from the ServiceNow Store and then associate the app with your own ServiceNow instance.

    For details, see [Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md).

2.  Install the Conversational Integration apps for Slack, Microsoft Teams, and Workplace, LINE, Twilio, WhatsApp, Facebook Messenger, Alexa, Google Assistant, Amazon Connect, on your ServiceNow instance once they become available for installation after installing from the ServiceNow Store.

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

-   **[Redirect user authentication to a Service Portal](../task/set-user-linkage.md)**  
After installing a pre-built Conversational Integration \(for messaging apps, Consumer apps or voice apps\), you can specify a Service Portal in which unauthenticated end users complete the user authentication step \(user account linking\), instead of in their ServiceNow instance. Users who do not have linked accounts complete authentication before continuing with the virtual agent in the messaging application.
-   **[Account linking in pre-built messaging integrations](va-adapter-autolinking.md)**  
In Virtual Agent, account linking maps the users of a supported chat or messaging application to their ServiceNow user profile. Account auto-linking authenticates your messaging users, which enables users to automatically access Virtual Agent topics that involve ServiceNow records. If needed, users can also manually unlink from or link to their ServiceNow accounts.
-   **[Control topic visibility in Virtual Agent messaging channels](../task/control-topic-visibility-channel.md)**  
Suppress the display of a topic in a Virtual Agent messaging channel by using a condition script that excludes the topic from a channel.
-   **[Conversational Integration with Apple Messages for Business](integration-apple-mssg.md)**  
Use the Conversational Integration with Apple Messages for Business application to empower customers to engage with your business using their Apple devices. Conversational Integration with Apple Messages for Business provides rich messaging capabilities such as Apple pay, forms, time picker, and authentication.
-   **[Conversational Integration with Facebook Messenger](messg-fbm.md)**  
Use this application to empower customers to engage with your business using Facebook Messenger.
-   **[Conversational Integration with Google chat](gchat-conv-integration.md)**  
Enable requesters to chat with Google chat or live agents using the Google chat application. Use the Conversational Integration with Google chat app, available from the ServiceNow Store, to associate your instance with Google chat.
-   **[Conversational Integration with LINE](messg-line.md)**  
Conduct user-initiated, system-initiated, or agent-initiated conversations using the Conversational Integration with LINE application. The application connects a requester with a virtual agent or live agent using your company's LINE account.
-   **[Conversational Integration with Microsoft Teams](teams-conv-integration.md)**  
Enable requesters to chat with Microsoft Teams or live agents using the Microsoft Teams application. Use the Conversational Integration with Microsoft Teams app, available from the ServiceNow Store, to associate your instance with Microsoft Teams.
-   **[Conversational Integration with Slack](../task/mssg-slack.md)**  
Use the Conversational Integration with Slack application to connect your requesters with Virtual Agent or live agents through your company’s Slack workspace.
-   **[Conversational SMS Integration with Twilio](sms-twilio-store-app.md)**  
Use this ServiceNow Store application to host Virtual Agent conversations on Twilio SMS to chat with virtual agent or live agents.
-   **[Conversational Integration with Workplace from Facebook](../task/mssg-workplace.md)**  
Use the Conversational Integration with Workplace from Facebook application to connect your requesters with Virtual Agent or live agents through your company’s Workplace from Facebook application.
-   **[Conversational Integration with WhatsApp \(powered by Twilio\)](messg-whatsapp-twilio.md)**  
Use this application to enable requesters to interact on WhatsApp chat with a virtual agent or live agent. The application connects a requester with a virtual agent or live agent using your company's WhatsApp-enabled Twilio phone number.
-   **[Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](messg-direct-whatsapp.md)**  
Use this application to enable requesters to interact on WhatsApp chat with a Virtual Agent or live agent. The application connects a requester with a Virtual Agent or live agent using your company's WhatsApp business phone number.
-   **[Conversational SMS Integration with AWS End User Messaging](conversational-sms-integration-amazon.md)**  
Install the Conversational SMS with AWS End User Messaging \(sn\_sms\_aws\_adapter\) plugin from the ServiceNow Store to enable users to connect to customer support agents via SMS using the Amazon End User Messaging as the SMS provider.
-   **[Integrating IBM Watson Assistant conversations](va-ibm-watson-assistant-config.md)**  
Use the IBM Watson Assistant topic to enable Virtual Agent to exchange information with conversations that were created in IBM Watson Assistant.

**Parent Topic:**[Integrating Virtual Agent with other channels](integrate-virtual-agent.md)

