---
title: Duplicating a Virtual Agent topic
description: Create a topic or topic block by copying an existing Virtual Agent topic or topic block and customize it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/duplicate-virtual-agent-topic.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Virtual Agent, topic, duplicate, duplication, copy, NLU, LLM]
breadcrumb: [Build conversations, Virtual Agent, Conversational Interfaces]
---

# Duplicating a Virtual Agent topic

Create a topic or topic block by copying an existing Virtual Agent topic or topic block and customize it.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Consider duplicating topics in the following scenarios:

-   When you want to use an existing topic, such as a prebuilt topic or topic block, as the basis for a new topic or topic block.
-   When you want to modify an active topic while preserving the original topic for reference purposes or as a backup.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Open the topic you want to duplicate.

4.  In the topic header bar, select the more actions on topics icon \[Omitted image "kebab-menu.png"\] Alt text:, then select **Duplicate**.

    1.  In the Duplicate window, enter the new name for the item.

    2.  Select **Save**.

5.  Update the properties on the **Properties** tab and on the **Flow** tab, change the conversation flow design as needed.

    **Note:** Keep in mind the goal or purpose of your new topic as you set the properties and update the flow. For example, you might need to select one or more LLM assistants.

<table id="table_ahw_hqt_hmb"><thead><tr><th>

If you're duplicating

</th><th>

See this section

</th></tr></thead><tbody><tr><td>

Topics

</td><td>

See [Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md) for a description of the topic properties that you can change and how to add or change the nodes in the flow.

</td></tr><tr><td>

Topic blocks

</td><td>

See [Create a reusable topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-topic-blocks.md) for a description of the topic block properties that you set and the input and output parameters that you define for the block.

</td></tr></tbody>
</table>6.  As you update your design, use the **Test** option to run your design in a chat test window, then fine-tune your design flow accordingly.

    For more information, see [Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/test-llm-topics.md).


## What to do next

If you’ve completed the topic or topic block, [publish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md) it to deploy it to your Virtual Agent clients.

**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

