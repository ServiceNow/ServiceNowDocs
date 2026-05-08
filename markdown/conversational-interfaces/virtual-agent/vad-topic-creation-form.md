---
title: Create a topic form
description: The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Create a topic form

The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.

The Create a topic form layout is similar to the Edit topic properties form layout found in the [Topic Properties tab](vad-topic-properties-tab.md). When you finish creating a topic using this form, the model type and topic types are locked in the Properties tab.

**Note:** Large language model \(LLM\) topics are faster and easier to set up and configure compared with NLU topics. The LLM model type doesn't need you to select, configure, or train models or intents. For more information, see [LLM topic discovery in Virtual Agent](../concept/va-llm.md).

![Two versions of the Create a topic form. First model type is LLM, where a description is required for topic discovery. Second model type is NLU/Keywords.](../images/vad-topic-creation-form-manage-assistants.png "Create a topic form, compared between LLM and NLU/Keyword model types")

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

The **LLM** value is used for topic discovery within LLMs, and the **NLU/Keywords** value is used for either keyword or NLU discovery. For more information, see [LLM topic discovery in Virtual Agent](../concept/va-llm.md).

 **Note:** If this field doesn't appear, verify that both the Now Assist panel and Now Assist in Virtual Agent are turned on. For more information, see Activate the Now Assist panel standard chat and [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md).

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

</td></tr><tr><td class="sub-head" colspan="2">

LLM topics\[LLM topic discovery only\]

</td></tr><tr><td>

Topic description used for discovery

</td><td>

A detailed explanation of the LLM topic's purpose, which differentiates it from other topics. The description is used for topic discovery, so the more detailed and specific the topic description is, the more likely it will be to find a good match.

A weak example would be: `Help users see how many vacation days they have left.` A stronger example would be `This topic is about a holiday calendar for employees in a company. Users can ask for the holiday list or company holiday for a specific year, specific date, inquire about a specific holiday, or ask if they have a day off for a particular holiday. The topic also covers the availability of a holiday calendar and specific holidays like Freedom Day and wellbeing Day.`

For more information, see[LLM description and instruction guidelines for Virtual Agent topics](../concept/va-llm-instruction-guidelines.md).

</td></tr><tr><td>

Select LLM assistants to make topics available to them and any primary assistants

</td><td>

The LLM assistant that you associate with the topic for more accurate topic discovery. If you established primary and secondary assistants during the Now Assist in Virtual Agent guided setup, an on-screen message explains whether the selected assistant is a primary or secondary assistant. When testing a primary LLM assistant, topics from the secondary assistants are included in topic discovery. To view the LLM assistants and their hierarchy, select **Manage assistants**.

 If you associate a topic block and a related topic with the same LLM assistant, both are shown as associated with that assistant.

 When you add an LLM assistant or remove one from your topic, the topic reverts to unpublished.

 When you associate an LLM topic with an LLM assistant and publish it, a record for the association is created in the Profile and Document Mapping \[sys\_cs\_document\_context\_profile\] table. If you dissociate the Setup topic from the LLM assistant before republishing, the record is deleted.

 For more information, see [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md).

</td></tr><tr><td class="sub-head" colspan="2">

Natural Language Understanding \(NLU\) topics\[NLU/Keywords topic discovery only\]

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

Toggle switch \(active by default in new topics\) to enable Virtual Agent to detect when you modify utterances or applies updates in an NLU model, and dynamically reacts to unexpected utterances and modifications. Toggle to the off position to prevent users from using the keyboard instead of the options available in the topic. For more information, see [Dialog Acts for Virtual Agent](../concept/c_dialog-acts.md).**Note:** This toggle is decoupled from the topic switching option found in all User Inputs aside from Grouped Choice and File Picker. It's available for all topic types aside from a Topic Block. This feature is currently available only for English.

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

 These channels are different from the default channels that are natively supported by Virtual Agent. Your instance may have additional channels for [custom chat integrations](../concept/va-custom-adapter-framework.md) created for it. For more information about channels, see [Deploying Virtual Agent topics in other channels](../concept/va-integrations.md).

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

Live agent context variables that are defined in the [General Chat Settings](../../conversational-interfaces/task/ac-configure-context-variables.md).Select the variables that provide dynamic context, which means information from the Virtual Agent chat. This information is transferred from the bot conversation to the live agent.

 For information about the default list of live agent variables, see [Live agent chat context variables](live-agent-chat-context-vars.md).

</td></tr><tr><td>

Available for Agent Autopilot

</td><td>

Toggle switch that determines whether the topic is available to a live agent.When enabled, an agent can search for and invoke the topic. For details, see [Conversation Autopilot](../../conversational-interfaces/concept/ci-agent-chat-using.md#).

Applicable to only keyword or NLU topic discovery.

</td></tr><tr><td class="sub-head" colspan="2">

Additional

</td></tr><tr><td>

Resume flow after topic switching

</td><td>

Toggle switch that lets the user return to the original conversation after changing topics during a conversation.

 Applicable to only keyword or NLU topic discovery. Not applicable to Small Talk topics.

</td></tr><tr><td>

Categories

</td><td>

Label used to identify and group-related topics, topic blocks, or custom controls.

</td></tr><tr><td>

Keywords\[NLU/Keywords topic discovery only\]

</td><td>

List of key phrases or terms that users enter to initiate the conversation with the Virtual Agent. Press **Enter** after each phrase. Keywords are also used for languages that are currently not available in NLU.

</td></tr></tbody>
</table>**Parent Topic:**[Assistant Designer interface reference](../concept/vad-reference.md)

