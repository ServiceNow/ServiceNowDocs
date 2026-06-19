---
title: Testing Now Assist enhanced chat conversations
description: Test conversational assets with assistants in enhanced chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/testing-enhanced-chat-conversations.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-11-06"
reading_time_minutes: 1
keywords: [Now Assist, Virtual Agent, enhanced chat, topics, subflows, actions, assistant]
breadcrumb: [Testing LLM topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Testing Now Assist enhanced chat conversations

Test conversational assets with assistants in enhanced chat.

You can test conversational assets such as topics, subflows, and actions in Assistant Designer using the enhanced chat requester view. You can only test conversations for assistants that have the enhanced chat turned on and configured in **All** &gt; **Conversational Interfaces** &gt; **Assistants**. After the enhanced chat is turned on for an assistant, in the Assistant Designer Asset library, select **Test assistant** &gt; **Test in enhanced chat** to test the associated conversational assets.

\[Omitted image "full-page-VAD-home-page-test.png"\] Alt text: Test options shown in theAssistant Designer Asset library's Test assistant drop-down menu. \[Omitted image "full-page-VAD-home-page-test-2.png"\] Alt text: Test options shown in theAssistant Designer Asset library's Test assistant drop-down menu.

**Note:** Enhanced chat experience is the default for Assistant Designer test panels. To change the default experience to standard chat, set the value of the system property **sn\_nowassist\_va.standard\_chat\_enabled** to true.

For all the Now Assist for Virtual Agent assistants and the Now Assist Panel - Platform Assistant, when testing the assistant:

-   If the assistant has the Standard Chat experience configured for any display location, you can choose between Standard Chat, Enhanced Chat, or Integrated Chat.
-   If the assistant only has the Enhanced Chat or Integrated Chat experience configured across all display locations, when you select **Test Assistant**, you can choose between those options.

For the Now Assist Panel - Developer Assistant, when testing the assistant by selecting **Test Assistant**, you're directed to test the Standard Chat experience.

**Parent Topic:**[Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/test-llm-topics.md)

