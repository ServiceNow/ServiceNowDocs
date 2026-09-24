---
title: Using pre-chat surveys with context variables for topic discovery
description: Capture user input from pre-chat surveys to use as utterances or keywords for topic discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/using-context-intent-prechat-survey.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create chat surveys, General chat settings, Conversational Interfaces Home for NLU, Configure NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# Using pre-chat surveys with context variables for topic discovery

Capture user input from pre-chat surveys to use as utterances or keywords for topic discovery.

If you're using a pre-chat survey, you can use information supplied by the user to direct them to the appropriate Virtual Agent topic without asking them to choose from a list of available topics.

A good example of this is the CSP Anonymous Pre-Chat Survey, which is included with the Customer Service Management \(CSM\) application. This survey applies to guest users on the CSP portal. In addition to asking for the user's name and email address, the last question asks the user to briefly describe the issue. The answer is mapped to the short\_description field in the question settings. This is the context for the user's answer.

\[Omitted image "csp-anonymous-prechat-survey.png"\] Alt text: Settings for the Please briefly describe your issue question in Survey Designer.

The user response can be passed to Virtual Agent for use in topic discovery. In order to do this, you must create a record for it in General Chat Settings.

\[Omitted image "ci-topic-context-intent-card.png"\] Alt text: General Chat settings Channels and routing tab, with View All button highlighted in Topic context intent card.

The Pre-chat short description as NLU intent record allows the CSP Anonymous Pre-Chat Survey input to function a bit like an NLU intent. When the survey runs, the interaction's short\_description is used as the search text for the conversation. Virtual Agent uses this input for topic discovery so that users don't have to select a topic from the Greetings screen.

\[Omitted image "prechat-short-description-nlu-intent.png"\] Alt text: Context topic intent record view corresponding with the pre-chat survey, with context and condition fields highlighted.

