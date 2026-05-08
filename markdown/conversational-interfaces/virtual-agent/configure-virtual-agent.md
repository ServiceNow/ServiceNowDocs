---
title: Configuring Virtual Agent
description: Configure the Virtual Agent features, components, and integrations that you need to provide support to your employees, IT teams, and customers.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Configuring, Virtual Agent, Conversational Interfaces Console, Agent Chat]
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Configuring Virtual Agent

Configure the Virtual Agent features, components, and integrations that you need to provide support to your employees, IT teams, and customers.

Use the Conversational Interfaces Console to activate and configure Virtual Agent. Some of the general settings in the console are shared with other applications, such as Agent Chat.

<table id="table_kbf_kxv_fsb"><thead><tr><th>

I want to...

</th><th>

See these topics

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Chat Client Display Options

</td></tr><tr><td>

Brand my bot

</td><td>

[Branding your chat client](../../conversational-interfaces/concept/branding-chat-client.md)

</td></tr><tr><td>

Preview new or unread messages in a minimized chat window

</td><td>

[Enable message preview on the chat widget](../../conversational-interfaces/task/web-client-message-preview.md)

</td></tr><tr><td class="sub-head" colspan="2">

Conversation Routing

</td></tr><tr><td>

Configure my bot to run in third-party messaging apps

</td><td>

[Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md).

</td></tr><tr><td>

Create pre-chat surveys

</td><td>

[Define pre-chat survey configurations](../../conversational-interfaces/task/ac-configure-pre-chat-surveys.md)

</td></tr><tr><td>

Create and use context variables to store chat-related information

</td><td>

[Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md)

</td></tr><tr><td>

Display or announce callback options to users through other ServiceNow apps

</td><td>

[Omnichannel Callback](../../omnichannel-callback/concept/omnichannel-callback.md)

</td></tr><tr><td>

Configure topic context intents

</td><td>

[Define topic context intent configurations](../../conversational-interfaces/task/ac-configure-context-topic-intent.md)

</td></tr><tr><td class="sub-head" colspan="2">

System Actions

</td></tr><tr><td>

Modify system chat messages

</td><td>

[Change Virtual Agent and Agent Chat system messages](../../conversational-interfaces/task/ac-change-system-messages.md)

</td></tr><tr><td>

Specify how links open from the chat window

</td><td>

[URL navigation in Conversational Interfaces](../../conversational-interfaces/concept/url-navigation-ci.md)

</td></tr><tr><td>

Configure my bot to detect sensitive data

</td><td>

[Configuring Sensitive Data Handler](../../conversational-interfaces/task/ac-configure-sensitive-data-handling.md)**Note:** This feature is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see Data Privacy.

</td></tr><tr><td>

Send email summaries of unread messages to users when they are inactive

</td><td>

[Sending missed chat activity emails](../../conversational-interfaces/task/ac-missed-activity-emails.md)

</td></tr></tbody>
</table><table id="table_grb_xf4_swb"><thead><tr><th>

I want to...

</th><th>

See these topics

</th></tr></thead><tbody><tr><td>

Get recommendations for Virtual Agent topics based on my data

</td><td>

[Quick start for Topic Recommendations](getting-started-topic-recommendations.md)

</td></tr><tr><td>

Configure performance tracking for Virtual Agent topics

</td><td>

[Create deflection configurations and patterns](../task/set-up-deflection-settings-va.md)

</td></tr><tr><td>

Use Natural Language Understanding \(NLU\) for topic discovery

</td><td>

[Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md)

 Creating models \(using NLU Workbench\)

</td></tr><tr><td>

Create custom greetings and setup topics

</td><td>

[Configure a Virtual Agent chat experience](../task/configure-default-chat-experience.md)

</td></tr><tr><td>

Determine which issues are routed to Virtual Agent first

</td><td>

[Configure and run an Issue Auto Resolution simulation](../task/configure-ar-simulations.md)

</td></tr><tr><td>

Send notifications to users in Virtual Agent

</td><td>

[Configuring Virtual Agent notifications](configuring-va-notifications.md)

 [Enable Virtual Agent notifications](../task/enable-va-notifications.md)

</td></tr><tr><td>

Use AI Search to return fallback results for Virtual Agent

</td><td>

[Improving the user experience with AI Search](va-ai-search.md)

</td></tr><tr><td>

Detect and dynamically translate Virtual Agent topics into a different language

</td><td>

[Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](dynamic-lang-detection-translation-enhanced-chat.md)

</td></tr></tbody>
</table>## Virtual Agent security

Platform hardening for your instance is leveraged by Virtual Agent, so you should follow the overall platform hardening recommendations. For details, see Secure your instance.

-   **[Customizing a Virtual Agent chat experience](va-conversation-settings.md)**  
Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.
-   **[Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md)**  
Configure Natural Language Understanding \(NLU\) in Virtual Agent to identify the NLU service provider for your instance. You can also specify the languages of NLU models used during conversation design, based on the languages supported by your NLU provider and the ServiceNow AI Platform®.
-   **[Use the portable chat widget to add Virtual Agent to your web page](use-portable-va-web-client.md)**  
The portable chat widget can run on third-party web pages, in the service portal, or in UI Builder portals.
-   **[Configure Virtual Agent for a ServiceNow mobile application](../task/configure-va-mobile-web-client.md)**  
Virtual Agent provides optimized templates for the mobile experience. Configure a service portal to run Virtual Agent on a ServiceNow mobile application.
-   **[Using multiple active conversations in Virtual Agent](c_multiple-active-conversations-va.md)**  
Virtual Agent features the ability to have multiple conversations at the same time, separated and directed by chosen context.
-   **[Using catalogs and autopilot in Virtual Agent](va-catalogs.md)**  
Use catalogs to search for and request services and products in chat widget conversations.
-   **[Configuring Virtual Agent notifications](configuring-va-notifications.md)**  
Send ServiceNow notifications directly to users via the Virtual Agent chatbot on supported messaging channels. Notifications can be simple informational messages for review, or actionable messages with buttons that users can select to perform certain actions.
-   **[Configure cross-scope access privileges for topic blocks and custom controls](../task/configure-cross-scope-privileges.md)**  
Enable topic authors and developers to access Virtual Agent topic blocks and custom controls from other scoped applications.
-   **[Create or modify custom Virtual Agent categories](../task/create-topic-category.md)**  
Create or change custom categories for organizing and grouping related Virtual Agent assets, such as topics. You can also make category labels visible in the Topic picker menu displayed to end users.

**Parent Topic:**[Virtual Agent](virtual-agent-landing-page.md)

