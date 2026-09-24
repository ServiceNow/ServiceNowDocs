---
title: Integrating Virtual Agent with messaging apps
description: Enable users to run Virtual Agent bot conversations in supported third-party messaging apps. Use the Conversational Integration apps for Slack, Microsoft Teams, and Workplace that are available from the ServiceNow Store to configure these messaging apps on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/va-integration-messaging-apps.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with messaging apps

Enable users to run Virtual Agent bot conversations in supported third-party messaging apps. Use the Conversational Integration apps for Slack, Microsoft Teams, and Workplace that are available from the ServiceNow Store to configure these messaging apps on your ServiceNow instance.

**Note:** Conversational Integration apps for Slack, Microsoft Teams, and other consumer apps and voice apps are not supported for on-prem instances.

## Admin setup

Use the Virtual Agent Conversational Integration apps to configure the messaging applications for your instance. Perform these basic installation steps to set up the Virtual Agent bot.

1.  Install the Conversational Integration messaging apps, that are pre-built with ServiceNow Virtual Agent from the ServiceNow Store and then associate the app with your own ServiceNow instance.

    For details, see [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md).

2.  Install the Conversational Integration apps for Slack, Microsoft Teams, Twilio, WhatsApp, and Google Assistant on your ServiceNow instance once they become available for installation from the ServiceNow Store.

    \[Omitted image "channels-and-integrations.png"\] Alt text: Channels and integrations in the Conversational Interfaces general settings portal.

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

    You can modify the default messages displayed to your users in Virtual Agent and Agent Chat conversations. For details about customizing them, see [Change Virtual Agent and Agent Chat system messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-change-system-messages.md).

-   **Rendering of input controls and bot responses in conversations**

    Input controls in Assistant Designer, such as the Carousel, render differently in bot conversations in messaging apps than in the web-based interface. Certain bot response controls, such as the Image response and Multi-response controls, also render differently in third-party messaging apps. For details about these differences, see the descriptions of the Assistant Designer [input controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-user-inputs.md), [bot responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-bot-responses.md), and [utilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-utilities.md).

-   **Attachments**

    In live agent conversations, users and agents can upload and exchange any type of attachment file when prompted.


## ServiceNow Otto support

|Existing channel integrations|Supports ServiceNow Otto|Supports synthesized response|
|-----------------------------|------------------------|-----------------------------|
|Microsoft Teams/Copilot|Yes|Yes|
|Slack|Yes|Yes|
|WhatsApp|Yes|No|
|SMS/Twilio|Yes|No|
|Google Chat|Yes|No|

-   **[Redirect user authentication to a Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/set-user-linkage.md)**  
After installing a pre-built Conversational Integration, you can specify a Service Portal in which unauthenticated end users complete the user authentication step \(user account linking\), instead of in their ServiceNow instance. Users who do not have linked accounts complete authentication before continuing with Virtual Agent in the messaging application.
-   **[Account linking in pre-built messaging integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-adapter-autolinking.md)**  
In Virtual Agent, account linking maps the users of a supported chat or messaging application to their ServiceNow user profile. Account auto-linking authenticates your messaging users, which enables users to automatically access Virtual Agent topics that involve ServiceNow records. If needed, users can also manually unlink from or link to their ServiceNow accounts.
-   **[Control topic visibility in Virtual Agent messaging channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/control-topic-visibility-channel.md)**  
Suppress the display of a topic in a Virtual Agent messaging channel by using a condition script that excludes the topic from a channel.
-   **[Conversational Integration with Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/integration-apple-mssg.md)**  
Use the Conversational Integration with Apple Messages for Business application to empower customers to engage with your business using their Apple devices. Conversational Integration with Apple Messages for Business provides rich messaging capabilities such as Apple pay, forms, time picker, and authentication.
-   **[Conversational Integration with Facebook Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/messg-fbm.md)**  
Use this application to empower customers to engage with your business using Facebook Messenger.
-   **[Conversational Integration with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/gchat-conv-integration.md)**  
Enable requesters to chat with Google Chat or live agents using the Google Chat application. Use the Conversational Integration with Google Chat app, available from the ServiceNow Store, to associate your instance with Google Chat.
-   **[Conversational Integration with LINE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/messg-line.md)**  
Conduct user-initiated, system-initiated, or agent-initiated conversations using the Conversational Integration with LINE application. The application connects a requester with a virtual agent or live agent using your company's LINE account.
-   **[Conversational Integration with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/teams-conv-integration.md)**  
Enable requesters to chat with Microsoft Teams or live agents using the Microsoft Teams application. Use the Conversational Integration with Microsoft Teams app, available from the ServiceNow Store, to associate your instance with Microsoft Teams.
-   **[Conversational Integration with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/mssg-slack.md)**  
Use the Conversational Integration with Slack application to connect your requesters with Virtual Agent or live agents through your company’s Slack workspace.
-   **[Conversational SMS Integration with AWS End User Messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversational-sms-integration-amazon.md)**  
Install the Conversational SMS with AWS End User Messaging \(sn\_sms\_aws\_adapter\) plugin from the ServiceNow Store to enable users to connect to customer support agents via SMS using the Amazon End User Messaging as the SMS provider.
-   **[Conversational SMS Integration with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/sms-twilio-store-app.md)**  
Use this ServiceNow Store application to host Virtual Agent conversations on Twilio SMS to chat with virtual agent or live agents.
-   **[Conversational Integration with WhatsApp \(powered by Twilio\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/messg-whatsapp-twilio.md)**  
Use this application to enable requesters to interact on WhatsApp chat with a virtual agent or live agent. The application connects a requester with a virtual agent or live agent using your company's WhatsApp-enabled Twilio phone number.
-   **[Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/messg-direct-whatsapp.md)**  
Use this application to enable requesters to interact on WhatsApp chat with a Virtual Agent or live agent. The application connects a requester with a Virtual Agent or live agent using your company's WhatsApp business phone number.

**Parent Topic:**[Conversational Integration apps for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/integrate-virtual-agent.md)

