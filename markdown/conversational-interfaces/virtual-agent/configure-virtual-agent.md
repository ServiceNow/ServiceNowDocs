---
title: Configuring Virtual Agent
description: Configure the Virtual Agent features, components, and integrations that you need to provide support to your employees, IT teams, and customers.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [Configuring, Virtual Agent, Conversational Interfaces Console, Agent Chat]
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Configuring Virtual Agent

Configure the Virtual Agent features, components, and integrations that you need to provide support to your employees, IT teams, and customers.

Use the Conversational Interfaces Console to activate and configure Virtual Agent. Some of the general settings in the console are shared with other applications, such as Agent Chat.

|I want to...|See these topics|
|------------|----------------|
|Chat Client Display Options|
|Brand my bot|[Branding your chat client](../../conversational-interfaces/concept/branding-chat-client.md)|
|Preview new or unread messages in a minimized chat window|[Enable message preview on the chat widget](../../conversational-interfaces/task/web-client-message-preview.md)|
|Conversation Routing|
|Configure my bot to run in third-party messaging apps|[Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md).|
|Create pre-chat surveys|[Define pre-chat survey configurations](../../conversational-interfaces/task/ac-configure-pre-chat-surveys.md)|
|Create and use context variables to store chat-related information|[Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md)|
|Display or announce callback options to users through other ServiceNow apps|[Omnichannel Callback](https://www.servicenow.com/docs/access?context=omnichannel-callback&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|
|Configure topic context intents|[Define topic context intent configurations](../../conversational-interfaces/task/ac-configure-context-topic-intent.md)|
|System Actions|
|Modify system chat messages|[Change Virtual Agent and Agent Chat system messages](../../conversational-interfaces/task/ac-change-system-messages.md)|
|Specify how links open from the chat window|[URL navigation in Conversational Interfaces](../../conversational-interfaces/concept/url-navigation-ci.md)|
|Configure my bot to detect sensitive data|[Configuring Sensitive Data Handler](../../conversational-interfaces/task/ac-configure-sensitive-data-handling.md)|
|Send email summaries of unread messages to users when they are inactive|[Sending missed chat activity emails](../../conversational-interfaces/task/ac-missed-activity-emails.md)|

<table id="table_grb_xf4_swb"><thead><tr><th>

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

 [Creating models](https://www.servicenow.com/docs/access?context=creating-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) \(using NLU Workbench\)

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



</td></tr></tbody>
</table>## Virtual Agent security

Platform hardening for your instance is leveraged by Virtual Agent, so you should follow the overall platform hardening recommendations. For details, see [Secure your instance](https://www.servicenow.com/docs/access?context=platsec-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **[Activate Virtual Agent](../task/activate-virtual-agent.md)**  
 You can activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) if you have the admin role. This plugin automatically activates other necessary plugins if they are not already active.
-   **[Setting up chat experiences for Virtual Agent users](va-conversation-settings.md)**  
Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.
-   **[Configuring the portable Virtual Agent chat widget](use-portable-va-web-client.md)**  
The Portable chat widget can run on third-party web pages, in the service portal, or in UI Builder portals.
-   **[Configure Virtual Agent for a ServiceNow mobile application](../task/configure-va-mobile-web-client.md)**  
Virtual Agent provides optimized templates for the mobile experience. Configure a service portal to run Virtual Agent on a ServiceNow mobile application.
-   **[Multiple active conversations for Virtual Agent](c_multiple-active-conversations-va.md)**  
As of the Yokohama release, Virtual Agent \(VA\) features the ability to have multiple conversations at the same time, separated and directed by chosen context.
-   **[Catalogs and Autopilot for Virtual Agent](va-catalogs.md)**  
Use Catalogs to search for and request services and products in chat widget conversations.
-   **[Configuring Virtual Agent notifications](configuring-va-notifications.md)**  
Send ServiceNow notifications directly to users via the Virtual Agent chatbot on supported messaging channels. Notifications can be simple informational messages for review, or actionable messages with buttons that users can select to perform certain actions.
-   **[Create cross-scope access privileges for topic blocks and custom controls](../task/configure-cross-scope-privileges.md)**  
Enable topic authors and developers to access Virtual Agent topic blocks and custom controls from other scoped applications.
-   **[Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md)**  
Configure Natural Language Understanding \(NLU\) in Virtual Agent to identify the NLU service provider for your instance. You can also specify the languages of NLU models used during conversation design, based on the languages supported by your NLU provider and the ServiceNow AI Platform®.
-   **[Create or modify custom categories](../task/create-topic-category.md)**  
Create or change custom categories for organizing and grouping related Virtual Agent assets, such as topics. You can also make category labels visible in the Topic picker menu displayed to end users.

**Parent Topic:**[Virtual Agent](virtual-agent-landing-page.md)

