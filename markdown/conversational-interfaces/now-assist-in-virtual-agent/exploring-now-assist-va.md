---
title: Exploring ServiceNow Otto for Virtual Agent
description: ServiceNow Otto for Virtual Agent uses large language models \(LLMs\) and generative AI skills to improve deflection rates and reduce the amount of time-consuming work that Natural Language Understanding \(NLU\) topic discovery requires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/exploring-now-assist-va.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Exploring, Now Assist, Virtual Agent, LLM, NLU, Natural Language Understanding, Large language model, skills]
breadcrumb: [ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Exploring ServiceNow Otto for Virtual Agent

ServiceNow Otto for Virtual Agent uses large language models \(LLMs\) and generative AI skills to improve deflection rates and reduce the amount of time-consuming work that Natural Language Understanding \(NLU\) topic discovery requires.

ServiceNow Otto capabilities bring generative AI to Virtual Agent. Using LLMs for topic discovery simplifies the amount of setup and configuration required for Virtual Agent. Topics that use keyword and Natural Language Understanding \(NLU\) discovery often require months of development and the involvement of dedicated subject matter experts. Unusual issues or questions may lead a user to contact a live agent instead. You can continue to use your existing NLU topics and migrate them into new LLM topics using the topic migration feature within Assistant Designer Asset library. For more information on topic migration, see [Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/llm-topic-migration.md).

Use the guided setup to configure ServiceNow Otto for Virtual Agent in a few minutes. No expertise is necessary to launch the experience. For more information, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

ServiceNow Otto for Virtual Agent is available through portals on the chat widget, the mobile app, and Microsoft Teams.

## Search in ServiceNow Otto for Virtual Agent

ServiceNow Otto for Virtual Agent enhance the user experience by combining AI Search with chat. These skills can increase issue resolution in Virtual Agent and reduce deflections to a live agent.

The following figure shows how the requester uses natural language rather than keywords in the chat. Now LLM Service determines the most likely option based on the requester's input and sends a synthesized response with possible action items. Queries can apply to both information searches and service catalog requests.

\[Omitted image "carousel-nds-cards-na-va.png"\] Alt text: A summary of the iPad options along with catalog options to either Go to request or Start request in the Virtual Agent.

ServiceNow Otto for Virtual Agent shows users the best possible answer to a query, in the form of actionable options displayed along with the results. The bot may generate answers based on what it found, or return actionable options or links. Users have the option to see more results as needed.

## Service Catalog access

ServiceNow Otto for Virtual Agent also gives users access to available options in the Service Catalog. Users can request an item, such as a mobile phone. The user can then provide more information to refine the search. For example, they may refine their request to a blue 256-GB iPhone. They can even request a new item instead, all in the same conversation, and the generative AI creates its responses using natural language.

For full catalog functionality in the chat window, enable the generative AI experience for catalog item request submissions. For more information, see [Configure ServiceNow Otto in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-gen-ai-catalog-item.md).

## LLM topic creation

Admins can create LLM topics for ServiceNow Otto for Virtual Agent. For more information, see [LLM assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/llm-assistants.md). Activate the ServiceNow Otto Topics skill in the ServiceNow Otto guided setup. For more information, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

For more examples of having a conversation with ServiceNow Otto for Virtual Agent, see [Using ServiceNow Otto for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.md).

The skill picker is configurable based on the user's requirements. For example, a user can change the **View all topics** label in the skill picker and add or remove the bullet list of promoted assets from the skill selection message.

## Benefits

ServiceNow Otto for Virtual Agent provides the following benefits.

|Benefit|Feature|User|
|-------|-------|----|
|Configure ServiceNow Otto for Virtual Agent in a few minutes, from either the Conversational Interfaces console or the AI Admin Hub console.|[Guided setup experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md)|virtual\_agent\_admin or admin|
|ServiceNow Otto skills can be turned on within the guided setup.|[Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-a-now-assist-skill.md)|virtual\_agent\_admin or admin|
|Deploy ServiceNow Otto for Virtual Agent on multiple portals using the chat widget, the mobile app, and Microsoft Teams.|[Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md)|virtual\_agent\_admin or admin|
|Generative AI enhances the user search experience with the ability to generate answers and enabling the user to select the **Show more results** option for a new search.|[ServiceNow Otto Q&amp;A Genius Results skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.md)|requesters|
|Give users in-chat access to available options in the Service Catalog.|[ServiceNow Otto Multi-Turn Catalog Ordering skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.md)|requesters|
|ServiceNow Otto for Virtual Agent switch easily between requests, using plain language when new queries are made in the same conversation.|[Mid-topic switching during ServiceNow Otto for Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/intent-switching-na-va.md)|requesters|
|Monitor performance metrics for ServiceNow Otto for Virtual Agent from the Conversational Interfaces console.|[Conversational Interfaces console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/exploring-ci.md)|virtual\_agent\_admin or admin|
|Monitor value metrics \(ServiceNow Otto usage versus ServiceNow Otto for Virtual Agent\) from the ServiceNow Otto admin console.|[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)|virtual\_agent\_admin or admin|

