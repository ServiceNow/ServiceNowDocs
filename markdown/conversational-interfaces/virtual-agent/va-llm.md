---
title: LLM topic discovery in Virtual Agent
description: Large language models \(LLMs\) enable Virtual Agent to process user statements in plain language. Conversations that use LLMs can outperform those conversations that use Natural Language Understanding \(NLU\), with easier setup.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Virtual Agent, Conversational Interfaces]
---

# LLM topic discovery in Virtual Agent

Large language models \(LLMs\) enable Virtual Agent to process user statements in plain language. Conversations that use LLMs can outperform those conversations that use Natural Language Understanding \(NLU\), with easier setup.

## How LLMs work in Virtual Agent

Watch this video to learn about LLM topics in Virtual Agent Designer.

Virtual Agent Designer LLM topic authoring video 

When you create a topic in Virtual Agent Designer, you can select LLM as the model type for your topic whenever Now Assist in Virtual Agent is turned on. Virtual Agent then uses LLM generative AI to discover topics that match the user's intent.

Unlike NLU topics, LLMs don't require models, intents, or keywords to be linked to the topic. LLMs can discover topics and perform language-related tasks, such as text generation for case summaries and resolution notes, without months of training on NLU models. Overall, you can create, configure, and deploy LLM topics faster than working with NLU.

With LLMs, Virtual Agent can do the following:

-   Perform topic discovery without needing a singular declared intent in a given topic.
-   Find intents without backup keywords as in NLU modeling.
-   Extract entity values without prior mapping as in NLU modeling.
-   Handle multiple conversation topic switches in a single conversation session.

For more information about LLMs, see Large language models on the ServiceNow AI Platform®.

## Topic discovery

With LLM topic discovery, topic authors no longer need to create and maintain complex NLU models and intents with backup keywords. The LLM does all of the heavy lifting for you. The only requirement is a robust, plain language topic description on the **Properties** tab in Virtual Agent Designer. The LLM uses this description to find the best topic match for the user utterance. If there are multiple potential matches, the user will see a list of topics to choose from.

For example, if a user asks Virtual Agent to calculate a ride share fee, the LLM matches the user utterance with an existing topic that can calculate the ride share with a tip.

## Entity extraction

With LLM topics, the LLM has all the information needed to determine if an utterance has the information to fulfill a request. Unlike NLU models, you don't need to associate entities with a user input node or add nodeless NLU entities as input variables to a topic. The LLM simply finds the entity that most closely fits the user intent.

## Topic switching

Topic switching is faster and easier with LLMs compared to NLU topics. The LLM processes your requests to change intent made in natural language, and activates the appropriate topic.

For example, if you start a conversation by asking for a mobile phone, you don't have to cancel the order first or restart the conversation. Instead, you can ask Virtual Agent to order a laptop instead. Virtual Agent immediately switches from the mobile phone topic to the laptop topic. Topic switching can be done during a query, but not within a catalog ordering flow.

Another example is when a user might ask a casual question or engage in small talk. The question might be unrelated to the original request. You can create small talk topics or set up small talk filters to help the Virtual Agent match and launch the appropriate conversation for the switched topic. For more information, see [Create a small talk topic](../task/create-small-talk.md) and Configure small talk filters.

## Additional resources

-   [Now Assist in Virtual Agent](../../now-assist-in-va/concept/now-assist-in-va-landing.md)
-   [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md)

