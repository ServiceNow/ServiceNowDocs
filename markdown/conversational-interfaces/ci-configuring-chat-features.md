---
title: General chat settings
description: Use the Conversational Interfaces Console to set up the basic chat features shared by Virtual Agent and Agent Chat.
locale: en-US
release: zurich
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [General, chat, settings, Conversational Interfaces, console, Virtual Agent, Agent Chat]
breadcrumb: [Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# General chat settings

Use the Conversational Interfaces Console to set up the basic chat features shared by Virtual Agent and Agent Chat.

<table id="table_kbf_kxv_fsb"><thead><tr><th>

I want to...

</th><th>

See these topics

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Chat Client Display Options

</td></tr><tr><td>

Brand my bot

</td><td>

[Branding your chat client](branding-chat-client.md)

</td></tr><tr><td>

Preview new or unread messages in a minimized chat window

</td><td>

[Enable message preview on the chat widget](../task/web-client-message-preview.md)

</td></tr><tr><td class="sub-head" colspan="2">

Conversation Routing

</td></tr><tr><td>

Configure my bot to run in third-party messaging apps

</td><td>

[Integrating Virtual Agent with messaging apps](../../virtual-agent/concept/va-integration-messaging-apps.md).

</td></tr><tr><td>

Create pre-chat surveys

</td><td>

[Define pre-chat survey configurations](../task/ac-configure-pre-chat-surveys.md)

</td></tr><tr><td>

Create and use context variables to store chat-related information

</td><td>

[Configure context variables for storing chat-related information](../task/ac-configure-context-variables.md)

</td></tr><tr><td>

Display or announce callback options to users through other ServiceNow apps

</td><td>

[Omnichannel Callback](../../omnichannel-callback/concept/omnichannel-callback.md)

</td></tr><tr><td>

Configure topic context intents

</td><td>

[Define topic context intent configurations](../task/ac-configure-context-topic-intent.md)

</td></tr><tr><td class="sub-head" colspan="2">

System Actions

</td></tr><tr><td>

Modify system chat messages

</td><td>

[Change Virtual Agent and Agent Chat system messages](../task/ac-change-system-messages.md)

</td></tr><tr><td>

Specify how links open from the chat window

</td><td>

[URL navigation in Conversational Interfaces](url-navigation-ci.md)

</td></tr><tr><td>

Configure my bot to detect sensitive data

</td><td>

[Configuring Sensitive Data Handler](../task/ac-configure-sensitive-data-handling.md)**Note:** This feature is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Send email summaries of unread messages to users when they are inactive

</td><td>

[Sending missed chat activity emails](../task/ac-missed-activity-emails.md)

</td></tr></tbody>
</table>-   **[Manage LLM virtual agents on the Assistants screen](../../virtual-agent/task/manage-llm-va.md)**  
Create, edit, and turn on/off LLM virtual agents from the Assistants screen.
-   **[Add your bot to a portal](../task/ac-configure-bot-portal.md)**  
Give your users a place to interact with your bot and human agents. Choose a Service Portal chat configuration provided with your base system, such as the Service Portal Agent Chat configuration used for Agent Chat and Virtual Agent. Your end users can initiate and maintain a bot or Agent Chat conversation in any page of the portal.
-   **[Branding your chat client](branding-chat-client.md)**  
Customize your chat interface with your own brand, including company logo and bot avatar, UI color schemes, fonts, and the chat support menu displayed to your users.
-   **[Enable message preview on the chat widget](../task/web-client-message-preview.md)**  
Admins can allow their end users to see a preview of any new or unread messages waiting for them when the chat window is minimized.
-   **[Enable public access to the chat widget](../task/enable-public-access-web-client.md)**  
Enable public access to the Virtual Agent chat widget for portals.
-   **[Configure context variables for storing chat-related information](../task/ac-configure-context-variables.md)**  
Specify chat context variables, also called Live Agent chat variables, for storing chat-related information, such as pre-chat survey responses. These variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. You can also define variables to capture contextual information passed in Virtual Agent topic scripts to share with live agents.
-   **[Change Virtual Agent and Agent Chat system messages](../task/ac-change-system-messages.md)**  
Customize the default system messages displayed during Virtual Agent conversations and Agent Chat.
-   **[URL navigation in Conversational Interfaces](url-navigation-ci.md)**  
Use URL navigation settings to specify where and how chat links open. You can configure certain links to open in a specific portal. You can also specify the link target, such as a popup window.
-   **[Create chat surveys](../task/create-chat-surveys.md)**  
Use Survey Designer to build conversational questionnaires for gathering pre-chat information and post-chat feedback from end users. These questionnaires run in the chat client for Virtual Agent and Agent Chat.
-   **[Define pre-chat survey configurations](../task/ac-configure-pre-chat-surveys.md)**  
Use pre-chat surveys to capture preliminary information from a customer. You can define a configuration that determines the pre-chat survey to be presented to your customers. From the responses received, Advanced Work Assignment routes chat conversations to appropriate queues and groups.
-   **[Define post-chat survey configurations](../task/define-post-chat-survey-config.md)**  
Control the post-chat questionnaire displayed to your requesters to gather feedback on their experience with live agents. You configure the post-chat surveys to be used for chat queues defined in Advanced Work Assignment.
-   **[Using pre-chat surveys with context variables for topic discovery](using-context-intent-prechat-survey.md)**  
Capture user input from pre-chat surveys to use as utterances or keywords for topic discovery.

