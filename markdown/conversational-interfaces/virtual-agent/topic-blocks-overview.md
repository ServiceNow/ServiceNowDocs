---
title: Maximizing code reuse with topic blocks
description: Topic blocks are reusable components that you can create to run common tasks and conversational elements in Virtual Agent conversations. Topic blocks simplify the topic authoring and maintenance process by enabling you to reuse standard procedures or actions across conversation topics.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Virtual Agent, Designer, Topic block, reusable, pre-built, utility, code reuse]
breadcrumb: [Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Maximizing code reuse with topic blocks

Topic blocks are reusable components that you can create to run common tasks and conversational elements in Virtual Agent conversations. Topic blocks simplify the topic authoring and maintenance process by enabling you to reuse standard procedures or actions across conversation topics.

## How reusable topic blocks work

A topic block is basically a subflow that performs certain actions or conversational tasks in a topic. For example, you can build a topic block that creates or retrieves certain types of records. You create topic blocks with Virtual Agent Designer, similar to the way that you build conversation topics. With Virtual Agent Designer, you can do the following:

-   Set topic block properties.
-   Define the controls \(nodes\) used in the block.
-   Test or preview the block.
-   Publish the block to make it available for use in topics or other topic blocks.

Unlike topics, topic blocks are not discoverable by a large language model \(LLM\), Natural Language Understanding \(NLU\), or keywords. The topic block's functionality can only be accessed by a topic.

A conversation that uses \(consumes\) a topic block is referred to as the calling topic. A topic block can call another topic block, but it cannot call itself. You can "nest" topic blocks in this manner, even if the flow returns to the initial topic, as in this example:

![Topic Block 1 calls TB 2, which in turn calls TB 3. Topic Block 3 can then call Topic Block 1 again.](../images/nested-topic-blocks-chain.png "Chain of nested topic blocks")

**Note:** If Virtual Agent detects an infinite loop, the conversation ends.

The Virtual Agent platform and applications provide pre-built topic blocks for common tasks or subflows. You can use these pre-built topic blocks in your conversation topics "as is" in the appropriate application scope by duplicating them. You can then customize these pre-built topic blocks as needed. Some of the common topic blocks include the following.

<table id="table_dxm_wkw_jkb"><thead><tr><th>

Pre-built topic blocks

</th><th>

Application scope

</th></tr></thead><tbody><tr><td>

-   Transfer to Live Agent: Transfers a bot conversation to a live agent.
-   Survey: Presents a survey for collecting feedback for an agent.
-   Geolocation: Gathers information about the user's location.
-   Pause: Insert a pause \(in seconds\) in the conversation.
-   Deflection: Tracks deflection metrics for the Virtual Agent.

</td><td>

Global. Provided with the Glide Virtual Agent plugin \(com.glide.cs.chatbot\).

</td></tr><tr><td>

Contextual search: Uses a search phrase to return search results in a card format, such as knowledge articles and catalog items.

</td><td>

Common topic block used by the CSM, HR Service Delivery, and ITSM business applications. Provided with the Service Management Virtual Agent Topic Blocks plugin \(com.glideapp.cs.sm\_topic\_blocks\). This plugin is included with the [Virtual Agent conversation plugins](../reference/prebuilt-topics-ITSM.md) for these business applications.

</td></tr></tbody>
</table>**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

On the home page, you can use the filter icon ![Filter icon.](../images/filter-icon.png) to filter and view only the topic blocks.

![Filtered list of topic blocks.](../images/topic-block-list.png)

After you create and publish a topic block, the block is available for use as a Topic Block utility in Virtual Agent Designer. You can add the topic block to a calling topic or to another topic block. In the following example, the calling topic uses the Contextual Search topic block. When a topic calls the Contextual Search topic block, the conversation flow contained in the topic block executes.

![Contextual Search topic block.](../images/tb-overview-example.png)

## What to do next

Working with topic blocks involves the following steps:

1.  [Create a reusable topic block.](../task/create-topic-blocks.md)

    Build a conversation component that performs a common function that can be reused in Virtual Agent conversations.

2.  [Add a reusable topic block to a calling topic or topic block.](../task/add-topic-blocks-to-topic.md)

    To run a specific subflow, add a reusable topic block to a calling \(parent\) topic or topic block. Specify the inputs that are used in the topic block and review outputs that are returned from the topic block.

3.  [Maintain topic blocks and associated calling topics \(as needed\).](updating-topic-blocks.md)

    When you update a published topic block, Virtual Agent Designer performs certain checks. Displayed messages inform you of changes that you may want to make to calling topics that use the updated block.


