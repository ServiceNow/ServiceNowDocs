---
title: Suggested actions
description: Suggested actions prompt you with two suggested actions related to your prior conversation that you may consider doing next. Suggested actions appear at the end of your Now Assist in Virtual Agent conversation.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-04-02"
reading_time_minutes: 1
keywords: [Now Assist, Virtual Agent, Suggested actions, Next best action, genius results, generative AI]
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Suggested actions

Suggested actions prompt you with two suggested actions related to your prior conversation that you may consider doing next. Suggested actions appear at the end of your Now Assist in Virtual Agent conversation.

**Note:** Suggested actions must be turned on through the **sn\_nowassist\_va.enable\_suggested\_actions** system property. For more information on turning on this feature, see [Now Assist in Virtual Agent system properties](../reference/nava-sys-props.md).

Suggested actions are applicable to Now Assist in Virtual Agent standard chat and enhanced chat conversations. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, the suggested actions appear after a `Here's what you can do next` header.

![Suggested actions of block calendar and notify teammates appear under the Here's what you can do next header.](../image/NASS-dynamic-window-suggested-actions-yp6.png "Example of suggested actions in enhanced chat")

![Suggested actions of block calendar and notify teammates appear under the Here's what you can do next header.](../image/NAVA-standard-chat-suggested-actions.png "Example of suggested actions in standard chat")

Selecting a suggested action begins that action within the same chat conversation. If applicable, relevant information from the prior conversation, such as your name, is brought into the selected action. Suggested actions appear only once per last completed action. After completing the suggested action, standard chat conversations close and enhanced chat conversations remain active.

