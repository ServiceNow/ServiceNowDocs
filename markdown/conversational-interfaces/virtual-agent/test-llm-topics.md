---
title: Testing LLM topics
description: Preview, test, and debug topics that use large language models \(LLMs\) in the Virtual Agent Designer chat window.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-02-26"
reading_time_minutes: 11
keywords: [LLM, Topic, Testing, Virtual Agent, Large Language Model]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Testing LLM topics

Preview, test, and debug topics that use large language models \(LLMs\) in the Virtual Agent Designer chat window.

You can test your topic's functions by running your conversation in a chat test window as you work. The web \(Service Portal\) chat client is the default test window.

Large language model \(LLM\) topics are faster and easier to test compared to Natural Language Understanding \(NLU\) topics. For example, you don't need to retest your topic after updating utterances and retraining models as with NLU topics.

If you're using the [Virtual Agent integrations with third-party messaging apps](../concept/va-integration-messaging-apps.md), elements in your conversation might appear differently in third-party messaging applications. Test your conversations in any third-party applications where you want to deploy Virtual Agent.

**Note:** If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.

## Testing your LLM topic in the chat test window

**Note:** An updated Virtual Agent Designer user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not enabled, you will see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

![You can find LLM testing options on the Virtual Agent Designer canvas and the home page.](../images/va-test-ui-options-llm-2.png "LLM test options")

Test LLM topics on the Virtual Agent Designer canvas by working with the **Test** options on the topic header bar. When testing from a single topic, the **Include topic discovery** option must be selected to work with the assistants. If the topic is associated with multiple LLM assistants, use the Assistant drop-down list to select which assistant you want to test. For more information about LLM assistants, see [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md).

**Note:** If your topic is missing any necessary information, an incomplete badge appears in the corner of the flow diagram pane. A yellow or red warning badge also appears next to each node. The incomplete badge lists the total number of issues, while the local warning badges show how many issues are found in each node. If you select **Test** when there are issues, an Issues window opens with the number of issues present along with the details of each issue. These details include a full description and a hyperlink to each incomplete item.

Alternatively, you can test active \(published\) LLM topics on the Topics page. Use the **LLM Assistant** filter to restrict your topics to only topics associated with that assistant, and then select **Test active topics**. If you don't use the **LLM Assistant** filter, select **Test LLM assistant topics** from the Test active topics drop-down list. When using the **Test active topics** option or sub-options from the Topics page, topic discovery is enabled, so it's not listed as an option. When testing from the Topics page, the Assistant drop-down list appears in the chat test window. You must have previously established at least the default Now Assist in Virtual Agent assistant to see the Assistant drop-down list. When a topic is associated with just one LLM assistant, the Assistant drop-down list defaults to that assistant name. If you have multiple assistants, select which assistant you want to work with using the Assistant drop-down list. For more information about creating multiple LLM assistants, see [Manage LLM virtual agents on the Assistants screen](../task/manage-llm-va.md).

The chat test window opens in the Now Assist in Virtual Agent chat widget. The Assistant drop-down list and **Include topic discovery** option might be displayed depending on where you originated the test from and if you have established any LLM assistants.

You can provide feedback to each utterance made by the LLM by selecting from the like thumbs-up icon ![Thumbs up icon](../images/llm-thumbs-up-like.png) or dislike thumbs-down icon ![Thumbs down icon](../images/llm-thumbs-down-dislike.png) options that appear when you hover over an utterance. All LLM user inputs aside from the Input Collector have these feedback options.

