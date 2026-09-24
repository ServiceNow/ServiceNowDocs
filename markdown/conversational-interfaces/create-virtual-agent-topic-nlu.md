---
title: \(Legacy\) Creating a Virtual Agent NLU topic
description: Use Virtual Agent Designer to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/create-virtual-agent-topic-nlu.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
keywords: [Create, Virtual Agent, topic, topic, designer, conversations, LLM, NLU, Large language model, Natural Language Understanding]
breadcrumb: [Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Creating a Virtual Agent NLU topic

Use Virtual Agent Designer to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.

## Before you begin

Do the following:

-   Review [\(Legacy\) Getting started with Virtual Agent Designer for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent-nlu.md).
-   Configure Virtual Agent NLU settings. For more information, see [\(Legacy\) Configure Natural Language Understanding in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-nlu-settings.md).
-   Plan your conversation before you begin. For more information, see [Designing a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/design-va-topic.md).
-   Verify that you're in the appropriate application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the **ITSM Virtual Agent Conversations** scope \(and not the scope for the ITSM NLU Model for Virtual Agent Conversations\). For details, see [\(Legacy\) Change the application scope for Virtual Agent Designer topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/change-application-scope-vad.md).

Role required: virtual\_agent\_admin or admin

## About this task

The topic is in the Inactive state until you publish it. Publishing a topic changes the topic state to Active and automatically deploys the topic to your Virtual Agent clients.

When NLU is enabled, the Set up Natural Language Understanding \(NLU\) section is displayed in the Topic Properties page. You can use this section to specify the associated NLU model and intent for the topic. You can also optionally specify keywords that Virtual Agent can use as a fallback if NLU doesn't return a matching intent and topic. For more information, see [\(Legacy\) Natural Language Understanding \(NLU\) topic discovery in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-NLU.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the Topics page, select **Create**.

3.  On the form, fill in the fields.

    For a description of the field values, see [\(Legacy\) Create a topic form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-topic-creation-form-nlu.md).

4.  On the **Flow** tab, build the conversation flow.

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

For details about each control and the corresponding properties that you define, see [User inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-user-inputs-nlu.md), [Bot responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-bot-responses.md), and [Utilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-utilities.md).

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
</table>5.  Select **Test** in the header bar to test your topic in a chat window.

    You can review test results in the adjoining tabs. For detailed information, see [\(Legacy\) Testing NLU/Keyword topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-designer-testing.md).

    If the ServiceNow Otto panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Otto panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments. For more information, see [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md).

6.  When you're finished with the topic, select **Save** in the topic header bar.

    The topic is in the Inactive state until you publish it.

    The topic header bar displays a `Saving in progress...` message. The toast message `Successfully saved your topic` appears in the lower-right corner afterward for four seconds, and can be closed by selecting the **X** in the message.


## What to do next

[Publish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md) the topic to deploy the topic to your Virtual Agent clients. The topic state changes to Active.

If you created a topic that might be frequently used in certain contexts \(environments\), consider promoting the topic as part of the [default or custom chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-conversation-settings.md).

-   **[\(Legacy\) NLU model mapping in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/nlu-model-binding-vad.md)**  
ServiceNow model groups help you to manage the localization of both topics and Natural Language Understanding \(NLU\) models more easily. You can map Virtual Agent topics to a new or existing model group directly from Virtual Agent.
-   **[\(Legacy\) Topic mapping to a multilingual NLU model group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/multilingual-nlu-model-group-topic-mapping.md)**  
When you map a topic to a multilingual model group in Virtual Agent Designer, the topic mappings for enabled languages are set up automatically.
-   **[\(Legacy\) Modify NLU utterances and entities for a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/modify-nlu-utterances-va-topic.md)**  
View, test, and modify NLU utterances for a Virtual Agent topic on the **NLU Intent** tab in Virtual Agent Designer.
-   **[\(Legacy\) Change the application scope for Virtual Agent Designer topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/change-application-scope-vad.md)**  
Set the application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the **ITSM Virtual Agent Conversations** scope \(and not the scope for the ITSM NLU \(Natural Language Understanding\) Model for Virtual Agent Conversations\).
-   **[\(Legacy\) Create a small talk topic for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-small-talk-nlu.md)**  
Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.
-   **[\(Legacy\) Add NLU to an existing keyword topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/add-nlu-existing-keyword-topic.md)**  
Create and map an NLU model group and intent for the topic from Assistant Designer.
-   **[\(Legacy\) Add nodeless NLU entities as input variables to a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/add-nodeless-entities-input-vars.md)**  
You can add nodeless NLU entities as input variables to a topic if NLU is enabled for Virtual Agent. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.
-   **[\(Legacy\) Use system-derived entities in an NLU topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/use-system-entities-va-topic.md)**  
Associate system-derived entities such as such as date, time, duration, or location with a node in a topic.

**Parent Topic:**[\(Legacy\) Building and deploying Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/using-virtual-agent-nlu.md)

