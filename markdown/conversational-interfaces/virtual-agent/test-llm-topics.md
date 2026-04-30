---
title: Testing LLM topics
description: Preview, test, and debug topics that use large language models \(LLMs\) in the Virtual Agent Designer chat window.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-08-06"
reading_time_minutes: 11
keywords: [LLM, Topic, Testing, Virtual Agent, Large Language Model]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Testing LLM topics

Preview, test, and debug topics that use large language models \(LLMs\) in the Virtual Agent Designer chat window.

You can test your topic's functions by running your conversation in a chat test window as you work. The web \(Service Portal\) chat client is the default test window.

Large language model \(LLM\) topics are faster and easier to test compared to Natural Language Understanding \(NLU\) topics. For example, you don't need to retest your topic after updating utterances and retraining models as with NLU topics.

If you're using the [Virtual Agent integrations with third-party messaging apps](../concept/va-integration-messaging-apps.md), elements in your conversation might appear differently in third-party messaging applications. Test your conversations in any third-party applications where you want to deploy Virtual Agent.

**Note:** If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.

## Testing your LLM topic in the chat test window

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

You can find LLM testing options on the canvas and the topics home pageAssistant Designer Asset library. The chat test window opens in the Now Assist in Virtual Agent chat widget. The Assistant drop-down list and **Include topic discovery** option might be displayed depending on where you originated the test from and if you have established any LLM assistants.

![Test options.](../images/va-test-ui-options-llm-4.png)

Test LLM topics on the Virtual Agent Designer canvas by working with the **Test** option on the topic header bar. When testing from a single topic, the **Include topic discovery** option must be selected to work with the assistants. If the topic is associated with multiple LLM assistants, use the Assistant drop-down list to select which assistant you want to test. For more information about LLM assistants, see [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md).

**Note:** The **Test in enhanced chat** option is available only from the Asset library list view. The **Test** button in the topic canvas adds options in a drop-down box if you configure Microsoft Teams or Slack for Virtual Agent.

![Add assistants in the Properties tab, followed by the Test skill discovery check box in the topic testing window, to select an assistant in the drop-down window.](../images/va-llm-test-window-assistants.png) ![Add assistants in the Properties tab, followed by the Test skill discovery check box in the topic testing window, to select an assistant in the drop-down window.](../images/va-llm-test-window-assistants-2.png)

![Virtual Agent Designer Now Assist Fallback screen.](../images/incl-topic-disc-2.png)

**Note:** If your topic is missing any necessary information, an incomplete badge appears in the corner of the flow diagram pane. A warning badge also appears next to each node. The incomplete badge lists the total number of issues, while the local warning badges show how many issues are found in each node. If you select **Test** when there are issues, an Issues window opens with the number of issues present along with the details of each issue. These details include a full description and a hyperlink to each incomplete item.

Alternatively, you can test active \(published\) LLM topics in the Asset library. Use the **LLM Assistant** filter to restrict your topics to only topics associated with that assistant, and then select **Test active topics**. If you don't use the **LLM Assistant** filter, select **Test LLM assistant topics** from the Test active topics drop-down list. When using the **Test active topics** option or sub-options from the Topics page, topic discovery is enabled, so it's not listed as an option. When testing from the Topics page, the Assistant drop-down list appears in the chat test window. You must have previously established at least the default Now Assist in Virtual Agent assistant to see the Assistant drop-down list. When a topic is associated with just one LLM assistant, the Assistant drop-down list defaults to that assistant name. If you have multiple assistants, select which assistant you want to work with using the Assistant drop-down list. For more information about creating multiple LLM assistants, see [Manage LLM virtual agents on the Assistants screen](../task/manage-llm-va.md).

You can provide feedback to each utterance made by the LLM by selecting from the like thumbs-up icon ![](../images/llm-thumbs-up-like.png) or dislike thumbs-down icon ![](../images/llm-thumbs-down-dislike.png) options that appear when you hover over an utterance. All LLM user inputs except the Input Collector have these feedback options.

![LLM feedback options.](../images/llm-test-thumbs-up-down.png)

The chat test window also displays adjoining tabs that provide details about your topic as you test it. The following tabs are available when testing LLM topics:

-   **Analyze test phrases** - Results for topic discovery based on your input.
-   **Modify instructions** - List of all the instructions in the topic that are sent to the LLM. This tab is only available when testing a single topic.
-   **Variables** - List of all the variables used in the conversation, such as input and Live Agent variables.
-   **Edit variables** - Options for editing the variables used in this topic.
-   **Context** - Options for specifying the context \(using context variables\) in which a topic is run.
-   **Logs** - List of the processing performed.

![Different tabs appear based on the type of LLM topic that you are testing.](../images/llm-testing-windows-2.png "Example test window and tabs")

The following tabs appear when you test their related topic types on the Virtual Agent Designer canvas:

-   The **Analyze test phrases**, **Modify instructions**, **Variables**, and **Logs** tabs appear for all LLM topic types.
-   The **Edit variables** tab appears for topic blocks and custom controls.
-   The **Context** tab appears for topics, setup topics, or small talk topics when you select **Include topic discovery**.

If you run tests from the Topics page, the test window shows only the **Analyze test phrases**, **Variables**, **Context** \(available by default, with no **Include topic discovery** option\), and **Logs** tabs.

## Analyze test phrases tab