![LLM response asking the user "Which color do you prefer: red or green?" followed by "red" or "green" choices. Like and dislike feedback options are shown in the message's corner.](../images/llm-test-thumbs-up-down.png "LLM response feedback options")

The chat test window also displays adjoining tabs that provide details about your topic as you test it. The following tabs are available when testing LLM topics:

-   **Analyze test phrases** - Results for topic discovery based on your input.
-   **Modify instructions** - List of all the instrucions in the topic that are sent to the LLM. This tab is only available when testing a single topic.
-   **Variables** - List of all the variables used in the conversation, such as input and Live Agent variables.
-   **Edit variables** - Options for editing the variables used in this topic.
-   **Context** - Options for specifying the context \(using context variables\) in which a topic is run.
-   **Logs** - List of the processing performed.

![Different tabs appear based on the type of LLM topic that you are testing.](../images/llm-testing-windows.png "Example test window and tabs")

The following tabs appear when you test their related topic types on the Virtual Agent Designer canvas:

-   The **Analyze test phrases**, **Modify instructions**, **Variables**, and **Logs** tabs appear for all LLM topic types.
-   The **Edit variables** tab appears for topic blocks and custom controls.
-   The **Context** tab appears for topics, setup topics, or small talk topics when you select **Include topic discovery**.

If you run tests from the Topics page, the test window shows only the **Analyze test phrases**, **Variables**, **Context** \(available by default, with no **Include topic discovery** option\), and **Logs** tabs.

## Analyze test phrases tab

When you test LLM topics, results for topic discovery appear based on your input. When testing topics associated with a primary LLM assistant, only the primary assistant's promoted topics appear. When you input a test phrase, you can see a variety of search results when Genius Results are enabled including skill \(topic\) discovery, Knowledge Base \(KB\) articles, and catalog items. Under the skills search results,a **Matching** badge appears next to the skill discovered, while variables and values may also be listed \(such as the variable **@laptop\_make** and the value **macbook**\), depending on the topic. These Genius Results only appear if you’re testing a published topic and have selected the **Include topic discovery** option. If the **Include topic discovery** option appears inactive, publish the topic and select an LLM assistant on the Properties tab to work with topic discovery. A `Search indexing in progress` message might appear, but you can still test while the search indexing runs although topic discovery might not be updated. For more information about how Genius Results work, see [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Additionally, when testing active LLM assistant topics from the Topics page, you see skills results for Semantic search. Semantic search analyzes the meanings and context of your search terms and uses that information to find results with similar meanings. It improves search recall by interpreting natural language to more accurately reflect your search's intent. If semantic search is deactivated for topic discovery testing, those results are not displayed. For more information about semantic search, see [Semantic vector search in AI Search](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

![Analyze test phrases tab, showing test phrase results for Skill Discovery, with Matching result, and Input and Output Skills categories.](../images/va-test-phrases-llm-toast-message-matching.png "Example Analyze test phrases tab for LLM topics")

## Modify instructions tab

If your topic contains any instructions that are sent to the LLM, they’re shown in the Nodes category. The Nodes category lists LLM user input nodes on the canvas, their field names, and their contents.

You can modify the content of any of the instructions to develop optimal instructions for the conversation. If a node has **Enforce user prompt** active, a blue check icon ![VAD Advanced options checkmark](../images/bluecheck.png) and a `User prompt enforced` message appears. Deactivate **Enforce user prompt** to modify the node's instructions.

If any of your user inputs have **Allow automatic slot filling** activated, the input's Detail Description becomes a static field. If **Allow automatic slot filling** is inactive, you can define detail description using a script or data pill picker. For more information, see the Allow automatic slot filling table entry in [Text user input control](va-text-input.md) or any other LLM user input controls.

Each instruction's status starts at `Original`. If you alter an instruction's content, its status changes to `Modified` and a revert icon![Revert icon](../images/revert-icon.png) appears next to it. The total number of instructions modified is listed at the bottom of the tab next to a **Save to topic** button. To test the modified instructions, select **Apply and restart**. To undo changes to an instruction, select the revert icon next to the instruction. Alternatively, undo all changes by selecting **Revert** that activates when you modify any instructions.

**Note:** If you select **Save to topic**, all changes are saved and all `Modified` messages reset to `Original`.

![Modify instructions tab showing user information with LLM instruction guidelines link, and Nodes held within an Input collector, including a locked node with User prompt is enforced message.](../images/va-prompt-discovery-llm-1.png "Example Modify instructions tab")

![Modify instructions tab with Modified instruction and Save to Topic updates. The Revert and Apply and Restart options activate when you make any changes.](../images/va-prompt-discovery-llm-2.png "Example Modify instructions tab with a modification")

If instructions in a node include potentially offensive content, a warning badge appears on the node. A yellow warning icon ![Yellow warning icon](../images/yellow-warning-icon.png) also appears next to the node name. Selecting **Apply and restart** inputs those instructions and removes the badge and icon, and the `Modified` status reverts to `Original`.

![Modify instructions tab showing offensive content warning badge, icons, and hover message. Selecting Apply and restart applies the instructions and removes the warnings.](../images/va-prompt-discovery-llm-3.png "Example Modify instructions tab with potentially offensive content warnings")

## Variables tab

The **Variables** tab displays a list of all the variables used in the conversation and the associated values captured as the conversation progresses, so that you can follow along. A conversation can have these variable types:

-   Input variables
-   Script variables
-   Live Agent variables
-   Variables passed between a calling topic and topic block

The list is separated into sections by variable types. The following example shows the Input variables section. Notice that for the static list control, both the display label and value are captured for the selected choice.

![Variables tab that shows the input variables and values, next to a screen capture of the conversation flow.](../images/va-variables-llm.png "Example list of input variables")

The following example shows the Input variables section for the grouped list control. This variable information appears similar to the static list control, but the variables are separated by each group of the grouped choice.

![Variables tab separated by group, with the node and Group name highlighted.](../images/llm-grouped-choice-variables.png "Example list of grouped choice variables")

## Edit Variables tab

When testing topic blocks and custom controls, you can edit the variables found in the nodes.

![Edit variables in the topic's nodes.](../images/va-edit-variables-llm.png)

## Context tab

The **Context** tab appears when you’re testing topics, setup topics, or small talk topics, to specify a different context for the chat. Choose a context variable from the list. The variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. For example, you could select **portal** from the list of variables and enter the portal name **IT Express**. The **Context** tab is unavailable when creating test cases.

For more information about defining context variables, see [Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md). For more information about live agent variables that are included with Virtual Agent, see [Live agent chat context variables](live-agent-chat-context-vars.md).

![Context tab with the context portal value of service portal.](../images/va-context-llm.png "Example Context tab")

## Next steps

When you're done testing your topic, close the test chat window. If necessary, use the test information to adjust your topic to perform more accurately. For example, the results on the **Analyze test phrases** tab may return low scores or `Unsure` or `Unknown` confidence ratings. Improve scores by updating the topic description or instructions in the LLM user input nodes.

**Parent Topic:**[Getting started with Virtual Agent Designer](conversation-designer-virtual-agent.md)

