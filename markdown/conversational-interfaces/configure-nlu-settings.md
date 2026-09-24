---
title: \(Legacy\) Configure Natural Language Understanding in Virtual Agent
description: Configure Natural Language Understanding \(NLU\) in Virtual Agent to identify the NLU service provider for your instance. You can also specify the languages of NLU models used during conversation design, based on the languages supported by your NLU provider and the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/configure-nlu-settings.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Configure Natural Language Understanding in Virtual Agent

Configure Natural Language Understanding \(NLU\) in Virtual Agent to identify the NLU service provider for your instance. You can also specify the languages of NLU models used during conversation design, based on the languages supported by your NLU provider and the ServiceNow AI Platform®.

## Before you begin

You can select only one NLU service provider for your instance. Virtual Agent supports the following NLU services:

-   **ServiceNow NLU** \(default\): Create your models, intents, and entities in Virtual Agent Designer and NLU Workbench.
-   **IBM Watson Assistant**: [Configure the IBM Watson Assistant intent and entity integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-watson-service-integration.md) so that Virtual Agent can access IBM Watson Assistant NLU model information.
-   **Google DialogFlow Essentials \(ES\)**: [Configure the Google DialogFlow ES intent and entity integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-dialogflow-es-integration.md) so that Virtual Agent can access Google Dialogflow ES NLU model information.

The **Activate** toggle switch for NLU is toggled on for all new Virtual Agent activations and the **NLU Service Provider** defaults to **ServiceNow NLU**. The **Activate** toggle switch is toggled off for Virtual Agent Lite. If you upgraded from the previous release, Virtual Agent retains the NLU settings and integration information for your NLU service provider.

Role required: virtual\_agent\_admin or admin

## About this task

The NLU-enabled topics that you preview, create, or update in Virtual Agent Designer must use NLU models created in the NLU service that you select here. For example, if you specify ServiceNow as the service provider, you can view and access topics that use ServiceNow NLU model groups.

Similarly, to work on NLU topics in multiple languages, the languages must be enabled in your NLU service and added to your model groups. For more information, see [Multilingual model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/multilingual-model-managent.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Click **Virtual Agent**.

3.  Under Natural Language Understanding \(NLU\), click **View Settings**.

4.  On the form, fill in the fields.

<table id="table_rx3_4sl_lpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NLU Service Provider

</td><td>

Available NLU service providers for intent and entity extraction. The Supported NLU Languages list is displayed. It shows all of the language plugins that have been installed. For **ServiceNow NLU**, English is enabled to **true** by default.

 This field is automatically set to **ServiceNow NLU**.

</td></tr><tr><td>

Ask user if topic VA chose is correct

</td><td>

Option to prompt the user to confirm that the matched intent is correct. This option enables user confirmation only on initial intent discovery.When enabled, Virtual Agent asks the user for confirmation before continuing to the automatically selected topic content. Enabling this field triggers the **Intent confirmation message** field.

If the user selects **No** for an initial intent, then Virtual Agent runs the global fallback topic. If the user selects **No** for an automatically selected intent in mid-topic, then Virtual Agent returns to the topic that the user was in.

</td></tr><tr><td>

Ask user if switched topic is correct

</td><td>

Option to prompt the user to confirm that the switched intent is correct. This option is enabled by default and prompts user confirmation only when the user triggers an intent switch in mid-topic.When enabled, Virtual Agent asks the user for confirmation before continuing to the switched topic content. Enabling this field triggers the **Intent confirmation message** field.

</td></tr></tbody>
</table>5.  Edit the **Intent confirmation message** field, if needed.

    Text entered in this field is shown to the user to confirm that the matched intent is correct.

6.  If you plan to use language-specific NLU models, enable the languages in the Supported NLU Languages list.

    A language is enabled if the Enabled column displays **true**. For more information, see [\(Legacy\) Enable NLU languages in Virtual Agent settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/enable-langs-va-gen-settings.md).

7.  Click **Save**.


## Result

When you create or update a topic in Virtual Agent Designer, you can choose NLU models available for your specified NLU provider and the specified languages, if applicable. You can also set the NLU entity properties for the input controls that you add to your topic flow.

