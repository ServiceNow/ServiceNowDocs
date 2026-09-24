---
title: \(Legacy\) Create a topic form
description: The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/vad-topic-creation-form-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Virtual Agent Designer interface reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Create a topic form

The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.

The Create a topic form layout is similar to the Edit topic properties form layout found in the [Topic Properties tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topic-properties-tab.md). When you finish creating a topic using this form, the model type and topic types are locked in the Properties tab.

\[Omitted image "vad-create-topic-form-nlu.png"\] Alt text:

<table id="table_dzy_15h_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application scope

</td><td>

Select the application scope where the topic becomes available.**Note:** The application scope cannot be changed once the topic is created.

</td></tr><tr><td>

Model Type

</td><td>

Select **NLU/Keywords** for either keyword or NLU discovery.

 **Note:** This field is visible only if you installed Now Assist in Virtual Agent.

</td></tr><tr><td>

Type

</td><td>

List of assets that you can create. Select **Topic**.

</td></tr><tr><td>

Internal name

</td><td>

Internal name for topics, small talk topics, and setup topics that reflects its business purpose. Internal name displays on the Virtual Agent Designer Topics page and must be unique across the platform.

</td></tr><tr><td>

Display name

</td><td>

Topic name that displays to users when they interact with Virtual Agent. Display name must be unique for either NLU/Keywords or LLM model type.

</td></tr><tr><td>

Topic description

</td><td>

Brief explanation of the topic purpose and functionality.If you use single quotes \(‘ ’\) in your description, do the following to avoid problems with your conversation:

1.  Navigate to **All**, then enter `sys_properties.list` in the filter.
2.  Search for and select `glide.ui.escape_all_script`, then set its value to **True**.

</td></tr><tr><td>

NLU Model

</td><td>

Natural Language Understanding model to be mapped to the topic. The model contains the user utterances that are associated with the trained intents and entities. This combination enables your bot to understand what a user says. Do one of the following:

-   Choose an existing model.
-   Select **Create Model** to create a new model group.

    1.  In the **Model Name** field, enter a name for the new model group.
    2.  In the **Intent name** field, accept the default value or enter a name for the new intent.
**Note:** New models are created in **Draft** state.


 **Tip:** To see how and where the NLU model is used, navigate to **NLU Workbench** &gt; **Models**, and sort the **Created for** column.

</td></tr><tr><td>

Associated Intent

</td><td>

The intent, when recognized by Virtual Agent, that launches this topic. If you specified or created a model, the intent is required. Do one of the following:

-   Choose an existing intent.
-   Select **Create intent** to create a new intent.

In the **Intent Name** field, accept the default value or enter a name for the new intent.


**Note:** This option is not available for read-only models.

</td></tr><tr><td>

Enable DialogActs

</td><td>

Toggle switch \(active by default in new topics\) to enable Virtual Agent to detect when you modify utterances or applies updates in an NLU model, and dynamically reacts to unexpected utterances and modifications. Toggle to the off position to prevent users from using the keyboard instead of the options available in the topic. For more information, see [\(Legacy\) Dialog Acts for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/c_dialog-acts.md).**Note:** This toggle is decoupled from the topic switching option found in all User Inputs aside from Grouped Choice and File Picker. It's available for all topic types aside from a Topic Block. This feature is currently available only for English.

</td></tr><tr><td>

Confirm modified values with users

</td><td>

Toggle switch to enable Virtual Agent to send a confirmation message to the user when the Virtual Agent detects a value change. This value is Active by default.**Note:** This toggle appears when **Enable DialogActs** is activated.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced properties \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Who can access this topic

</td></tr><tr><td>

System Roles

</td><td>

Roles that a user must have to view and run the topic. If a topic is public \(available to users, including guest users, who aren't authenticated in the ServiceNow platform\), select only the Public role.

</td></tr><tr><td>

Channels

</td><td>

Chat clients in which the topic or topic block will run.

 These channels are different from the default channels that are natively supported by Virtual Agent. Your instance may have additional channels for [custom chat integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-custom-adapter-framework.md) created for it. For more information about channels, see [Deploying Virtual Agent topics in other channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-integrations.md).

</td></tr><tr><td>

Context

</td><td>

Expression logic to specify a condition for presenting this topic to users. The condition must evaluate to true. You can set this field using either the condition builder or a script.

-   **Condition**: Use the condition builder to add or edit conditions.
-   **Script**: Use the script editor to create or edit a script that contains a condition statement.

</td></tr><tr><td class="sub-head" colspan="2">

Live agent

</td></tr><tr><td>

Live agent context variables

</td><td>

Live agent context variables that are defined in the [General Chat Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-context-variables.md).Select the variables that provide dynamic context, which means information from the Virtual Agent chat. This information is transferred from the bot conversation to the live agent.

 For information about the default list of live agent variables, see [Live agent chat context variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/live-agent-chat-context-vars.md).

</td></tr><tr><td>

Available for Agent Autopilot

</td><td>

Toggle switch that determines whether the topic is available to a live agent.When enabled, an agent can search for and invoke the topic. For details, see [Conversation Autopilot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/agent-chat/ci-agent-chat-using.md).

</td></tr><tr><td class="sub-head" colspan="2">

Additional

</td></tr><tr><td>

Resume flow after topic switching

</td><td>

Toggle switch that lets the user return to the original conversation after changing topics during a conversation.

 Not applicable to Small Talk topics.

</td></tr><tr><td>

Categories

</td><td>

Label used to identify and group-related topics, topic blocks, or custom controls.

</td></tr><tr><td>

Keywords

</td><td>

List of key phrases or terms that users enter to initiate the conversation with the Virtual Agent. Press **Enter** after each phrase. Keywords are also used for languages that are currently not available in NLU.

</td></tr></tbody>
</table>**Parent Topic:**[\(Legacy\) Virtual Agent Designer interface reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-reference-nlu.md)

