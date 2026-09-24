---
title: Publish a Virtual Agent topic
description: Deploy an inactive topic or an updated topic to save it and make it available to users on Virtual Agent clients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Build conversations, Virtual Agent, Conversational Interfaces]
---

# Publish a Virtual Agent topic

Deploy an inactive topic or an updated topic to save it and make it available to users on Virtual Agent clients.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

You can also publish topic blocks and custom controls to make them available for use in calling topics.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Select the topic, topic block, or custom control to publish or republish.

4.  In the topic header bar, select **Publish**.

    Selecting **Publish** when there are issues present opens a Validation Issues tab next to the property sheet, which counts up and details all issues needing correction. These details include a hyperlink for each incomplete item. If the issue is in a node, selecting the hyperlink opens the property sheet for that node. As each issue is resolved, the list on the shelf updates to show the remaining errors. Once there are no issues to resolve, the publishing dialog box opens.

    \[Omitted image "va-validation-issues-tab.png"\] Alt text: Assistant Designer Asset library canvas sidebar showing Validation Issues tab containing error message and hyperlink to node containing error.

    The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for four seconds, and can be closed by selecting the **X** in the message.

    For topics, the topic state is Active and the Published state changes to Published just now.

5.  Verify that your topics work as expected by opening them in a test conversation window in one of the following ways.

<table id="choicetable_uyk_3w1_scc"><tbody><tr><td id="d94034e151">

**Topic Flow or Properties tab**

</td><td>

Select **Test**.

</td></tr><tr><td id="d94034e163">

**Asset library page**

</td><td>

Under the **Select assistant** drop-down menu, choose the assistant associated with your topic, and then select **Test assistant**.

</td></tr></tbody>
</table>    For more information about testing ServiceNow Otto LLM topics, see [Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/test-llm-topics.md).


## Result

The topic blocks and custom controls are published and are available for use in calling topics.

**Note:** Active topics, including setup topics and small talk topics, can also be available for use after the topics are published. For more information, see [Control topic discovery and visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/manage-topics-task.md).

**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