When you test LLM topics, results for topic discovery appear based on your input. When testing topics associated with a primary LLM assistant, only the primary assistant's promoted assets appear. When you input a test phrase, you can see a variety of search results when Genius Results are enabled including skill \(topic\) discovery, Knowledge Base \(KB\) articles, and catalog items. Under the skills search results,a **Matching** badge appears next to the skill discovered, whilevariables and values may also be listed \(such as the variable **@laptop\_make** and the value **macbook**\), depending on the topic. These Genius Results only appear if you’re testing a published topic and have selected the **Include topic discovery** option. If the **Include topic discovery** option appears inactive, publish the topic and select an LLM assistant on the Properties tab to work with topic discovery. A `Search indexing in progress` message might appear, but you can still test while the search indexing runs although topic discovery might not be updated. For more information about how Genius Results work, see [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Additionally, when testing active LLM assistant topics from the Topics page, you see skills results for Semantic search. Semantic search analyzes the meanings and context of your search terms and uses that information to find results with similar meanings. It improves search recall by interpreting natural language to more accurately reflect your search's intent. If semantic search is deactivated for topic discovery testing, those results are not displayed. For more information about semantic search, see [Semantic vector search in AI Search](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

![Analysis tab showing matching result for utterance Check ticket.](../images/va-test-phrases-llm-toast-message-matching-2.png)

## Modify instructions tab

If your topic contains any instructions that are sent to the LLM, they’re shown in the Nodes category. The Nodes category lists LLM user input nodes on the canvas, their field names, and their contents.

You can modify the content of any of the instructions to develop optimal instructions for the conversation. If a node has **Enforce user prompt** active, a blue check icon ![](../images/bluecheck.png) and a `User prompt enforced` message appears. Deactivate **Enforce user prompt** to modify the node's instructions.

If any of your user inputs have **Allow automatic slot filling** activated, the input's Detail Description becomes a static field. If **Allow automatic slot filling** is inactive, you can define detail description using a script or data pill picker. For more information, see the Allow automatic slot filling table entry in [Text user input control](va-text-input.md) or any other LLM user input controls.

Each instruction's status starts at `Original`. If you alter an instruction's content, its status changes to `Modified` and a revert icon ![](../images/revert-icon.png) appears next to it. The total number of instructions modified is listed at the bottom of the tab next to a **Save to topic** button. To test the modified instructions, select **Apply and restart**. To undo changes to an instruction, select the revert icon next to the instruction. Alternatively, undo all changes by selecting **Revert** that activates when you modify any instructions.

**Note:** If you select **Save to topic**, all changes are saved and all `Modified` messages reset to `Original`.

The following image shows the **Modify instructions** tab showing user information with LLM instruction guidelines link, and Nodes held within an Input collector, including a locked node with User prompt is enforced message.

![Modify instructions tab.](../images/va-prompt-discovery-llm-1-2.png)

The following image shows the **Modify instructions** tab with Modified instruction and Save to Topic updates. The **Revert** and **Apply and Restart** options activate when you make any changes.

![Modify instructions tab with Modified instruction and Save to Topic updates.](../images/va-prompt-discovery-llm-2-2.png)

## Variables tab

The **Variables** tab displays a list of all the variables used in the conversation and the associated values captured as the conversation progresses, so that you can follow along. A conversation can have these variable types:

-   Input variables
-   Script variables
-   Live Agent variables
-   Variables passed between a calling topic and topic block

The list is separated into sections by variable types. The following example shows the Input variables section. Notice that for the static list control, both the display label and value are captured for the selected choice.

![Variables tab that shows the input variables and values, next to a screen capture of the conversation flow.](../images/va-variables-llm-2.png)

The following example shows the Input variables section for the grouped list control. This variable information appears similar to the static list control, but the variables are separated by each group of the grouped choice.

![Variables tab separated by group, with the node and Group name highlighted.](../images/llm-grouped-choice-variables-2.png)

## Edit Variables tab

When testing topic blocks and custom controls, you can edit the variables found in the nodes.

![Edit variables in the topic's nodes.](../images/va-edit-variables-llm-2.png)

## Context tab

The **Context** tab appears when you’re testing topics, setup topics, or small talk topics, to specify a different context for the chat. Choose a context variable from the list. The variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. For example, you could select **portal** from the list of variables and enter the portal name **IT Express**. The **Context** tab is unavailable when creating test cases.

For more information about defining context variables, see [Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md). For more information about live agent variables that are included with Virtual Agent, see [Live agent chat context variables](live-agent-chat-context-vars.md).

![Context tab with the context portal value of service portal.](../images/va-context-llm-2.png)

## Logs tab

The **Logs** tab displays a running log of server events, user entries, and Virtual Agent responses in the chat. You can review the logs to look for any important data about the chat including potential errors.

![Logs tab displaying list of events in Virtual Agent conversation.](../images/va-llm-test-window-logs.png)

## Next steps

When you're done testing your topic, close the test chat window. If necessary, use the test information to adjust your topic to perform more accurately. For example, the results on the **Analyze test phrases** tab may return low scores or `Unsure` or `Unknown` confidence ratings. Improve scores by updating the topic description or instructions in the LLM user input nodes.

-   **[Testing Now Assist enhanced chat conversations](../concept/testing-enhanced-chat-conversations.md)**  
Test conversational assets with assistants in enhanced chat.

**Parent Topic:**[Getting started with Virtual Agent Designer](conversation-designer-virtual-agent.md)

