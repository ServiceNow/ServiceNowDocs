---
title: Maximizing code reuse with topic blocks
description: Topic blocks are reusable components that you can create to run common tasks and conversational elements in Virtual Agent conversations. Topic blocks simplify the topic authoring and maintenance process by enabling you to reuse standard procedures or actions across conversation topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/topic-blocks-overview.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Virtual Agent, Designer, Topic block, reusable, prebuilt, utility, code reuse]
breadcrumb: [Other Virtual Agent features, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Maximizing code reuse with topic blocks

Topic blocks are reusable components that you can create to run common tasks and conversational elements in Virtual Agent conversations. Topic blocks simplify the topic authoring and maintenance process by enabling you to reuse standard procedures or actions across conversation topics.

## How reusable topic blocks work

A topic block is basically a subflow that performs certain actions or conversational tasks in a topic. For example, you can build a topic block that creates or retrieves certain types of records. You create topic blocks with Assistant Designer, similar to the way that you build conversation topics. In the Assistant Designer Asset library, you can do the following:

-   Set topic block properties.
-   Define the controls \(nodes\) used in the block.
-   Test or preview the block.
-   Publish the block to make it available for use in topics or other topic blocks.

Unlike topics, topic blocks are not discoverable by a large language model \(LLM\). The topic block's functionality can only be accessed by a topic.

A conversation that uses \(consumes\) a topic block is referred to as the calling topic. A topic block can call another topic block, but it cannot call itself. You can "nest" topic blocks in this manner, even if the flow returns to the initial topic, as in this example:

\[Omitted image "nested-topic-blocks-chain.png"\] Alt text: Topic Block 1 calls TB 2, which in turn calls TB 3. Topic Block 3 can then call Topic Block 1 again.

**Note:** If Virtual Agent detects an infinite loop, the conversation ends.

The Virtual Agent platform and applications provide prebuilt topic blocks for common tasks or subflows. You can use these prebuilt topic blocks in your conversation topics "as is" in the appropriate application scope by duplicating them. You can then customize these prebuilt topic blocks as needed. Some of the common topic blocks include the following.

<table id="table_dxm_wkw_jkb"><thead><tr><th>

Prebuilt topic blocks

</th><th>

Application scope

</th></tr></thead><tbody><tr><td>

-   Live Agent: Transfers a bot conversation to a live agent.
-   Survey-LLM: Presents a survey for collecting feedback for an agent.
-   AIA Interrupt Handler: Stop AI agent execution.

</td><td>

Global. Provided with the Glide Virtual Agent plugin \(com.glide.cs.chatbot\).

</td></tr></tbody>
</table>On the home page, you can use the filter icon \[Omitted image "filter-icon.png"\] Alt text: Filter icon. to filter and view only the topic blocks.

\[Omitted image "topic-block-list.png"\] Alt text: Filtered list of topic blocks.

After you create and publish a topic block, the block is available for use as a Topic Block utility in the Asset library. You can add the topic block to a calling topic or to another topic block. In the following example, the calling topic uses the Contextual Search topic block. When a topic calls the Contextual Search topic block, the conversation flow contained in the topic block executes.

\[Omitted image "tb-overview-example.png"\] Alt text: Contextual Search topic block.

## What to do next

Working with topic blocks involves the following steps:

1.  [Create a reusable topic block.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-topic-blocks.md)

    Build a conversation component that performs a common function that can be reused in Virtual Agent conversations.

2.  [Add a reusable topic block to a calling topic or topic block.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/add-topic-blocks-to-topic.md)

    To run a specific subflow, add a reusable topic block to a calling \(parent\) topic or topic block. Specify the inputs that are used in the topic block and review outputs that are returned from the topic block.

3.  [Maintain topic blocks and associated calling topics \(as needed\).](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/updating-topic-blocks.md)

    When you update a published topic block, Assistant Designer performs certain checks. Displayed messages inform you of changes that you may want to make to calling topics that use the updated block.


