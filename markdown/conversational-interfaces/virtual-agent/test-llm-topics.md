---
title: Testing LLM topics
description: Preview, test, and debug topics that use large language models \(LLMs\) in the Assistant Designer chat window.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 3
keywords: [LLM, Topic, Testing, Virtual Agent, Large Language Model]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Testing LLM topics

Preview, test, and debug topics that use large language models \(LLMs\) in the Assistant Designer chat window.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

## About testing LLM topics

You can test your topic's functions by running your conversation in a chat test window as you work. The web \(Service Portal\) chat client is the default test window.

If you're using the [Virtual Agent integrations with third-party messaging apps](../concept/va-integration-messaging-apps.md), elements in your conversation might appear differently in third-party messaging applications. Test your conversations in any third-party applications where you want to deploy Virtual Agent.

**Note:** If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.

## Starting a test

You can find LLM testing option on the Virtual Agent Designer canvas.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.
2.  Select the **Asset library** tab.
3.  Select the **LLM** option.
4.  Select the topic that you want to test.
5.  Select **Test**.

    ![Assistant Designer Asset library list and topic canvas views. Test options on both are highlighted.](../images/va-test-ui-options-llm-4.png)


The chat test window opens in the Now Assist in Virtual Agent chat widget.

![](../images/test-llm-widget.png)

If the topic is associated with multiple LLM assistants, select the **Test skill discovery** check box, then open the Assistant drop-down list to select which assistant you want to test. For more information about LLM assistants, see [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md).

**Note:** The **Test in enhanced chat** option is available only from the Asset library list view. The **Test** button in the topic canvas adds options in a drop-down box if you configure Microsoft Teams or Slack for Virtual Agent.

![Add assistants in the Properties tab, followed by the Test skill discovery check box in the topic testing window, to select an assistant in the drop-down window.](../images/va-llm-test-window-assistants.png)

**Note:** If your topic is missing any necessary information, an incomplete badge appears in the corner of the flow diagram pane. A warning badge also appears next to each node. The incomplete badge lists the total number of issues, while the local warning badges show how many issues are found in each node. If you select **Test** when there are issues, an Issues window opens with the number of issues present along with the details of each issue. These details include a full description and a hyperlink to each incomplete item.

## Feedback

You can provide feedback to each utterance made by the LLM by selecting from the like thumbs-up icon ![](../images/llm-thumbs-up-like.png) or dislike thumbs-down icon ![](../images/llm-thumbs-down-dislike.png) options that appear when you hover over an utterance. All LLM user inputs except the Input Collector have these feedback options.

![LLM feedback options.](../images/llm-test-thumbs-up-down.png)

If you run tests from the Topics page, the test window shows only the **Analyze test phrases**, **Variables**, **Context** \(available by default, with no **Include topic discovery** option\), and **Logs** tabs.

## Next steps

When you're done testing your topic, close the test chat window. If necessary, use the test information to adjust your topic to perform more accurately. For example, the results on the **Analysis** tab may return low scores or `Unsure` or `Unknown` confidence ratings. Improve scores by updating the topic description or instructions in the LLM user input nodes.

-   **[Test details](test-llm-details.md)**  
The chat test window displays adjoining tabs that provide details about your topic as you test it.

**Parent Topic:**[Getting started with Virtual Agent Designer](conversation-designer-virtual-agent.md)

