---
title: Testing Now Assist enhanced chat conversations
description: Test conversational assets with assistants in the enhanced chat.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-11-06"
reading_time_minutes: 1
keywords: [Now Assist, Virtual Agent, enhanced chat, topics, subflows, actions]
breadcrumb: [Testing LLM topics, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Testing Now Assist enhanced chat conversations

Test conversational assets with assistants in the enhanced chat.

You can test conversational assets such as topics, subflows, and actions in Assistant Designer using the enhanced chat requester view. You can only test conversations for assistants that have the enhanced chat turned on and configured in **All** &gt; **Conversational Interfaces** &gt; **Assistants**. After the enhanced chat is turned on for an assistant, in the Assistant Designer Asset library, select **Test assistant** &gt; **Test in enhanced chat** to test the associated conversational assets.

![Test in enhanced chat from the Assistant Designer Asset library's Test assistant button.](../../now-assist-in-va/image/full-page-VAD-home-page-test.png "Example of Assistant Designer Asset library testing")

**Note:** Enhanced chat experience is the default for Assistant Designer test panels. To change the default experience to standard chat, set the value of the system property **sn\_nowassist\_va.standard\_chat\_enabled** to true.

For all the Now Assist for Virtual Agent assistants and the Now Assist Panel - Platform Assistant, when testing the assistant:

-   If the assistant has the Standard Chat experience configured for any display location, you can choose between Standard Chat versus Enhanced Chat.
-   If the assistant only has the Enhanced Chat experience configured across all display locations, when you select **Test Assistant**, you're directed to test the Enhanced Chat experience.

For the Now Assist Panel - Developer Assistant, when testing the assistant by selecting **Test Assistant**, you're directed to test the Standard Chat experience.

**Parent Topic:**[Testing LLM topics](../reference/test-llm-topics.md)

