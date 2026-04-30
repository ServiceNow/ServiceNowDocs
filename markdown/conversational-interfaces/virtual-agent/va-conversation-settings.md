---
title: Setting up chat experiences for Virtual Agent users
description: Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [Chat, experiences, Virtual Agent, context, AI Search, Lite, custom, Conversational Interfaces, custom greetings and setup]
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Setting up chat experiences for Virtual Agent users

Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.

## How chat experiences work

A chat experience defines the structure of a bot conversation \(setup topics\), an initial set of topics displayed to users \(promoted assets\), and the AI Search configurations for displaying search results in conversations. Virtual Agent provides a preconfigured, default chat experience that you \(admins and topic authors\) can use to control the user experience with Virtual Agent.

You can configure the default chat experience and also create custom chat experiences, tailored to the context in which different users run Virtual Agent, such as the service portal or channel that they're using. Custom chat experiences inherit the default chat experience settings, but you can override the defaults as needed for a given context.

**Note:** If you're using Virtual Agent Lite, you can configure certain setup topics in the default chat experience but you can't create custom chat experiences.

A chat experience consists of setup topics, promoted assets, and a search profile:

-   **Setup topics**

    Virtual Agent provides common conversational elements, such as a welcome greeting to begin a conversation and a conversation closing, and automatically includes them in virtual agent conversations. These pre-built elements, called setup topics, are part of a basic conversation structure that is applied to all your conversations. They are installed with Virtual Agent and Virtual Agent Lite.

    These setup topics run automatically at appropriate points in a conversation, based on the context, utterances \(if NLU is enabled\), topic description \(if LLM is enabled\) or keywords that users enter during the conversation.

    ![Virtual Agent conversation window showing pre-built setup topics: Greeting, Virtual Agent capabilities, Anything else, Survey, and Closing.](../images/setup-topics-example.png "Example setup topics in a conversation")

    Virtual Agent provides the following types of pre-built setup topics:

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

    In NLU conversations, setup topics have corresponding intents \(set in the pre-built NLU model for setup topics\) and also keywords. Virtual Agent recognizes the utterances or keywords that users can enter to run certain setup topics, such as the Virtual Agent Capabilities \(help\) topic or the Live Agent support topic. Setup topics for LLM conversations rely on their own descriptions as the intents, which the LLM uses for topic discovery.

    You can preview \(test\) the pre-built setup topics to see how they work. On the Virtual Agent Designer home page, use the filter icon ![Filter icon.](../images/filter-icon.png) to sort only for Setup Topics, and then select the setup topics to test. Pre-built topics are read-only, but you can duplicate, customize \(modify\) if needed, and publish them.

-   **Promoted topics**

    You can display a collection of up to six topics that are relevant to your users, displayed before the **Show me everything** button in the chat window. You can use these promoted assets in a chat experience to give your users quick and convenient access to the topics used for a given context.

    **Note:** Promoted topics may not be supported on all clients.

    ![Promoted topics displayed after Virtual Agent Greeting setup topic.](../images/promoted-topics-example.png "Example promoted assets")

    For more information, see [Promote or demote LLM conversational subflows, actions, and topics in Virtual Agent Designer](../task/promote-demote-va-topics.md)

-   **Search profile**

    A search profile defines how Virtual Agent search results are generated for an AI Search application. The search application's configuration specifies a search profile to use, and also determines how the generated results are displayed to users. Virtual Agent uses a default search application configuration and search profile that controls the data sources used for searches. Its UI configuration \(set in the Entity View Action Mapping application\) controls the search results displayed in Genius Result answer cards and multi-link output. These configurations also apply to search results generated as a fallback when Virtual Agent can't determine the appropriate topic. For more information, see [Improving the user experience with AI Search](va-ai-search.md).

    ![Virtual Agent chat window showing AI Search results.](../images/va-ai-search-example3.png "Example AI Search result")


## Get started with chat experiences

Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**, and then select **Virtual Agent**. Use the **Custom Greetings and Setup** tile to manage the default and custom chat experiences. You can do the following:

-   Configure the default chat experience, including the setup topics, promoted assets, and search criteria used. For example, you can activate the Virtual Agent Feedback setup topic so that it is applied to all your bot conversations.
-   Create different custom chat experiences based on the context in which your end users run Virtual Agent. The settings that you define in a custom chat experience override the default chat experience.

-   **[Working with setup topics](working-setup-topics.md)**  
Setup topics are part of a standard conversation structure applied to all your conversations, such as the welcome greeting or fallback responses. Setup topics run at the appropriate spot in a conversation based on the context, keywords, or utterances entered by the user, and any conditions that are specified for the setup topic.
-   **[Configure a Virtual Agent chat experience](../task/configure-default-chat-experience.md)**  
Change the preconfigured Virtual Agent default chat experience or create a custom chat experience for your users. You can configure setup topics, specify promoted topics, and if needed, change the search profile.
-   **[Test chat experiences](../task/test-custom-experience.md)**  
After you create or modify a Virtual Agent chat experience, you can test \(simulate\) it to verify that it works as expected.

**Parent Topic:**[Configuring Virtual Agent](configure-virtual-agent.md)

