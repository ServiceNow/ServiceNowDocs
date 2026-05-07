---
title: Testing assistants
description: Simulate and test assistant conversations from Asset library.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 2
keywords: [Now Assist, Virtual Agent, enhanced chat, topics, subflows, actions, assistant]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Testing assistants

Simulate and test assistant conversations from Asset library.

You can test assistants directly from the Asset library.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.
2.  Select the **Asset library** tab.
3.  Select the **LLM** option.
4.  From the Assistant list, select the assistant that you want to test. The assets available to the selected assistant is shown under All assets.
5.  Select **Test assistant**.

![Test options shown in the Assistant Designer Asset library's Test assistant drop-down menu.](../images/full-page-VAD-home-page-test-2.png)

Depending on the chat experience set up for the assistant, you can test using [Standard chat](../../now-assist-in-va/concept/nava-standard-chat.md) experience or [Enhanced chat](../../now-assist-in-va/concept/nava-enhanced-chat.md) experience. For more information about setting up the chat experience for an assistant, see [Manage an assistant chat experience](../../now-assist-in-va/task/manage-assistant-chat-experience.md).

**Note:** The Now Assist Panel - Platform \(default\) assistant can also use the  experience. The premium experience is configured by default.

**Note:** Enhanced chat experience is the default for Assistant Designer test panels. To change the default experience to standard chat, set the value of the system property **sn\_nowassist\_va.standard\_chat\_enabled** to true.

For all the Now Assist for Virtual Agent assistants and the Now Assist Panel - Platform Assistant, when testing the assistant:

-   If the assistant has the Standard Chat experience configured for any display location, you can choose between Standard Chat, Enhanced Chat, or Integrated Chat.
-   If the assistant only has the Enhanced Chat or Integrated Chat experience configured across all display locations, when you select **Test Assistant**, you can choose between those options.

For the Now Assist Panel - Developer Assistant, when testing the assistant by selecting **Test Assistant**, you're directed to test the Standard Chat experience.

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

**Related topics**  


[Test details](../reference/test-llm-details.md)

