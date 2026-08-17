---
title: Publish a Virtual Agent topic
description: Deploy an inactive topic or an updated topic to save it and make it available to users on Virtual Agent clients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Getting started with Assistant Designer Asset library, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Publish a Virtual Agent topic

Deploy an inactive topic or an updated topic to save it and make it available to users on Virtual Agent clients.

## Before you begin

**Note:** An updated Assistant Designer Asset library user interface is available when you install ServiceNow Otto in Virtual Agent. This content assumes that you can see the list view. If ServiceNow Otto in Virtual Agent is not installed, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

If you're using Natural Language Understanding \(NLU\) topic discovery, you can publish the model at the same time as the topic if the model meets publication criteria. Make sure that your model has passed through all phases of development and is ready to publish. If you haven’t refined, tested, and optimized your model, you may not be able to publish it in Assistant Designer Asset library. For more information, see [Model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/model-management-phases.md).

Role required: virtual\_agent\_admin or admin

## About this task

You can also publish topic blocks and custom controls to make them available for use in calling topics.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

    **Tip:** If you need to work with NLU/keyword topics, set the discovery type toggle switch to **NLU/keyword**.

3.  Select the topic, topic block, or custom control to publish or republish.

4.  In the topic header bar, select **Publish**.

    Selecting **Publish** when there are issues present opens a Validation Issues tab next to the property sheet, which counts up and details all issues needing correction. These details include a hyperlink for each incomplete item. If the issue is in a node, selecting the hyperlink opens the property sheet for that node. As each issue is resolved, the list on the shelf updates to show the remaining errors. Once there are no issues to resolve, the publishing dialog box opens.

    \[Omitted image "va-validation-issues-tab.png"\] Alt text: Assistant Designer Asset library canvas sidebar showing Validation Issues tab containing error message and hyperlink to node containing error.

    If you're using NLU topic discovery, the Choose what to publish dialog box appears. Select the available items to publish with the topic, such as the NLU model and language mappings, and then select **Publish**.

    **Note:** If the **Publish** option is unavailable, the model may need some work. For example, the model may not have enough intents or may need more utterances for some intents. Fix these issues before proceeding. Also, if a model language is unavailable, the language-specific model has never been published. Publish it from the NLU Workbench. For more information, see [Model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/model-management-phases.md).

    The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for four seconds, and can be closed by selecting the **X** in the message.

    For topics, the topic state is Active and the Published state changes to Published just now.

5.  Verify that your topics work as expected by opening them in a test conversation window in one of the following ways.

<table id="choicetable_uyk_3w1_scc"><tbody><tr><td id="d95262e224">

**Topic properties tab**

</td><td>

-   For NLU/keyword topics, select **Test**.
-   For LLM topics, select **Test** or open the drop-down menu and select **Preview in ServiceNow Otto panel**.


</td></tr><tr><td id="d95262e254">

**LLM home page**

</td><td>

Under the **Select assistant** drop-down menu, choose the assistant associated with your topic, then select **Test assistant**.

</td></tr><tr><td id="d95262e269">

**NLU/keyword home page**

</td><td>

Select **Test active topics**.

</td></tr></tbody>
</table>    **Note:** For more information about testing ServiceNow Otto LLM topics, see [Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/test-llm-topics.md). For NLU/keyword topics, enter keywords or NLU utterances that correspond to the topic intent. For the pre-built Virtual Agent topics, the bot returns a list of topics that match the entered keyword or utterance. See [Testing NLU/Keyword topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-designer-testing.md) for more information.


## Result

The topic blocks and custom controls are published and are available for use in calling topics.

**Note:** Active topics, including setup topics and small talk topics, can also be available for use after the topics are published. For more information, see [Control topic discovery and visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/manage-topics-task.md).

**Parent Topic:**[Getting started with Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

