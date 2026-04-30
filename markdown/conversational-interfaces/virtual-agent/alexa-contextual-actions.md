---
title: Contextual actions for Alexa
description: Use the contextual actions supported by Conversational Integration with Alexa to receive an appropriate response during custom chat integrations with Alexa.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience, Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Conversational IVR with Amazon Connect, Virtual Agent integration with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Contextual actions for Alexa

Use the contextual actions supported by Conversational Integration with Alexa to receive an appropriate response during custom chat integrations with Alexa.

## Hi

You can type or speak the `hi` command to initiate a conversation, in the middle of a conversation, or even inside a specific topic.

When you type or say `hi` in the middle of the topic, you are shown an option to either **End conversation** or to **Cancel**. If you end the conversation, the Alexa skill is reset and you can restart the skill by speaking your invocation name. If you cancel the conversation, you are redirected to the last topic that you were at.

## Bye

The `Bye` command is used to end a conversation.

You can type `bye` or speak this command in the middle of a conversation to end the conversation.

## Help

The `help` command is used to request help using the bot.

You can type `help` or speak this command to ask your Alexa skill any questions. If you want to restart the conversation, say `hi` or restart the conversation.

## Restart

The `restart` command is used to end a bot conversation that is either in progress or runs into an error, and then begin a new conversation.

You can type `restart` or speak this command anywhere in the middle of a conversation.

**Note:** For excluding contextual actions Logout/Notifications for Alexa, you must add the records to the Excluded channel table \[sys\_cs\_contextual\_action\_excluded\_channel\].

