---
title: Create a Virtual Agent topic
description: Use Virtual Agent Designer to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-09-26"
reading_time_minutes: 10
keywords: [Create, Virtual Agent, topic, topic, designer, conversations, LLM, NLU, Large language model, Natural Language Understanding]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent topic

Use Virtual Agent Designer to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.

## Before you begin

Virtual Agent Designer LLM topic authoring video 

Do the following:

-   Review [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).
-   Configure Virtual Agent settings. For example, if you're creating large language model \(LLM\) topics, turn on Now Assist in Virtual Agent. For more information, see [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md). If you're creating Natural Language Understanding \(NLU\) topics, configure NLU settings. For more information, see [Configure Natural Language Understanding in Virtual Agent](configure-nlu-settings.md).
-   Plan your conversation before you begin. For more information, see [Designing a Virtual Agent topic](../concept/design-va-topic.md).
-   Verify that you're in the appropriate application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the **ITSM Virtual Agent Conversations** scope \(and not the scope for the ITSM NLU Model for Virtual Agent Conversations\). For details, see [Change the application scope for Virtual Agent Designer topics](change-application-scope-vad.md).

Role required: virtual\_agent\_admin or admin

## About this task

The topic is in the Inactive state until you publish it. Publishing a topic changes the topic state to Active and automatically deploys the topic to your Virtual Agent clients.

The Large Language Model \(LLM\) topic type is faster and easier to set up compared to using Natural Language Understanding. You don't have to select NLU intents or train NLU models for your virtual agent. For more information, see [LLM topic discovery in Virtual Agent](../concept/va-llm.md).

When NLU is enabled, the Set up Natural Language Understanding \(NLU\) section is displayed in the Topic Properties page. You can use this section to specify the associated NLU model and intent for the topic. You can also optionally specify keywords that Virtual Agent can use as a fallback if NLU doesn't return a matching intent and topic. For more information, see [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent](../concept/va-NLU.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Set the discovery type toggle switch to **LLM** or **NLU/keyword** depending on the type of topic you're creating.

3.  Select the type of topic.

    -   For LLM topics:
        1.  Select **Create asset**.

            ![Assistant Designer Asset library page for Virtual Agent Designer with LLM topic discovery type andCreate asset button highlighted.](../images/vad-home-2.png)

        2.  From the Create asset window, select **Topic**.

            ![Create asset window with Topic selection highlighted.](../images/create-asset-2.png)

            **Important:** Selecting any of the other assets in the window will open the create flow in the respective application.

    -   For NLU/Keyword topics, select **Create topic**.

        ![Assistant Designer Asset library page set to NLU/Keyword topic discovery, and Create topic button highlighted.](../images/vad-home-nlu.png)

4.  On the form, fill in the fields.

    For a description of the field values, see [Create a topic form](../reference/vad-topic-creation-form.md).

5.  On the topic creation form, select **Create**.

6.  On the **Flow** tab, build the conversation flow.

<table id="table_mmy_blm_hmb"><thead><tr><th>

Flow steps

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add controls

</td><td>

To create the topic flow:

1.  Select the controls for user inputs, bot responses, or utilities from the palette and drop them onto the canvas.

When you add a control to the canvas, it becomes a node in the conversation flow.

2.  For each node, complete the corresponding property sheet. In the topic header bar, select **Save**. The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for 4 seconds, and can be closed by selecting the **X** in the message.

For details about each control and the corresponding properties that you define, see [User inputs](../reference/va-user-inputs.md), [Bot responses](../reference/va-bot-responses.md), and [Utilities](../reference/va-utilities.md).

 As you add controls, watch for a yellow warning badge or a red error badge in the corner of the control. The number on the badge indicates the number of issues in that control, such as missing mandatory information in the property sheet. \(Highlighting a badge or the "Incomplete" banner at the top of the property sheet details the items in need of correction.\)

</td></tr><tr><td>

Move a node

</td><td>

Select the node, drag it to the new location in the flow, and Select **Save**.

</td></tr><tr><td>

Delete a node

</td><td>

Select the **X** in the upper right corner of the node. In the topic header bar, select **Save**. The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for 4 seconds, and can be closed by selecting the **X** in the message.

 **Note:** You can't delete a node that has a script variable used by subsequent JavaScript expressions in the flow. Also, you can delete a decision node only when it has a single branch.

</td></tr></tbody>
</table>7.  Select **Test** in the header bar to test your topic in a chat window.

    You can review test results in the adjoining tabs. For detailed information, see [Testing LLM topics](../reference/test-llm-topics.md) and [Testing NLU/Keyword topics](../reference/va-designer-testing.md).

    If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments. For more information, see [Integrating Virtual Agent with messaging apps](../concept/va-integration-messaging-apps.md).

8.  When you're finished with the topic, select **Save** in the topic header bar.

    The topic is in the Inactive state until you publish it.

    The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for four seconds, and can be closed by selecting the **X** in the message.


## What to do next

[Publish](publish-virtual-agent-topic.md) the topic to deploy the topic to your Virtual Agent clients. The topic state changes to Active.

If you created a topic that might be frequently used in certain contexts \(environments\), consider promoting the topic as part of the [default or custom chat experience](../concept/va-conversation-settings.md).

-   **[NLU model mapping in Virtual Agent Designer](../concept/nlu-model-binding-vad.md)**  
ServiceNow model groups help you to manage the localization of both topics and Natural Language Understanding \(NLU\) models more easily. You can map Virtual Agent topics to a new or existing model group directly from Virtual Agent Designer.
-   **[Topic mapping to a multilingual NLU model group](../concept/multilingual-nlu-model-group-topic-mapping.md)**  
When you map a topic to a multilingual model group in Virtual Agent Designer, the topic mappings for enabled languages are set up automatically.
-   **[Modify NLU utterances and entities for a Virtual Agent topic](modify-nlu-utterances-va-topic.md)**  
View, test, and modify NLU utterances for a Virtual Agent topic on the **NLU Intent** tab in Virtual Agent Designer.
-   **[Add NLU to an existing keyword topic](add-nlu-existing-keyword-topic.md)**  
Create and map an NLU model group and intent for the topic from Virtual Agent Designer.
-   **[Add nodeless NLU entities as input variables to a topic](add-nodeless-entities-input-vars.md)**  
You can add nodeless NLU entities as input variables to a topic if NLU is enabled for Virtual Agent. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.
-   **[Branch a Virtual Agent conversation with a Decision utility](add-decision-utility-va-topic.md)**  
Your conversations may need to branch depending on end user input or choices. Use the Decision utility to branch the conversation when certain conditions are met.
-   **[Insert a header card in a Static Choice or Dynamic Choice control](insert-header-card-user-input-control.md)**  
When you create a Virtual Agent topic, you can include images and YouTube videos on Static Choice and Dynamic Choice user input controls.
-   **[Change the application scope for Virtual Agent Designer topics](change-application-scope-vad.md)**  
Set the application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the **ITSM Virtual Agent Conversations** scope \(and not the scope for the ITSM NLU \(Natural Language Understanding\) Model for Virtual Agent Conversations\).
-   **[Define script variables for a topic](define-script-variables-topic.md)**  
Use the Variables sidebar to define script variables for a topic. Script variables can store information that is not found in ServiceNow tables. This information can then be shared elsewhere in a topic.
-   **[Create a small talk topic](create-small-talk.md)**  
Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.
-   **[Control topic discovery and visibility](manage-topics-task.md)**  
Admins and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.
-   **[Use system-derived entities in an NLU topic](use-system-entities-va-topic.md)**  
Associate system-derived entities such as such as date, time, duration, or location with a node in a topic.

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

