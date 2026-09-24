---
title: Creating a Virtual Agent topic
description: Use the Assistant Designer Asset library to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/create-virtual-agent-topic.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [Create, Virtual Agent, topic, topic, designer, conversations, LLM, Large language model]
breadcrumb: [Build conversations, Virtual Agent, Conversational Interfaces]
---

# Creating a Virtual Agent topic

Use the Assistant Designer Asset library to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.

## Before you begin

\[Omitted video\] Description: Assistant Designer LLM topic authoring video

Do the following:

-   Review [Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md).
-   Configure Virtual Agent settings. For example, if you're creating large language model \(LLM\) topics, turn on ServiceNow Otto for Virtual Agent. For more information, see [Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-now-assist-va.md).
-   Plan your conversation before you begin. For more information, see [Designing a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/design-va-topic.md).
-   Verify that you're in the appropriate application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the **ITSM Virtual Agent Conversations** scope.

Role required: virtual\_agent\_admin or admin

## About this task

The topic is in the Inactive state until you publish it. Publishing a topic changes the topic state to Active and automatically deploys the topic to your Virtual Agent clients.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Set the topic discovery toggle switch to **LLM**.

4.  Select **Create asset**.

    \[Omitted image "vad-home-2.png"\] Alt text: Asset library page.

5.  From the Create asset window, select **Topic**.

    **Important:** Selecting any of the other topics in the window will open the create flow in the respective application.

    \[Omitted image "create-asset-2.png"\] Alt text: List of assets, select topic to create a topic.

6.  On the form, fill in the fields.

    For a description of the field values, see [Create a topic form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topic-creation-form.md).

7.  After filling the topic creation form, select **Create**.

8.  On the **Flow** tab, build the conversation flow.

<table id="table_mmy_blm_hmb"><thead><tr><th>

Flow steps

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add controls

</td><td>

To create the topic flow:

1.  Select the controls for user inputs, bot responses, or utilities from the palette and drop them onto the canvas.

When you add a control to the canvas, it becomes a node in the conversation flow.

2.  For each node, complete the corresponding property sheet. In the topic header bar, select **Save**. The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for 4 seconds, and can be closed by selecting the **X** in the message.

For details about each control and the corresponding properties that you define, see [User inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-user-inputs.md), [Bot responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-bot-responses.md), and [Utilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-utilities.md).

 As you add controls, watch for a yellow warning badge or a red error badge in the corner of the control. The number on the badge indicates the number of issues in that control, such as missing mandatory information in the property sheet. \(Highlighting a badge or the "Incomplete" banner at the top of the property sheet details the items in need of correction.\)

</td></tr><tr><td>

Move a node

</td><td>

Select the node, drag it to the new location in the flow, and Select **Save**.

</td></tr><tr><td>

Delete a node

</td><td>

Select the **X** in the upper right corner of the node. In the topic header bar, select **Save**. The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for 4 seconds, and can be closed by selecting the **X** in the message.

 **Note:** You can't delete a node that has a script variable used by subsequent JavaScript expressions in the flow. Also, you can delete a decision node only when it has a single branch.

</td></tr></tbody>
</table>9.  Select **Test** in the header bar to test your topic in a chat window.

    You can review test results in the adjoining tabs. For detailed information, see [Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/test-llm-topics.md).

    If the ServiceNow Otto panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Otto panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments. For more information, see [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md).

10. When you're finished with the topic, select **Save** in the topic header bar.

    The topic is in the Inactive state until you publish it.

    The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for four seconds, and can be closed by selecting the **X** in the message.


## What to do next

[Publish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md) the topic to deploy the topic to your Virtual Agent clients. The topic state changes to Active.

If you created a topic that might be frequently used in certain contexts \(environments\), consider promoting the topic as part of the [default or custom chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-conversation-settings.md).

**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

