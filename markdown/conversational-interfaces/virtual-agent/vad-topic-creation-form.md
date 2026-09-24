---
title: Create a topic form
description: The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/vad-topic-creation-form.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Assistant Designer interface reference, Reference, Virtual Agent, Conversational Interfaces]
---

# Create a topic form

The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.

The Create a topic form layout is similar to the Edit topic properties form layout found in the [Topic Properties tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topic-properties-tab.md). When you finish creating a topic using this form, the model type and topic types are locked in the Properties tab.

\[Omitted image "vad-topic-creation-form-manage-assistants.png"\] Alt text: The Create a topic form for LLM topics.

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

The **LLM** value is used for topic discovery within LLMs. For more information, see [LLM topic discovery in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-llm.md).

 **Note:** If this field doesn't appear, verify that both the ServiceNow Otto panel and ServiceNow Otto are turned on. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md) and [Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-now-assist-va.md).

</td></tr><tr><td>

Type

</td><td>

List of assets that you can create. Select **Topic**.

</td></tr><tr><td>

Internal name

</td><td>

Internal name for topics, small talk topics, and setup topics that reflects its business purpose. Internal name displays on the Assistant Designer Asset library and must be unique across the platform.

</td></tr><tr><td>

Display name

</td><td>

Topic name that displays to users when they interact with Virtual Agent. Display name must be unique.

</td></tr><tr><td>

Topic description used for discovery

</td><td>

A detailed explanation of the LLM topic's purpose, which differentiates it from other topics. The description is used for topic discovery, so the more detailed and specific the topic description is, the more likely it will be to find a good match.

A weak example would be: `Help users see how many vacation days they have left.` A stronger example would be `This topic is about a holiday calendar for employees in a company. Users can ask for the holiday list or company holiday for a specific year, specific date, inquire about a specific holiday, or ask if they have a day off for a particular holiday. The topic also covers the availability of a holiday calendar and specific holidays like Freedom Day and wellbeing Day.`

For more information, see[LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-llm-instruction-guidelines.md).

</td></tr><tr><td>

Select LLM assistants to make topics available to them and any primary assistants

</td><td>

The LLM assistant that you associate with the topic for more accurate topic discovery. If you established primary and secondary assistants during the ServiceNow Otto for Virtual Agent guided setup, an on-screen message explains whether the selected assistant is a primary or secondary assistant. When testing a primary LLM assistant, topics from the secondary assistants are included in topic discovery. To view the LLM assistants and their hierarchy, select **Manage assistants**.

 If you associate a topic block and a related topic with the same LLM assistant, both are shown as associated with that assistant.

 When you add an LLM assistant or remove one from your topic, the topic reverts to unpublished.

 When you associate an LLM topic with an LLM assistant and publish it, a record for the association is created in the Profile and Document Mapping \[sys\_cs\_document\_context\_profile\] table. If you dissociate the Setup topic from the LLM assistant before republishing, the record is deleted.

 For more information, see [Create LLM assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/llm-assistants.md).

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

</td></tr><tr><td class="sub-head" colspan="2">

Additional

</td></tr><tr><td>

Categories

</td><td>

Label used to identify and group-related topics, topic blocks, or custom controls.

</td></tr></tbody>
</table>**Parent Topic:**[Assistant Designer interface reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-reference.md)

