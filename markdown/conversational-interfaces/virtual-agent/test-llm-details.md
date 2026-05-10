---
title: Test details
description: The chat test window displays adjoining tabs that provide details about your topic as you test it.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 6
breadcrumb: [Testing LLM topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Test details

The chat test window displays adjoining tabs that provide details about your topic as you test it.

The following tabs are available when testing LLM topics:

-   **Analysis**: Results for topic discovery based on your input.
-   **Modify instructions**: List of all the instructions in the topic that are sent to the LLM. This tab is only available when testing a single topic.
-   **Variables**: List of all the variables used in the conversation, such as input and Live Agent variables.
-   **Edit variables**: Options for editing the variables used in the topic.
-   **Context**: Options for specifying the context \(using context variables\) in which a topic is run.
-   **Logs**: List of the processing performed.

The following tabs appear when you test their related topic types on the Virtual Agent Designer canvas:

-   The **Analyze test phrases**, **Modify instructions**, **Variables**, and **Logs** tabs appear for all LLM topic types.
-   The **Edit variables** tab appears for topic blocks and custom controls.
-   The **Context** tab appears for topics, setup topics, or small talk topics when you select **Include topic discovery**.

## Analysis tab

When you test LLM topics, results for topic discovery appear based on your input. When testing topics associated with a primary LLM assistant, only the primary assistant's promoted assets appear. When you input a test phrase, you can see a variety of search results when Genius Results are enabled including skill \(topic\) discovery, Knowledge Base \(KB\) articles, and catalog items. Under the skills search results, a **Matching** badge appears next to the skill discovered, while variables and values may also be listed \(such as the variable **@laptop\_make** and the value **macbook**\), depending on the topic. These Genius Results only appear if you’re testing a published topic and have selected the **Include topic discovery** option. If the **Include topic discovery** option appears inactive, publish the topic and select an LLM assistant on the Properties tab to work with topic discovery. A `Search indexing in progress` message might appear, but you can still test while the search indexing runs although topic discovery might not be updated. For more information about how Genius Results work, see [Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-ais.md).

Additionally, when testing active LLM assistant topics from the Topics page, you see skills results for Semantic search. Semantic search analyzes the meanings and context of your search terms and uses that information to find results with similar meanings. It improves search recall by interpreting natural language to more accurately reflect your search's intent. If semantic search is deactivated for topic discovery testing, those results are not displayed. For more information about semantic search, see [Semantic vector search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/semantic-search-ais.md).

![Analysis tab showing matching result for utterance Check ticket.](../images/va-test-phrases-llm-toast-message-matching-2.png)

## Modify instructions tab

If your topic contains any instructions that are sent to the LLM, they’re shown in the Nodes category. The Nodes category lists LLM user input nodes on the canvas, their field names, and their contents.

You can modify the content of any of the instructions to develop optimal instructions for the conversation. If a node has **Enforce user prompt** active, a blue check icon ![](../images/bluecheck.png) and a `User prompt enforced` message appears. Deactivate **Enforce user prompt** to modify the node's instructions.

If any of your user inputs have **Allow automatic slot filling** activated, the input's Detail Description becomes a static field. If **Allow automatic slot filling** is inactive, you can define detail description using a script or data pill picker. For more information, see the Allow automatic slot filling table entry in [Text user input control](va-text-input.md) or any other LLM user input controls.

Each instruction's status starts at `Original`. If you alter an instruction's content, its status changes to `Modified` and a revert icon ![](../images/revert-icon.png) appears next to it. The total number of instructions modified is listed at the bottom of the tab next to a **Save to topic** button. To test the modified instructions, select **Apply and restart**. To undo changes to an instruction, select the revert icon next to the instruction. Alternatively, undo all changes by selecting **Revert** that activates when you modify any instructions.

**Note:** If you select **Save to topic**, all changes are saved and all `Modified` messages reset to `Original`.

The following image shows the **Modify instructions** tab showing user information with LLM instruction guidelines link, and Nodes held within an Input collector, including a locked node with User prompt is enforced message.

![Modify instructions tab.](../images/va-prompt-discovery-llm-1.png)

The following image shows the **Modify instructions** tab with Modified instruction and Save to Topic updates. The **Revert** and **Apply and Restart** options activate when you make any changes.

![Modify instructions tab with Modified instruction and Save to Topic updates.](../images/va-prompt-discovery-llm-2.png)

## Variables tab

The **Variables** tab displays a list of all the variables used in the conversation and the associated values captured as the conversation progresses, so that you can follow along. A conversation can have these variable types:

-   Input variables
-   Script variables
-   Live Agent variables
-   Variables passed between a calling topic and topic block

The list is separated into sections by variable types. The following example shows the Input variables section. Notice that for the static list control, both the display label and value are captured for the selected choice.

![Variables tab that shows the input variables and values, next to a screen capture of the conversation flow.](../images/va-variables-llm.png)

The following example shows the Input variables section for the grouped list control. This variable information appears similar to the static list control, but the variables are separated by each group of the grouped choice.

![Variables tab with the node and Group name highlighted.](../images/llm-grouped-choice-variables.png)

## Edit Variables tab

When testing topic blocks and custom controls, you can edit the variables found in the nodes.

![Edit variables in the topic's nodes.](../images/va-edit-variables-llm.png)

## Context tab

The **Context** tab appears when you’re testing topics, setup topics, or small talk topics, to specify a different context for the chat. Choose a context variable from the list. The variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. For example, you could select **portal** from the list of variables and enter the portal name **IT Express**. The **Context** tab is unavailable when creating test cases.

For more information about defining context variables, see [Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md). For more information about live agent variables that are included with Virtual Agent, see [Live agent chat context variables](live-agent-chat-context-vars.md).

![Context tab with the context portal value of service portal.](../images/va-context-llm.png)

## Logs tab

The **Logs** tab displays a running log of server events, user entries, and Virtual Agent responses in the chat. You can review the logs to look for any important data about the chat including potential errors.

![Logs tab displaying list of events in Virtual Agent conversation.](../images/va-llm-test-window-logs.png)

**Parent Topic:**[Testing LLM topics](test-llm-topics.md)

