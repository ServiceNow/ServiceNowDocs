---
title: Using pre-chat surveys with context variables for topic discovery
description: Capture user input from pre-chat surveys to use as utterances or keywords for topic discovery.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Using pre-chat surveys with context variables for topic discovery

Capture user input from pre-chat surveys to use as utterances or keywords for topic discovery.

If you're using a pre-chat survey, you can use information supplied by the user to direct them to the appropriate Virtual Agent topic without asking them to choose from a list of available topics.

A good example of this is the CSP Anonymous Pre-Chat Survey, which is included with the Customer Service Management \(CSM\) application. This survey applies to guest users on the CSP portal. In addition to asking for the user's name and email address, the last question asks the user to briefly describe the issue. The answer is mapped to the short\_description field in the question settings. This is the context for the user's answer.

![Settings for the Please briefly describe your issue question in Survey Designer.](../image/csp-anonymous-prechat-survey.png "Question settings for the CSP Anonymous Pre-Chat Survey in Survey Designer")

The user response can be passed to Virtual Agent for use in topic discovery. In order to do this, you must create a record for it in General Chat Settings.

![General Chat settings Channels and routing tab, with View All button highlighted in Topic context intent card.](../image/ci-topic-context-intent-card.png "Topic context intent card in General Chat Settings")

The Pre-chat short description as NLU intent record allows the CSP Anonymous Pre-Chat Survey input to function a bit like an NLU intent. When the survey runs, the interaction's short\_description is used as the search text for the conversation. Virtual Agent uses this input for topic discovery so that users don't have to select a topic from the Greetings screen.

![Context topic intent record view corresponding with the pre-chat survey, with context and condition fields highlighted.](../image/prechat-short-description-nlu-intent.png "The Context topic intent record that corresponds with the pre-chat survey")

-   **[Define topic context intent configurations](../task/ac-configure-context-topic-intent.md)**  
Use pre-chat survey information to determine the appropriate Virtual Agent conversation topic automatically displayed to end users \(requesters\), rather than prompting them to choose from a list of conversation topics.

**Parent Topic:**[General chat settings](ci-configuring-chat-features.md)

