---
title: Testing NLU/Keyword topics
description: Use the chat test window to preview, test, and debug Natural Language Understanding \(NLU\)/Keyword topics.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
keywords: [Virtual Agent, NLU/Keyword, Natural Language Understanding, topic, testing, chat widget, Service Portal]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Testing NLU/Keyword topics

Use the chat test window to preview, test, and debug Natural Language Understanding \(NLU\)/Keyword topics.

As you work on a topic in Virtual Agent Designer, you can run your conversation in a chat test window. The default test window is the web \(Service Portal\) chat client.

If you're using the [Virtual Agent integrations with third-party messaging apps](../concept/va-integration-messaging-apps.md), elements in your conversation might appear differently in third-party messaging applications. Test your conversations in any third-party applications where you want to deploy Virtual Agent.

If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.

## Testing your NLU/Keyword topic in the chat test window

![NLU/Keyword testing options are available on both the Virtual Agent Designer canvas and the Assistant Designer Asset library.](../images/va-test-ui-options-nlu-2a.png "Example NLU/Keyword test options")

To run your topic in the chat test window, select the **Test** option in the topic header bar. Alternatively, you can test active \(published\) topics by selecting **Test active topics** while viewing NLU topics on the home page.

**Note:** If your topic is missing any necessary information, an incomplete badge appears in the corner of the flow diagram pane. A yellow or red warning badge also appears next to each node. The incomplete badge lists the total number of issues, while the local warning badges show how many are found in each node. Selecting **Test** when there are issues present opens a Validation Issues tab on the sidebar, which counts up and details all the issues needing correction. These details include a full description and a hyperlink to each incomplete node.

The chat test window opens in the chat widget and displays adjoining tabs that provide details about your topic as you test it. You can use these tabs:

-   **Analyze Test Phrases** - The results for intent matching and entity recognition appear based on what you entered in the conversation.
-   **Variables** - List of all the variables used in the conversation, such as input and live agent variables.
-   **Context** - Options for specifying the context \(using context variables\) in which a topic is run.
-   **Logs** - A list of the processing performed.

![Conversation test tabs shown in the chat test window, with Analyze test phrases, Variables, Context, and Logs options highlighted.](../images/va-test-tabs-2.png "Example Natural Language Understanding (NLU) chat test window and test tabs")

By default, the **Include Topic Discovery** option is enabled. This option automatically performs topic discovery and generates prediction results for NLU topics using test phrases that you enter in the test window. The conversation begins with the Virtual Agent greeting and the button for the menu of available topics.

If you're using the **Test Active Topics** option or sub-options from the home page, topic discovery is enabled, so it's not listed as an option. Testing active topics behaves the same as testing from a topic except that test cases can't be created.

## Analyze test phrases tab

For NLU enabled topics, the **Analyze test phrases** tab provides an analysis of the possible intents that match the test phrase \(utterance\) that you entered in the chat test window. The tab lists the prediction results, which include matched intents and their prediction scores, along with any entity recognition and slot-filling results. The top match is listed first. The predicted intents depend on the prediction confidence threshold set in the NLU service.

![Analyze test phrases tab, showing test phrase results for multiple intent matches.](../images/va-test-phrases-multiple-results-2.png "Example Analyze test phrases tab for NLU/Keyword topics")

If an utterance doesn't match a current intent, you can add or change utterances in Virtual Agent Designer. For more information, see [Modify NLU utterances and entities for a Virtual Agent topic](../task/modify-nlu-utterances-va-topic.md).

Make changes, train the model again, and then retest until you're satisfied with the results. When the topic is ready, you can publish both the topic and the model from Virtual Agent Designer.

## Variables tab

The **Variables** tab displays a list of all the variables used in the conversation and the associated values captured as the conversation progresses, so that you can follow along. A conversation can have these variable types:

-   Input variables
-   Script variables
-   Live agent variables
-   Variables passed between a calling topic and topic block
-   "Nodeless" NLU entities declared as a slot-filled variable for the topic

The list is separated into sections by type of variable. The following example shows the Input variables section. Notice that for the static list control, both the display label and value are captured for the selected choice.

![Variables tab that shows the input variables and values, next to a screen capture of the conversation flow.](../images/va-test-variables-tab-2.png "Example list of input variables")

The following example shows the Input variables section for the grouped list control. This variable information appears similar to the static list control, but the variables are separated by each group of the grouped choice.

![Variables tab separated by group, with the node and Group name highlighted.](../images/vad-grouped-choice-variables-2.png "Example list of grouped choice variables")

## Context tab

Use the **Context** tab to specify a different context for the chat. Choose a context variable from the list. These variables contain contextual information that can be used to determine topic intent or control how chats are routed to live agents. For example, you could select **portal** from the list of variables and enter the portal name **IT Express**. The **Context** tab is unavailable when creating test cases.

For more information about defining context variables, see [Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md). For more information about live agent variables that are included with Virtual Agent, see [Live agent chat context variables](live-agent-chat-context-vars.md).

![Context tab with the context portal value of IT Express.](../images/va-cce-it-express-2.png "Example Context tab")

## Logs tab

The **Logs** tab displays the processing and error messages that are recorded while running your conversation. If you're using scripts in Virtual Agent Designer, use `gs.log`, `gs.print`, and `gs.warn` statements in your scripts to output information in this log.

![Logs tab that contains processing information about the topic.](../images/va-conv-preview-logs2a.png "Example Logs tab")

## Next steps

When you're done testing your topic, close the test chat window. If needed, you can use the test information to fine-tune your conversation. For example, if the results on the **Analyze test phrases** tab return multiple possible matches for your utterance, you could update the utterances for your intent and NLU model on the **NLU Intent** tab for your topic.

-   **[Train and test your NLU model in Virtual Agent Designer](../task/train-test-publish-nlu-model-vad.md)**  
Use the **NLU Intent** tab to train and try a Natural Language Understanding \(NLU\) model that is mapped to a topic without leaving Virtual Agent Designer.
-   **[Automated testing for Virtual Agent topics that use NLU topic discovery](../concept/automated-testing-va-topics.md)**  
Automated testing for your Virtual Agent topic flows uses the ServiceNow Automated Test Framework product through Assistant Designer. You can create and run automated tests through the Automated Test Framework to confirm that your topic flow works after making a change.

**Parent Topic:**[Getting started with Virtual Agent Designer](conversation-designer-virtual-agent.md)

