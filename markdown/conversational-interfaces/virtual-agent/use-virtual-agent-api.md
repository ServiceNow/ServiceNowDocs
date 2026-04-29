---
title: Using Virtual Agent API
description: Virtual Agent API enables ServiceNow developers, advanced users, and admins to use Virtual Agent with an enterprise or any other third-party chat interface that supports conversational interfaces or as a secondary bot in an environment with multiple, specialized bots managed by a primary bot.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [use]
breadcrumb: [Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using Virtual Agent API

Virtual Agent API enables ServiceNow developers, advanced users, and admins to use Virtual Agent with an enterprise or any other third-party chat interface that supports conversational interfaces or as a secondary bot in an environment with multiple, specialized bots managed by a primary bot.

The following sections detail how to use Virtual Agent API to complete various tasks, such as closing an idle bot, enabling Now Assist experience, and various controls for the bot output response.

-   **[Enable synthesized response in Virtual Agent API](../task/va-api-enable-synthesized-response.md)**  
You can now enable synthesized response in the conversations with the primary bot.
-   **[Configure interaction record to store clientSessionId in Virtual Agent API](../task/va-api-interaction-record-third-party-chat.md)**  
You can configure to store **clientSessionId** to support third-party chat applications.
-   **[Configure to support chat history in Virtual Agent API](../task/va-api-support-chat-history.md)**  
You can now support your live agents to see chat history in their conversations with the primary bot.
-   **[Enable Now Assist experience in Virtual Agent API](../task/enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.md)**  
Enable Now Assist experience in Virtual Agent API to support generative AI skills across multiple provider channels.
-   **[../task/va-api-enable-premium-chat.md](../task/va-api-enable-premium-chat.md)**  

-   **[Configure multiple provider applications](../task/configure-multiple-provider-applications.md)**  
You can configure multiple provider applications to support AI agents where there are multiple primary bots using Virtual Agent API and you need to distinguish between them.
-   **[Transform Virtual Agent API request and response](../task/transform-virtual-agent-api-request-and-response.md)**  
You can transform Virtual Agent API request and response into supported formats through the scripted extension points provided in Virtual Agent API.
-   **[Enable synchronous support in Virtual Agent API](../task/virtual-agent-api-enable-synchronous-support.md)**  
You can support synchronous mode for your conversation with primary bot.
-   **[Virtual Agent bot-to-bot integration](bot2bot.md)**  
The Virtual Agent API supports environments that use multiple bots. In this situation, a primary bot communicates with third-party secondary bots, such as a ServiceNow bot.
-   **[Closing idle bot-to-bot conversations](va-b2b-open-conversation.md)**  
In bot-to-bot integrations \(Virtual Agent API\), abandoned conversations that are "idle" for more than an hour are automatically closed by the scheduled job, **Time Out Abandoned B2B Conversations**. This job runs hourly each day.
-   **[Controls in Virtual Agent API](va-api-controls.md)**  
Virtual Agent API provides you various controls to manage the responses in your conversation.

**Parent Topic:**[Virtual Agent API](virtual-agent-api-landing-page.md)

