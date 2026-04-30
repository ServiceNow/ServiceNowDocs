---
title: Dialog Acts for Virtual Agent
description: As part of the Vancouver release, the Dialog Acts feature expands natural language communication with Virtual Agent, leading to more fluid conversations between user and agent.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent, Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Dialog Acts for Virtual Agent

As part of the Vancouver release, the Dialog Acts feature expands natural language communication with Virtual Agent, leading to more fluid conversations between user and agent.

## How Dialog Acts works

Dialog Acts interprets and applies user inputs during a Virtual Agent conversation. With this feature active, you engage with Virtual Agent in your own natural language, instead of selecting replies based on prompts in the topic.

For example, if you request a laptop in a Virtual Agent conversation, you use the topic prompts to select a manufacturer, screen size, and amount of RAM. Without Dialog Acts, you change specifications only by following the prompts in the topic, potentially taking more time to loop through a Virtual Agent conversation as you reset your options. With Dialog Acts, if you change your mind about any of the laptop's specifications before finishing the request, you can input an utterance such as, "Actually, I need 8 GB of RAM." If your input matches the Natural Language Understanding \(NLU\) model closely enough, the specifications are changed immediately, even if you're on a different point in the topic. If the input doesn't match, it's added to a list of ignorable utterances.

User utterances are stored in the Open NLU Predict State Tracking \[open\_nlu\_predict\_state\_tracking\] table, while feedback is tracked by the Open NLU Predict Dialog Act Feedback \[open\_nlu\_predict\_dialog\_act\_feedback\] table. Languages are tracked in the Open NLU Driver Languages \[open\_nlu\_driver\_language\] table. In the current release, English is the sole language support for Dialog Acts.

## Activating Dialog Acts

Activate Dialog Acts by toggling the **Enable Dialog Acts** switch in the [Create a topic form](../reference/vad-topic-creation-form.md) or the [Topic Properties tab](../reference/vad-topic-properties-tab.md). When activated, a second **Confirm modified values** toggle appears. Use this switch to provide a prompt confirming that a variable is to be changed based on your utterances.

## Considerations for implementing Dialog Acts

The Dialog Acts feature is available as long as NLU is active for the instance and the topic. However, at least one of the preconfigured responses must be Active for the Dialog Acts toggles in the [Topic Properties tab](../reference/vad-topic-properties-tab.md) to be available. Dialog Acts can work without a model intent, but it can't select an entity if the topic is not associated with that model or intent.

Decision nodes can be modified by a condition or script to skip reprompting by Dialog Acts. However, the **Modify Dialog Acts** toggle doesn't work if there are multiple date-time nodes on a topic.

## Available Dialog Acts responses

The current release includes the following types of responses, stored in the Open NLU Dialog Acts \[open\_nlu\_dialog\_act\] table:

|Type|Description|
|----|-----------|
|Modify|Alter a variable recorded previously.|
|Affirm|Confirm a variable.|
|Negate|Decline confirming a variable.|

