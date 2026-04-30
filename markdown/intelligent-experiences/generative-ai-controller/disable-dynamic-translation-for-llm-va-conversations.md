---
title: Disable Dynamic Translation for LLM Virtual Agent conversations
description: Enable dynamic translation of chat messages into English before they are sent to the ServiceNow large language model \(Now LLM\) in generative AI topics to support users who speak other languages.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Disable Dynamic Translation for LLM Virtual Agent conversations

Enable dynamic translation of chat messages into English before they are sent to the ServiceNow® large language model \(Now LLM\) in generative AI topics to support users who speak other languages.

## Before you begin

You must have Dynamic Translation for Virtual Agent installed and active for your Virtual Agent. For more information, check out .

Role required: admin

## About this task

Dynamic Translation is enabled by default.

There are certain limitations of Dynamic Translation for Virtual Agent. Catalog item names are not automatically translated, and only languages configured for language detection will be recognized.

## Procedure

1.  Navigate to the System Properties table by entering `sys_properties.list` in the navigator.

2.  Search for select the `sn_generative_ai.disable_dynamic_translation` system property.

3.  Set the property value to `true`.

4.  Select **Save** to save the record.


## Result

Chat requester utterances are translated into English before being sent to Now LLM and output messages are translated back into the requester's preferred language.

