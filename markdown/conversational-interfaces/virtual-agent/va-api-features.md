---
title: Virtual Agent API features
description: You can use the Virtual Agent API to integrate many of the same features that are available in Virtual Agent and Agent Chat into your chat environment. Feature support varies depending on your ServiceNow release and the Store app version number of the API.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent API features

You can use the Virtual Agent API to integrate many of the same features that are available in Virtual Agent and Agent Chat into your chat environment. Feature support varies depending on your ServiceNow release and the Store app version number of the API.

For information about the request and response templates for Virtual Agent API, as well as examples of common use cases, see [Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

## Key features

The main features in Virtual Agent API starting with version 1.0.9 include the following:

-   Provider authentication using static, hash, and token-based authentication
-   Auto-linking user IDs to ServiceNow accounts for a personalized experience
-   Virtual Agent transfer to a live agent in Agent Chat
-   Intent classification in bot-to-bot integrations through the following strategies:
    -   The primary bot determines the user intent and sends the user request to Virtual Agent so that the corresponding topic is displayed to the user.
    -   The primary bot sends the user utterance to Virtual Agent so that it can discover the intent and return a prediction confidence score. A higher confidence score indicates that the predicted topic more accurately matches the user utterance.

## Version 1.0.12 features

-   **[Automatically close idle bot-to-bot conversations](va-b2b-open-conversation.md)**

    You can automatically close conversations that have been idle for more than one hour. The **Time Out Abandoned B2B Conversations** job runs hourly each day and automatically closes idle conversations that requesters have abandoned.

-   **[Conversation states and reason codes in Virtual Agent interaction records](va-interactions.md)**

    When a user or primary bot ends a conversation, Virtual Agent records the state and reason codes in the interaction records. For example, an end user can type **End** to stop the conversation or click the **X** button to close the chat.

-   **Notifying when a conversation ends**

    The primary bot is notified when Virtual Agent or Agent Chat conversations end. The primary bot is also notified when it must take control of a conversation. Virtual Agent uses the following flags:

    -   **completed**: Sent when the conversation with Virtual Agent or a live agent is finished.
    -   **takeControl**: Sent when the primary bot must take control. This typically occurs when Virtual Agent can't determine the conversation intent after two consecutive attempts \(the default value\). You can add the **va.bot.to.bot.take.control\_times** system property to change the default number of attempts that Virtual Agent tries to determine the conversation intent.
    For more information, see [Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

-   **Changes with intents**
    -   Share the NLU confidence score for an intent match if NLU is enabled in Virtual Agent.
    -   Enable end users to jump directly into a topic based on intent matching by the primary bot.

## Version 1.3.0 features

Starting with version 1.3.0, Virtual Agent API supports logging as a system property \(**va.bot.to.bot.logging\_enabled**\).

**Parent Topic:**[Using Virtual Agent API](virtual-agent-api.md)

