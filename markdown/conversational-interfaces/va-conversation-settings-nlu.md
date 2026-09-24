---
title: \(Legacy\) Customizing a Virtual Agent NLU chat experience
description: Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/va-conversation-settings-nlu.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 9
keywords: [Chat, experiences, Virtual Agent, context, AI Search, Lite, custom, Conversational Interfaces, custom greetings and setup]
breadcrumb: [Configure NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Customizing a Virtual Agent NLU chat experience

Create different chat experiences for your end users based on the context in which they initiate a conversation with Virtual Agent.

## How chat experiences work

A chat experience defines the structure of a bot conversation \(setup topics\), an initial set of topics displayed to users \(promoted assets\), and the AI Search configurations for displaying search results in conversations. Virtual Agent provides a preconfigured, default chat experience that you \(admins and topic authors\) can use to control the user experience with Virtual Agent.

You can configure the default chat experience and also create custom chat experiences, tailored to the context in which different users run Virtual Agent, such as the service portal or channel that they're using. Custom chat experiences inherit the default chat experience settings, but you can override the defaults as needed for a given context.

**Note:** If you're using Virtual Agent Lite, you can configure certain setup topics in the default chat experience but you can't create custom chat experiences.

A chat experience consists of setup topics, promoted assets, and a search profile:

-   **Setup topics**

    Virtual Agent provides common conversational elements, such as a welcome greeting to begin a conversation and a conversation closing, and automatically includes them in virtual agent conversations. These pre-built elements, called setup topics, are part of a basic conversation structure that is applied to all your conversations. They are installed with Virtual Agent and Virtual Agent Lite.

    These setup topics run automatically at appropriate points in a conversation, based on the context, utterances \(if NLU is enabled\) or keywords that users enter during the conversation.

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

    In NLU conversations, setup topics have corresponding intents \(set in the pre-built NLU model for setup topics\) and also keywords. Virtual Agent recognizes the utterances or keywords that users can enter to run certain setup topics, such as the Virtual Agent Capabilities \(help\) topic or the Live Agent support topic.

    You can preview \(test\) the pre-built setup topics to see how they work. On the Virtual Agent Designer home page, use the filter icon \[Omitted image "filter-icon.png"\] Alt text: Filter icon. to sort only for Setup Topics, and then select the setup topics to test. Pre-built topics are read-only, but you can duplicate, customize \(modify\) if needed, and publish them.

-   **Promoted topics**

    You can display a collection of up to six topics that are relevant to your users, displayed before the **Show me everything** button in the chat window. You can use these promoted assets in a chat experience to give your users quick and convenient access to the topics used for a given context.

    **Note:** Promoted topics may not be supported on all clients.

-   **Search profile**

    A search profile defines how Virtual Agent search results are generated for an AI Search application. The search application's configuration specifies a search profile to use, and also determines how the generated results are displayed to users. Virtual Agent uses a default search application configuration and search profile that controls the data sources used for searches. Its UI configuration \(set in the Entity View Action Mapping application\) controls the search results displayed in Genius Result answer cards and multi-link output. These configurations also apply to search results generated as a fallback when Virtual Agent can't determine the appropriate topic. For more information, see [\(Legacy\) Implementing AI Search in NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-ai-search.md).


## Get started with chat experiences

Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**, and then select **Virtual Agent**. Use the **Custom Greetings and Setup** tile to manage the default and custom chat experiences. You can do the following:

-   Configure the default chat experience, including the setup topics, promoted assets, and search criteria used. For example, you can activate the Virtual Agent Feedback setup topic so that it is applied to all your bot conversations.
-   Create different custom chat experiences based on the context in which your end users run Virtual Agent. The settings that you define in a custom chat experience override the default chat experience.

<table id="table_kbf_kxv_fsb"><thead><tr><th>

I want to...

</th><th>

See these topics

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Display options

</td></tr><tr><td>

Branding

</td><td>

[Branding your chat client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/branding-chat-client.md)

</td></tr><tr><td>

Message preview

</td><td>

[Enable message preview on the chat widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/web-client-message-preview.md)

</td></tr><tr><td>

Public access

</td><td>

[Enable public access to the chat widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/enable-public-access-web-client.md)

</td></tr><tr><td class="sub-head" colspan="2">

Channels and routing

</td></tr><tr><td>

Channels

</td><td>

[Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md).

</td></tr><tr><td>

Pre-chat surveys

</td><td>

[\(Legacy\) Define pre-chat survey configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-pre-chat-surveys.md)

</td></tr><tr><td>

Context variables

</td><td>

[Configure context variables for storing chat-related information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-context-variables.md)

</td></tr><tr><td>

Topic context intent

</td><td>

[\(Legacy\) Define topic context intent configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-context-topic-intent.md)

</td></tr><tr><td class="sub-head" colspan="2">

System actions

</td></tr><tr><td>

System messages

</td><td>

[Change Virtual Agent and Agent Chat system messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-change-system-messages.md)

</td></tr><tr><td>

URL navigation

</td><td>

[\(Legacy\) URL navigation in NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/url-navigation-ci.md)

</td></tr><tr><td>

Sensitive data detection

</td><td>

[\(Legacy\) Configuring sensitive data handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-sensitive-data-handling.md)**Note:** This feature is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-privacy-landing.md).

</td></tr><tr><td>

Missed activity emails

</td><td>

[Sending missed chat activity emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/agent-chat/ac-missed-activity-emails.md)

</td></tr></tbody>
</table><table id="table_grb_xf4_swb"><thead><tr><th>

I want to...

</th><th>

See these topics

</th></tr></thead><tbody><tr><td>

Get recommendations for Virtual Agent topics based on my data

</td><td>

[\(Legacy\) Quick start for Topic Recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/getting-started-topic-recommendations.md)

</td></tr><tr><td>

Configure performance tracking for Virtual Agent topics

</td><td>

[\(Legacy\) Create deflection configurations and patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/set-up-deflection-settings-va.md)

</td></tr><tr><td>

Use Natural Language Understanding \(NLU\) for topic discovery

</td><td>

[\(Legacy\) Configure Natural Language Understanding in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-nlu-settings.md)

 [Creating models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/creating-models.md) \(using NLU Workbench\)

</td></tr><tr><td>

Create custom greetings and setup topics

</td><td>

[\(Legacy\) Configure a Virtual Agent NLU chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-default-chat-experience.md)

</td></tr><tr><td>

Determine which issues are routed to Virtual Agent first

</td><td>

[\(Legacy\) Configure and run an Issue Auto Resolution simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-ar-simulations.md)

</td></tr><tr><td>

Send notifications to users in Virtual Agent

</td><td>

[Configuring Virtual Agent notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configuring-va-notifications.md)

 [Enable Virtual Agent notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/enable-va-notifications.md)

</td></tr><tr><td>

Use AI Search to return fallback results for Virtual Agent

</td><td>

[\(Legacy\) Implementing AI Search in NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-ai-search.md)

</td></tr><tr><td>

Detect and dynamically translate Virtual Agent topics into a different language

</td><td>

[Language detection and dynamic machine translation in Virtual Agent in enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/dynamic-lang-detection-translation-enhanced-chat.md)

</td></tr></tbody>
</table>