---
title: Disable Dynamic Translation for LLM Virtual Agent conversations
description: Enable dynamic translation of chat messages into English before they are sent to the large language model in generative AI topics to support users who speak other languages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/disable-dynamic-translation-for-llm-va-conversations.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Disable Dynamic Translation for LLM Virtual Agent conversations

Enable dynamic translation of chat messages into English before they are sent to the large language model in generative AI topics to support users who speak other languages.

## Before you begin

You must have Dynamic Translation for Virtual Agent installed and active for your Virtual Agent. For more information, check out .

Role required: admin

## About this task

Dynamic Translation is enabled by default.

There are certain limitations of Dynamic Translation for Virtual Agent. Catalog item names aren't automatically translated, and only languages configured for language detection will be recognized.

## Procedure

1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.

2.  Select the magnifying glass icon \(\[Omitted image "magnifying-glass-fill-24.svg"\] Alt text:\) to expand the column search row.

3.  In the Name column, enter `sn_generative_ai.disable_dynamic_translation` and then press **Enter** to search.

4.  Open the matching record.

5.  Set the property value to `true`.

6.  Select **Save** to save the record.


## Result

Chat requester utterances are translated into English before being sent to the LLM, and output messages are translated back into the requester's preferred language.

