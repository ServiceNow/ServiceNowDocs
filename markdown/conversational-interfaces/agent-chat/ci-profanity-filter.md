---
title: Profanity Filter for Agent Chat overview
description: The Profanity Filter for Agent Chat prevents agents from sending messages to requesters that include profane language \(also known as forbidden keywords\). If an agent is upset and tries to send a message with offensive language, the Profanity Filter prevents the requester from seeing the message.
locale: en-US
release: yokohama
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Profanity Filter for Agent Chat overview

The Profanity Filter for Agent Chat prevents agents from sending messages to requesters that include profane language \(also known as forbidden keywords\). If an agent is upset and tries to send a message with offensive language, the Profanity Filter prevents the requester from seeing the message.

If an agent tries to send a message with profane language, the Profanity Filter blocks the message and flags the forbidden keywords. The Profanity Filter warns the agent that the message contains forbidden keywords and alerts the chat manager to the agent's use of profane language.

![Agent Chat conversation with a highlighted message containing a forbidden keyword.](../image/agent-chat-profanity-filter-agentside.png)

When the Profanity Filter detects forbidden keywords in a message entered by the agent:

-   the message containing the forbidden keywords is highlighted in the agent's chat window.
-   the agent receives a notification that they have used a forbidden keyword.
-   the message with the forbidden keyword is not sent to the requester.
-   if the agent has exceeded the number of forbidden keywords in a specified amount of time, a message is sent to the chat manager.
-   the forbidden keyword is marked in the transcript of the chat conversation.

## Notifying the chat manager

You can configure the Profanity Filter to notify the chat manager if an agent tries to use more than the specified number of forbidden keywords over the specified time. The Profanity Filter considers all conversations owned by the agent when determining the number of forbidden keywords used. If the agent tries to send a message with a forbidden keyword, the chat manager receives a notification. If the Manager Workspace or Agent Workspace is the active window, a real-time notification displays. If the Manager Workspace or Agent Workspace isn't the active window, a notification displays on the summary view in the Workspace notification menu. In the incident entry, the chat manager can review the incident and the chat log and privately message the agent.

## Machine learning-based or keyword-based

The Profanity Filter uses a machine learning-based model or a keyword-based model to determine whether a message includes forbidden keywords. The machine learning-based model analyzes keywords and phrases in the context of the agent's entire message before determining whether any forbidden keywords in the message should be considered profane. For example, the statement "I made a silly mistake" would be considered not profane while "You sound so silly" would be considered profane. The machine learning-model is not on each instance individually – you cannot change the model directly to account for customized keywords and phrases.

The keyword-based model compares a message against a list of forbidden keywords to determine whether something should be considered profane. You can allow certain keywords or phrases even if those keywords are considered profane in a generic sense. Common examples are book or movie titles that might contain forbidden keywords and but should still be allowed in a conversation. Conversely you can configure the Profanity Filter to block certain keywords or phrases even if the words may not always seem profane. The Profanity Filter analyzes each message against the list of allowed and forbidden keywords before running it through the model-based mode.

|Allowed keyword|Forbidden keyword|Message to be analyzed|System behavior|
|---------------|-----------------|----------------------|---------------|
| | |You are a dummy.|Message is blocked.|
|UNIX for Dummies| |The reference book "UNIX for Dummies" might be useful.|Message is allowed.|
|UNIX for dummies|stupid|"UNIX for Dummies" is a stupid book.|Message is blocked.|
| |foolish|I feel so foolish for not knowing the answer to your question.|Message is blocked.|
| | |I feel so foolish for not knowing the answer to your question.|Message is allowed.|

|Allowed keyword|Forbidden keyword|Message to be analyzed|System behavior|
|---------------|-----------------|----------------------|---------------|
| |dummy|You are a dummy.|Message is blocked.|
| | |You are a dummy.|Message is allowed.|

## Domain separation

The Profanity Filter works with domain separation. If the domain is set to Global, then the keywords apply to both the agent and requester domains. For the agent and requester to see each other's domain, the administrator must do one of the following:

-   Include the domain where the regular expression should be visible as a child domain to the corresponding parent domain.
-   Grant necessary access to the appropriate domain if it's a sister domain.
-   Set the keywords under a global domain.

