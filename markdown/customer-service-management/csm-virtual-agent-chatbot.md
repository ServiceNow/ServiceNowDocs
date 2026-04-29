---
title: Customer Service Virtual Agent conversations
description: Predefined Customer Service Virtual Agent chatbot conversations enable your customers to get help with the product. Integrating Natural Language Understanding \(NLU\) models with your virtual agent chatbot topics enables chatbots to analyze, understand, and navigate the user to the right topic based on the inferred intent.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Virtual Agent, Chat channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# Customer Service Virtual Agent conversations

Predefined Customer Service Virtual Agent chatbot conversations enable your customers to get help with the product. Integrating Natural Language Understanding \(NLU\) models with your virtual agent chatbot topics enables chatbots to analyze, understand, and navigate the user to the right topic based on the inferred intent.

A conversation topic defines the dialog between the Virtual Agent \(chatbot\) and the user to accomplish a specific goal.

## Activating Virtual Agent conversations

The system administrator or a virtual agent admin must do the following to enable the chatbot conversations:

-   Enable the Glide Virtual Agent plugin \(com.glide.cs.chatbot\).
-   Enable the Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\).
-   [Publish](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) the following read-only pre-defined virtual agent chatbot topics and topic blocks:

    **Note:** You can duplicate a topic and then customize it.

    -   Check Case Status \(Template\)

        Users can search cases and check the status of an existing case.

    -   Get Help with a Product \(Template\)

        Users can get help on an issue with a product, search relevant knowledge articles, or create a case for the issue.

    -   Get Help \(Template\)

        This topic is for users who are not logged in and want to chat anonymously. Users can use keywords and search relevant knowledge articles or choose to be transferred to a live agent. You can integrate this topic with the [Virtual agent - Facebook messaging integration](../task/update-authentication-facebook-va-integration.md) to enable chat using your messaging application.

    -   Get Help with an Order \(Template\)

        Users can get help on an issue with an existing order, search relevant knowledge articles, or create a case for the issue.

    -   Submit Request \(Template\)

        Users can submit a request for searching and using one of the catalog items.

    -   Create Case

        Creates a case from Virtual Agent when no relevant topics for the issue you have are displayed.

    -   Update Case

        Users can update a case from Virtual agent.


Your users can run the published topics in your chat support client.

## Activating Virtual Agent conversations with NLU

-   The Customer Service NLU Model for Virtual Agent Conversations \(com.sn\_csm.nlu\) plugin is automatically enabled when you enable the Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\).

    After you enable the plugin, you can view the following read-only intents for the Customer Service NLU for VA models in Studio:

    -   CheckCaseStatus
    -   GetHelp
    -   GetHelpWithProduct
    -   GetHelpWithOrder
    -   SubmitRequest
    Each intent corresponds to a [chatbot topic](../task/csm-virtual-agent-conversation.md). To customize an intent, you can [import](https://www.servicenow.com/docs/access?context=import-nlu-intent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) an existing intent from the Customer Service NLU for Virtual Agent model and then [link the NLU model with the associated intent for the topic](https://www.servicenow.com/docs/access?context=va-NLU&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

-   Enable ServiceNow NLU in the [general settings](https://www.servicenow.com/docs/access?context=va-conversation-settings&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

**Related topics**  


[Get help using virtual agent conversations](../task/csm-virtual-agent-conversation.md)

[Natural Language Understanding in Virtual Agent](https://www.servicenow.com/docs/access?context=va-NLU&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

