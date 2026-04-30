---
title: Natural Language Understanding topic discovery logic in Virtual Agent
description: Understand how Virtual Agent returns intents and how it selects which intents to show to the user.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [NLU, Virtual agent]
breadcrumb: [Debug a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Natural Language Understanding topic discovery logic in Virtual Agent

Understand how Virtual Agent returns intents and how it selects which intents to show to the user.

## Prerequisites for topic discovery

Virtual Agent can discover a topic when the following conditions are met:

-   The topic must be published and active.

    In the Topics \[sys\_cs\_topic\] table, the **Active**, **Published**, and **Is Topic Discoverable** values are set to **true**.

    **Note:** The **Is Topic Visible** column does not affect topic discovery.

-   The topic must be discoverable.
-   Topic conditions must evaluate to true at runtime.
-   If any roles are configured for the topic, the requestor must have at least one of those roles.
-   The topic's NLU model must have a binding for the session language.

## NLU topic discovery logic

Virtual Agent sends a prediction request to the NLU provider. The request contains the utterance and all registered NLU model IDs that are bound to the session language. Matches return NLU intents that correspond with a topic. Virtual Agent then responds in one of the following ways:

-   Automatically selects a topic for the requester, based on the confidence score.
-   Prompts the requester to pick a topic from the returned list of matches.
-   Finds no matching topics.

If no matches are found but backup keywords are enabled \(the **com.glide.cs.nlu.keywords.enabled** property is **true**\), Virtual Agent searches for a topic based on keywords.

![Topic discovery flow chart showing the process Virtual Agent uses to deliver a topic to the user.](../images/va-topic-discovery-logic.png "Virtual Agent topic discovery logic")

## Virtual Agent NLU confidence scores

Virtual Agent uses confidence scores to return predicted intents. To set the confidence value:

1.  Navigate to **Conversational Interfaces** &gt; **External NLU Integrations** &gt; **Drivers**.
2.  Select **ServiceNow NLU**. You can also select All and enter `open_nlu_driver.list`.
3.  In the **Intent Confidence Threshold** field, enter the confidence threshold.

If an intent's confidence score is greater than or equal to the configured threshold, Virtual Agent considers it a good match.

Virtual Agent uses the following logic when selecting intents:

-   Auto-selects the highest predicted intent.

    This occurs when only one intent is matched, or in the event of a tie-breaker, when the next closest match is a distant second.

    **Note:** If ServiceNow NLU is used and the **Intent Confidence Delta** field in the ServiceNow NLU driver table \(open\_nlu\_driver.list\) is set to **0**, there can be no tiebreaker.

-   Returns a topic list for the requester to choose from.

    This occurs if auto-select is not applicable. The length of the list is determined by the **com.glide.cs.max\_number\_display\_topics** system property.

-   No intents are matched.

    When zero NLU Intents are predicted with a confidence score greater than or equal to the configured threshold, Virtual Agent falls back to a keyword search if configured. \(The **com.glide.cs.nlu.keywords.enabled** and **com.glide.cs.nlu.keywords.include\_topics\_bound\_to\_lang** system properties are **true**\).


## Mid-topic NLU topic discovery logic

While a topic is running, the requester can enter an utterance or phrase that results in a topic switch. For example:

1.  The requester is in a Virtual Agent conversation, and Topic A is running.
2.  Topic A prompts the user to enter their date of birth.
3.  Instead of choosing a date, the requester types, "I want to view my Incidents."
4.  Virtual Agent can't resolve this phrase to a date, so it issues an NLU prediction request.
5.  The NLU predictor returns Intent B, and Virtual Agent sees that Topic B is bound to Intent B.
6.  Virtual Agent switches the conversation to Topic B, which then presents information to the requester about their incidents.

![Topic discovery flow chart that shows the process Virtual Agent uses to change topics in the middle of a conversation.](../images/va-midtopic-discovery-logic.png "Virtual Agent mid-topic discovery logic")

**Parent Topic:**[Debug a Virtual Agent topic](../reference/virtual-agent-troubleshooting-guide.md)

**Related topics**  


[Resolve Natural Language Understanding \(NLU\) topic discovery issues](../reference/va-topic-discovery-issues.md)

