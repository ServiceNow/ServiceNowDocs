---
title: Testing LLM topics
description: Preview, test, and debug topics that use large language models \(LLMs\) in the Assistant Designer Asset library chat window.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/test-llm-topics.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [LLM, Topic, Testing, Virtual Agent, Large Language Model]
breadcrumb: [Test and improve, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Testing LLM topics

Preview, test, and debug topics that use large language models \(LLMs\) in the Assistant Designer Asset library chat window.

## About testing LLM topics

You can test your topic's functions by running your conversation in a chat test window as you work. The web \(Service Portal\) chat client is the default test window.

If you're using the [Virtual Agent integrations with third-party messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md), elements in your conversation might appear differently in third-party messaging applications. Test your conversations in any third-party applications where you want to deploy Virtual Agent.

**Note:** If the ServiceNow Otto panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Otto panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.

## Starting a test

You can find the testing option on the Assistant Designer canvas.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.
2.  Select the **Asset library** tab.
3.  Select the topic that you want to test.
4.  Select **Test**.

    \[Omitted image "va-test-ui-options-llm-4.png"\] Alt text: Assistant Designer Asset library list and topic canvas views. Test options on both are highlighted.


The chat test window opens in the ServiceNow Otto for Virtual Agent chat widget.

\[Omitted image "test-llm-widget.png"\] Alt text: The chat test window opens with the default response from the assistant.

If the topic is associated with multiple LLM assistants, select the **Test skill discovery** check box, then open the Assistant drop-down list to select which assistant you want to test. For more information about LLM assistants, see [Create LLM assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/llm-assistants.md).

**Note:** The **Test in enhanced chat** option is available only from the Asset library list view. The **Test** button in the topic canvas adds options in a drop-down box if you configure Microsoft Teams or Slack for Virtual Agent.

\[Omitted image "va-llm-test-window-assistants.png"\] Alt text: Add assistants in the Properties tab, followed by the Test skill discovery check box in the topic testing window, to select an assistant in the drop-down window.

**Note:** If your topic is missing any necessary information, an incomplete badge appears in the corner of the flow diagram pane. A warning badge also appears next to each node. The incomplete badge lists the total number of issues, while the local warning badges show how many issues are found in each node. If you select **Test** when there are issues, an Issues window opens with the number of issues present along with the details of each issue. These details include a full description and a hyperlink to each incomplete item.

## Feedback

You can provide feedback to each utterance made by the LLM by selecting from the like thumbs-up icon \[Omitted image "llm-thumbs-up-like.png"\] Alt text: or dislike thumbs-down icon \[Omitted image "llm-thumbs-down-dislike.png"\] Alt text: options that appear when you hover over an utterance. All LLM user inputs except the Input Collector have these feedback options.

\[Omitted image "llm-test-thumbs-up-down.png"\] Alt text: The bot asks: which color do you prefer? Red or green? A thumbs up and a thumbs down icon appear in the chat window.

If you run tests from the Topics page, the test window shows only the **Analyze test phrases**, **Variables**, **Context** \(available by default, with no **Include topic discovery** option\), and **Logs** tabs.

## Next steps

When you're done testing your topic, close the test chat window. If necessary, use the test information to adjust your topic to perform more accurately. For example, the results on the **Analysis** tab may return low scores or `Unsure` or `Unknown` confidence ratings. Improve scores by updating the topic description or instructions in the LLM user input nodes.

-   **[Test details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/test-llm-details.md)**  
The chat test window displays adjoining tabs that provide details about your topic as you test it.

**Parent Topic:**[Testing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/testing-enhanced-chat-conversations.md)

