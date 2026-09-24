---
title: Testing assistants
description: Simulate and test assistant conversations from Asset library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/testing-enhanced-chat-conversations.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Now Assist, Virtual Agent, enhanced chat, topics, subflows, actions, assistant]
breadcrumb: [Build conversations, Virtual Agent, Conversational Interfaces]
---

# Testing assistants

Simulate and test assistant conversations from Asset library.

You can test assistants directly from the Asset library.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.
2.  Select the **Asset library** tab.
3.  Select the **LLM** option.
4.  From the Assistant list, select the assistant that you want to test. The assets available to the selected assistant is shown under All assets.
5.  Select **Test assistant**.

    **Note:** You can test both active and inactive assistants.


\[Omitted image "full-page-VAD-home-page-test-2.png"\] Alt text: Test in enhanced chat from the Assistant Designer Asset library's Test assistant drop-down menu.

Depending on the chat experience set up for the assistant, you can test using [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/nava-standard-chat.md) experience or [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/nava-enhanced-chat.md) experience. For more information about setting up the chat experience for an assistant, see [Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/manage-assistant-chat-experience.md).

**Note:** The ServiceNow Otto Panel - Platform \(default\) assistant can also use the [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/nava-integrated-chat.md) experience. The premium experience is configured by default.

**Note:** Enhanced chat experience is the default for Assistant Designer test panels. To change the default experience to standard chat, set the value of the system property **sn\_nowassist\_va.standard\_chat\_enabled** to true.

For all the ServiceNow Otto assistants and the ServiceNow Otto Panel - Platform Assistant, when testing the assistant:

-   If the assistant has the Standard Chat experience configured for any display location, you can choose between Standard Chat and Enhanced Chat.
-   If the assistant only has the Enhanced Chat experience configured across all display locations, when you select **Test Assistant**, you're directed to test the Enhanced Chat experience.

For the ServiceNow Otto Panel - Developer Assistant, when testing the assistant by selecting **Test Assistant**, you're directed to test the Standard Chat experience.

-   **[Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/test-llm-topics.md)**  
Preview, test, and debug topics that use large language models \(LLMs\) in the Assistant Designer Asset library chat window.
-   **[Debug a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/virtual-agent-troubleshooting-guide.md)**  
Investigate and resolve unexpected behavior in your custom Virtual Agent topics, topic blocks, and controls.

**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

**Related topics**  


[Test details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/test-llm-details.md)

