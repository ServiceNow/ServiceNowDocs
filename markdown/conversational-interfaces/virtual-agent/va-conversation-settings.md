---
title: Customizing a Virtual Agent chat experience
description: Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-conversation-settings.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Chat, experiences, Virtual Agent, AI Search, Conversational Interfaces, custom greetings and setup]
breadcrumb: [Configure, Virtual Agent, Conversational Interfaces]
---

# Customizing a Virtual Agent chat experience

Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.

## Get started with chat experiences

Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**, and then select **Virtual Agent**. Use the **Custom Greetings and Setup** tile to manage the default and custom chat experiences. You can do the following:

-   Configure the default chat experience, including the setup topics, promoted assets, and search criteria used. For example, you can activate the Virtual Agent Feedback setup topic so that it is applied to all your bot conversations.
-   Create different custom chat experiences based on the context in which your end users run Virtual Agent. The settings that you define in a custom chat experience override the default chat experience.

## How chat experiences work

A chat experience defines the structure of a bot conversation \(setup topics\), an initial set of topics displayed to users \(promoted assets\), and the AI Search configurations for displaying search results in conversations. Virtual Agent provides a preconfigured, default chat experience that you \(admins and topic authors\) can use to control the user experience with Virtual Agent.

You can configure the default chat experience and also create custom chat experiences, tailored to the context in which different users run Virtual Agent, such as the service portal or channel that they're using. Custom chat experiences inherit the default chat experience settings, but you can override the defaults as needed for a given context.

A chat experience consists of setup topics, promoted assets, and a search profile:

-   **Setup topics**

    Virtual Agent provides common conversational elements, such as a welcome greeting to begin a conversation and a conversation closing, and automatically includes them in virtual agent conversations. These prebuilt elements, called setup topics, are part of a basic conversation structure that is applied to all your conversations. They are installed with Virtual Agent.

    These setup topics run automatically at appropriate points in a conversation, based on the topic description or keywords that users enter during the conversation.

    \[Omitted image "setup-topics-example.png"\] Alt text: Virtual Agent conversation window showing prebuilt setup topics: Greeting, LLM topic, and Closing.

    1.  Greeting
    2.  LLM topic \(conversational catalog request\)
    3.  Closing
    Virtual Agent provides the following types of prebuilt setup topics:

    |Setup topic|Description|
    |-----------|-----------|
    |Greeting|Presents a welcome greeting to users, and asks users to enter a request or see what items it can assist with.|
    |Provide Virtual Agent Feedback|Displays a survey to get user feedback on the conversational experience, before the conversation ends.|
    |Live Agent Support|Enables users to request a live agent transfer and view items that the live agent can assist with.|
    |Virtual Agent Capabilities|Presents a list of what the virtual agent can help with.|
    |Error Handling Topic|Displays a standard error message when an unrecoverable system error occurs and transfers the user to a live agent.|
    |Closing Conversation|Displays a closing message that ends the conversation.|
    |AI Search Fallback|Generates AI Search results for a user when Virtual Agent can't find a matching intent and topic or keyword.|
    |Fallback Topic|Presents standard messages that ask the user to enter another request or select a different topic when the virtual agent does not understand a user entry or selection.|
    |Anything Else Topic|After completing a task or request, virtual agent asks if the user needs further assistance with another request or task.|

    Setup topics for LLM conversations rely on their own descriptions as the intents, which the LLM uses for topic discovery.

    You can preview \(test\) the prebuilt setup topics to see how they work. On the Assistant Designer home page, use the filter icon \[Omitted image "filter-icon.png"\] Alt text: Filter icon. to sort only for Setup Topics, and then select the setup topics to test. Prebuilt topics are read-only, but you can duplicate, customize \(modify\) if needed, and publish them.

-   **Promoted topics**

    You can display a collection of up to six topics that are relevant to your users, displayed before the **Show me everything** button in the chat window. You can use these promoted assets in a chat experience to give your users quick and convenient access to the topics used for a given context.

    **Note:** Promoted topics may not be supported on all clients.

    For more information, see [Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)

-   **Search profile**

    A search profile defines how Virtual Agent AI Search results are generated. You can assign search sources to a chat assistant. Search sources are used to determine what the assistant looks at to answer user queries. For more information, see [Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/add-info-sources-assistant.md).


