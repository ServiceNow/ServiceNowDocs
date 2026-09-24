---
title: Exploring Virtual Agent
description: The ServiceNow Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. Design and build automated conversations that use large language models \(LLMs\) and AI to improve deflection rates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/exploring-virtual-agent.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [Virtual Agent, Exploring, Now Assist, LLM, NLU, Natural Language Understanding, Large language model]
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Exploring Virtual Agent

The ServiceNow Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. Design and build automated conversations that use large language models \(LLMs\) and AI to improve deflection rates.

## Overview of Virtual Agent

Virtual Agent helps solve ordinary issues and delivers results for common requests, leaving your agents and technicians free to focus on more complex user issues. You can change the look and feel of the chat experience to suit each audience for your business, including running your chatbot in a variety of common or custom messaging channels. Use the Assistant Designer Analytics tab to monitor your bot's success.

Your developers have access to large language model \(LLM\) topic discovery. Assistant Designer includes LLM controls that make topic authoring easier so that you can deliver self-service solutions more quickly.

\[Omitted image "mmasset0022339.svg"\] Alt text: Virtual Agent increases deflection and improves self-service in a customizable environment. With ServiceNow Otto for Virtual Agent, development time is faster and uses generative AI LLM topic discovery.

## Virtual Agent and ServiceNow Otto for Virtual Agent

Virtual Agent refers to the Glide Virtual Agent plugin \[com.glide.cs.chatbot\]. ServiceNow Otto for Virtual Agent refers to the \[sn\_nowassist\_va\] plugin. Some of the original NLU and keyword functionality that comes with the Glide Virtual Agent plugin is planned for deprecation, and therefore the remaining topic discovery option is LLM discovery. For more information about NLU deprecation, see [\(Legacy\) Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent-landing-page-nlu.md).

## Search in ServiceNow Otto for Virtual Agent

ServiceNow Otto for Virtual Agent enhance the user experience by combining AI Search with chat. These skills can increase issue resolution in Virtual Agent and reduce deflections to a live agent.

The following figure shows how the requester uses natural language rather than keywords in the chat. The LLM determines the most likely option based on the requester's input and sends a synthesized response with possible action items. Queries can apply to both information searches and service catalog requests.

\[Omitted image "carousel-nds-cards-na-va.png"\] Alt text: A summary of the iPad options along with catalog options to either Go to request or Start request in the Virtual Agent.

ServiceNow Otto for Virtual Agent shows users the best possible answer to a query, in the form of actionable options displayed along with the results. The bot may generate answers based on what it found, or return actionable options or links. Users have the option to see more results as needed.

## Service Catalog access

ServiceNow Otto for Virtual Agent also gives users access to available options in the Service Catalog. Users can request an item, such as a mobile phone. The user can then provide more information to refine the search. For example, they may refine their request to a blue 256-GB iPhone. They can even request a new item instead, all in the same conversation, and the generative AI creates its responses using natural language.

For full catalog functionality in the chat window, enable the generative AI experience for catalog item request submissions. For more information, see [Configure ServiceNow Otto in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-gen-ai-catalog-item.md).

## AI agents in Virtual Agent

Virtual Agent supports AI agents. When a user asks a question in chat, an AI agent understands the query and can reason, plan, and execute using tools such as the following:

-   AI agents
-   Virtual Agent topics
-   Conversational actions and subflows
-   Catalogs
-   Knowledge articles
-   Generative AI skills

Virtual Agent supports multi-intent queries with AI agents if there are associated AI agents per user query.

## Virtual Agent availability

The Virtual Agent platform is available as a professional subscription that is automatically included with the ServiceNow AI Platform®.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

Assistant Designer provides all the core functionality for creating and deploying Virtual Agent conversations. Virtual Agent includes the following features, which are automatically installed with the Glide Virtual Agent plugin \(com.glide.cs.chatbot\):

-   Virtual Agent chat widget
-   Virtual Agent notifications
-   Conversational custom chat integration framework
-   Conversational Interfaces console for admin configuration

## Virtual Agent benefits

|Benefit|Feature|User|
|-------|-------|----|
|Configure ServiceNow Otto for Virtual Agent in a few minutes, from either the Conversational Interfaces console or the AI Admin Hub console.|[Guided setup experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-now-assist-va.md)|virtual\_agent\_admin or admin|
|Use a conversation designer to build and test conversations without scripting or advanced skills. Drag and drop elements on the graphical canvas to see the entire flow. Go further with branching, looping, and scripting.|[Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)|virtual\_agent\_admin or admin|
|Deploy ServiceNow Otto for Virtual Agent on multiple portals using the chat widget, the mobile app, and Microsoft Teams.|[Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-now-assist-va.md)|virtual\_agent\_admin or admin|
|Give users in-chat access to available options in the Service Catalog.|[ServiceNow Otto Multi-Turn Catalog Ordering skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/using-now-assist-in-va.md)|requesters|
|Seamlessly transfer the entire conversation history and context to the right human agent so they can quickly address any escalations and resolve user issues.|[Escalate to human assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/using-va-agent-chat.md)|virtual\_agent\_admin or admin|
|ServiceNow Otto for Virtual Agent switch easily between requests, using plain language when new queries are made in the same conversation.|[Mid-topic switching during ServiceNow Otto for Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/intent-switching-na-va.md)|requesters|
|Analyze the performance of assistants in Assistant Designer.|[Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/ai-engagement-analytics.md)|virtual\_agent\_admin or admin|
|Connect to where your employees and customers already are—in web portals, Now® Mobile apps, and collaboration tools like Slack and Microsoft Teams, and any other popular chat or messaging app.|[Conversational Integration apps for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/integrate-virtual-agent.md)|virtual\_agent\_admin or admin|
|Serve your international Virtual Agent users, regardless of their language and locale.|[Dynamic Translation in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/dynamic-translation-va.md)|virtual\_agent\_admin or admin|

**Note:** For developer training, go to the [Developer's Portal](https://developer.servicenow.com/dev.do) \(login required\). Navigate to **Learn** &gt; **Courses** &gt; **Virtual Agent**.

