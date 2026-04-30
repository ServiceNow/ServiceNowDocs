---
title: Natural Language Understanding \(NLU\) topic discovery in Virtual Agent
description: Apply Natural Language Understanding \(NLU\) models that enable Virtual Agent to process user statements in automated conversations. An NLU model provides information that your virtual agent uses to determine what users want to do and to extract relevant values from their input. With NLU, Virtual Agent can offer a more natural and engaging conversational experience.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Explore, Virtual Agent, Conversational Interfaces]
---

# Natural Language Understanding \(NLU\) topic discovery in Virtual Agent

Apply Natural Language Understanding \(NLU\) models that enable Virtual Agent to process user statements in automated conversations. An NLU model provides information that your virtual agent uses to determine what users want to do and to extract relevant values from their input. With NLU, Virtual Agent can offer a more natural and engaging conversational experience.

## NLU components

ServiceNow NLU can learn the syntax, semantics, and vocabulary of your company using the data in your ServiceNow instance. Use NLU Workbench, the NLU model builder, and the NLU inference service to enable the system to learn and respond to user intent.

The following elements work together to identify what the user wants to do so that a solution can be found:

-   **Model groups**

    A model group supports a given application, user roles, and languages. For example, you may have a model that supports the Search feature and another model that supports . Typically, a model group contains multiple intents. For more information, see [Model management](https://www.servicenow.com/docs/access?context=model-management-phases&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **Intents**

    Intents represent actions. They describe what the user wants to do or what your application can handle. Intents can pertain to any of the following:

    -   Functions, such as resetting a password or ordering an item.
    -   Domains, such as healthcare, financial, or government.
    -   Customers, such as the US Army, Wells Fargo, or Boeing.
    In Virtual Agent, a single intent is mapped to one conversation topic.

    For more information, see [NLU intents](https://www.servicenow.com/docs/access?context=intents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **Utterances**

    Instead of keywords, you enter natural language examples, called utterances. Utterances help NLU to evaluate word meanings and contexts so it can infer user or system actions. Example utterances might include the following:

    -   Reset my password.
    -   Change password.
    -   I don't remember my password.
    -   Forgot my password.
    -   My password needs to be reset.
-   **Entities**

    Entities represent the object of \(or context for\) the action. You can define them for individual intents. NLU can match defined entities with user input to slot-fill the values. Slot-filling can eliminate the need to ask some questions within a topic flow. There are three basic types of entities that you can define:

    -   Common or system entities, such as date, time, currency, location, quantity, people, or organization.
    -   Entities based on ServiceNow records, such as a case number.
    -   Company- or domain-specific entities, such as meeting rooms, company policies, and so forth.
    For more information, see [NLU entities](https://www.servicenow.com/docs/access?context=entities&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).


## How NLU models work in Virtual Agent

When you create or update topics in Virtual Agent Designer, you specify the NLU model and intent that Virtual Agent uses to find the appropriate conversation topic for fulfilling the intent.

Virtual Agent supports models from different services. You can use the following providers:

-   ServiceNow NLU models that you create using NLU Workbench.

    ServiceNow provides pre-built \(read-only\) NLU models and topics for various ServiceNow business applications, such as Customer Service Management, HR Service Delivery, and ITSM. You can use the intents defined in these pre-built models and reuse them when you create your own models.

-   If you're using IBM Watson Assistant as your NLU service provider, NLU intents and entities are created in IBM Watson Assistant.
-   If you're using Google Dialogflow ES as your NLU service provider, NLU intents and entities are defined in the Google Cloud platform.

**Note:** Virtual Agent supports only one NLU service provider per instance.

With NLU models, your virtual agent can do the following:

-   Perform topic discovery.
-   Designate backup keywords in case an intent is not matched.
-   Extract entity values.
-   Handle conversation switching in a conversation session.

These capabilities are explained in the following sections.

## Topic discovery

When users provide an utterance, the utterance is a statement that is associated with a specific intent. Virtual Agent processes these utterances to launch the appropriate conversation topic. Each topic has a single intent that you specify in Virtual Agent Designer.

During the topic discovery process, intents are matched to topics. Virtual Agent returns the most relevant topics for a user's request. The topic discovery process returns the following results to a user:

-   Single match: When a user utterance directly matches an intent \(topic\), the topic runs automatically.
-   Multiple matches: When a user utterance matches more than one intent, Virtual Agent returns a choice list of the relevant matches so that the user can choose the appropriate topic.

    **Note:** If there are multiple matches, Virtual Agent returns three intents by default. You can change the number of topics returned by using the **com.glide.cs.max\_number\_display\_topics** system property.

-   No matches: When Virtual Agent can't find a matching intent, it uses AI Search to generate search results that display relevant links to Q&amp;A knowledge articles, Service Catalog items, or person \(user\) records.

    This feature is controlled by the AI Search Fallback setup topic and the Virtual Agent search configurations, which are enabled by default in [chat experiences](va-conversation-settings.md). To learn more about the AI Search results generated, see [Virtual Agent integration with AI Search](va-ai-search.md).

    If you disable the AI Search Fallback setup topic, Virtual Agent automatically displays a fallback error message that enables the user to select a topic or enter a different request.

    ![Virtual Agent responds with, "I am sorry, but I didn't understand your request." The user can type a new utterance or select Show Me Everything.](../images/setup-va-fallback-no-ustand.png "Example fallback message")

    For details about how the AI Search Fallback setup topic and the fallback response \(the fallback setup topic\) work, see [Customizing a Virtual Agent chat experience](va-conversation-settings.md).


For detailed information about NLU topic discovery, see [Natural Language Understanding topic discovery logic in Virtual Agent](how-topic-discovery-works.md).

## Topic discovery with backup keywords

When you create or update topics, you can also optionally specify keywords that Virtual Agent uses to determine the topic if NLU doesn't return a matching intent and topic. Virtual Agent uses keywords in the following situations:

-   No topics \(intents\) are discovered.
-   The appropriate topic \(intent\) can't be determined because too many topics \(intents\) are discovered.
-   The language of the topic and intent is not currently supported in NLU.

**Note:** If Virtual Agent can't determine the topic based on NLU or the keyword, it falls back on the AI Search capability to deliver relevant results. The AI Search capability must be enabled.

## Entity extraction

With NLU models, Virtual Agent can determine when user statements in a conversation contain important information to fulfill a task or goal. Entities identify the information that Virtual Agent can extract from the conversation, such as an object or a person's name. To extract the appropriate values, Virtual Agent uses the entity information that is associated with an intent that is defined in the NLU model.

When designing your topic, you can use entities as follows:

-   [Associate an entity with a user input node](../reference/va-user-inputs.md) on the **Flow** tab. You can specify whether Virtual Agent asks the user to confirm the slot-filled entity value or to skip the node.
-   [Add nodeless NLU entities as input variables to a topic](../task/add-nodeless-entities-input-vars.md). These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.

## Conversation switching

Users engaged in a Virtual Agent conversation can switch topics anytime during the conversation. For example, a user might be updating an item in the user's employee profile. But before completing the update, that user might ask to order an item instead. Virtual Agent can find and run the appropriate topic based on the user's request. You can enable users who switched topics to resume the original conversation.

Another example is when a user might ask a casual question or engage in small talk. The question might be unrelated to the original request. By reviewing the intents defined in the NLU model, Virtual Agent can match and launch the appropriate conversation for the switched topic.

## ServiceNow NLU multi-language support and integration with Virtual Agent Designer

If you're using ServiceNow NLU, you can map an NLU model group and an associated intent to a topic. You can also update, train, and test the associated NLU model from within Virtual Agent Designer. As you work on a topic, you can also improve or modify the utterances and the associated entities for an intent without leaving the interface.

ServiceNow NLU model groups contain a primary language and secondary languages. Use the primary language to author your topic, which can then be translated into the secondary languages within the group. For more information, see [Multilingual model management](https://www.servicenow.com/docs/access?context=multilingual-model-managent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

As you work on your topics, Virtual Agent Designer provides language-mapping views for previewing and testing topics with their associated language-specific models. For more information, see [Localizing Virtual Agent conversations](localize-va-topic.md).

