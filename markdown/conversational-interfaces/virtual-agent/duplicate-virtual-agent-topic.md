---
title: Duplicate a Virtual Agent topic
description: Create a new topic or topic block by copying an existing Virtual Agent topic or topic block and customize it.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Virtual Agent, topic, duplicate, duplication, copy, NLU, LLM]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Duplicate a Virtual Agent topic

Create a new topic or topic block by copying an existing Virtual Agent topic or topic block and customize it.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Consider duplicating topics in the following scenarios:

-   When you want to use an existing topic, such as a prebuilt topic or topic block, as the basis for a new topic or topic block.
-   When you want to modify an active topic while preserving the original topic for reference purposes or as a backup.
-   When you want to convert a Natural Language Understanding \(NLU\) topic to a large language model \(LLM\) topic.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and in the Asset library, select the topic you want to duplicate.

2.  In the topic header bar, select the more actions on topics icon ![](../images/kebab-menu.png), then select **Duplicate**.

    1.  In the Duplicate window, enter the new name for the item.

    2.  Select **Save**.

3.  Update the properties on the **Properties** tab and on the **Flow** tab, change the conversation flow design as needed.

    **Note:** Keep in mind the goal or purpose of your new topic as you set the properties and update the flow. For example, if you're using keyword-based topics, you might need to change certain keywords based on the purpose of your new topic. For LLM topics, you might need to select one or more LLM assistants. For Natural Language Understanding \(NLU\)-enabled topics, you might need to change the NLU model and intent associated with the topic.

<table id="table_ahw_hqt_hmb"><thead><tr><th>

If you're duplicating

</th><th>

See this section

</th></tr></thead><tbody><tr><td>

Topics

</td><td>

See [Create a Virtual Agent topic](create-virtual-agent-topic.md) for a description of the topic properties that you can change and how to add or change the nodes in the flow.

</td></tr><tr><td>

Topic blocks

</td><td>

See [Create a reusable topic block](create-topic-blocks.md) for a description of the topic block properties that you set and the input and output parameters that you define for the block.

</td></tr></tbody>
</table>4.  As you update your design, use the **Test** option to run your design in a chat test window, then fine-tune your design flow accordingly.

    For details on test features of LLM topics, see [Testing LLM topics](../reference/test-llm-topics.md).

    For details on test features regarding NLU topics, see [Testing NLU/Keyword topics](../reference/va-designer-testing.md).


## What to do next

If you’ve completed the topic or topic block, [publish](publish-virtual-agent-topic.md) it to deploy it to your Virtual Agent clients.

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

