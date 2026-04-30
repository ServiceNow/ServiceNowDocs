---
title: Configure Now Assist for Sourcing and Procurement Operations \(SPO\)
description: If you have the sn\_nowassist\_admin.nsa\_admin role, you can configure the Now Assist for Sourcing and Procurement Operations \(SPO\) application so that your requesters, procurement specialists, and sourcing managers can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and Core UI.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure Now Assist for Sourcing and Procurement Operations \(SPO\)

If you have the sn\_nowassist\_admin.nsa\_admin role, you can configure the Now Assist for Sourcing and Procurement Operations \(SPO\) application so that your requesters, procurement specialists, and sourcing managers can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and Core UI.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

The following Now Assist for Sourcing and Procurement Operations \(SPO\) fulfillers skills are activated by default:

-   Email response for acknowledgement task
-   Email response for negotiation
-   Email response for procurement case
-   Email response for procurement task
-   Email response for purchase requisition
-   Email response for sourcing event
-   Email response for sourcing request
-   Email response for sourcing task
-   Sentiment analysis for procurement case
-   Sourcing request summarization for fulfillers
-   Sourcing event summarization for fulfillers
-   Negotiation summarization for fulfillers
-   Purchase requisition summarization for fulfillers
-   Procurement case summarization for fulfillers

If the Now Assist for Sourcing and Procurement Operations \(SPO\) fulfillers skills are turned off, you can reactivate them or configure them using the Now Assist Admin console. The console contains everything that you need to install the plugins and configure the generative AI skills. For more information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

|Now Assist for SPO skills|Description|
|-------------------------|-----------|
|Document extraction|Enables requesters to define and customize the fields that Now Assist extracts from uploaded Statements of Work \(SOWs\), quotes, and other supporting attachments.|
|Email response for acknowledgement task|Generate email responses and suggest templates for acknowledgement tasks based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for negotiation|Generate email responses and suggest templates for negotiations based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for procurement case|Generate email responses and suggest templates for procurement cases based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for procurement task|Generate email responses and suggest templates for procurement tasks based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for purchase requisition|Generate email responses and suggest templates for purchase requisitions based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for sourcing event|Generate email responses and suggest templates for sourcing events based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for sourcing request|Generate email responses and suggest templates for sourcing requests based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Email response for sourcing task|Generate email responses and suggest templates for sourcing tasks based on conversation context to help fulfillers draft emails quickly and maintain clear communication.|
|Negotiation summarization for fulfillers|Summarize negotiations to keep fulfillers informed on their status, progress, and action items.|
|Procurement case summarization for fulfillers|Summarize procurement cases and keep fulfillers informed about their status, progress, and action items.|
|Purchase requisition summarization for fulfillers|Summarize purchase requisitions and keep fulfillers informed about their status, progress, and action items.|
|Purchase requisition summarization for requesters|Summarize purchase requisitions to keep requesters informed about their status, progress, and action items.|
|Product category predictor|Suggests the most likely product category for a fulfiller when the primary ML-based category prediction doesn’t meet the confidence threshold.|
|Purchase order summarization for requesters|Summarize purchase orders to keep requesters informed about their status, progress, and action items.|
|Sentiment analysis for procurement case|Analyze requester sentiment across procurement case to help fulfillers prioritize urgent issues and make informed decisions. This skill provides sentiment evaluations, trend analysis, and AI-generated summaries that explain the reasoning behind each sentiment.|
|Sourcing event summarization for fulfillers|Summarize sourcing events to keep fulfillers informed on their status, progress, and action items.|
|Sourcing request summarization for fulfillers|Summarize sourcing requests and keep fulfillers informed about their status, progress, and action items.|
|Sourcing request summarization for requesters|Summarize sourcing requests to keep requesters informed about their status, progress, and action items.|
|Spend category predictor|Suggests the appropriate spend category for a fulfiller when primary ML-based category prediction doesn’t meet the confidence threshold.|

![Skills available on Now Assist for Sourcing and Procurement Operations.](../image/now-assist-spo-explore.png "Now Assist skills for SPO")

## Procedure

1.  Install the Now Assist for Sourcing and Procurement Operations \(SPO\) plugin \(sn\_spend\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for Now Assist for Sourcing and Procurement Operations \(SPO\)](../concept/now-assist-spo-supporting-info.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Features** tab of the Now Assist Admin console.

3.  Expand the **Finance and Supply Chain** workflow group and select **Sourcing and Procurement Operations**.

    The Sourcing and Procurement Operations features are grouped under the Finance and Supply Chain workflow group. Each feature has its associated skills.

4.  Activate and configure the skills for Now Assist for Sourcing and Procurement Operations \(SPO\).

<table id="table_bcq_z34_tcc"><thead><tr><th>

Skills

</th><th>

Action

</th></tr></thead><tbody><tr><td>

-   Sourcing request summarization for requesters
-   Purchase requisition summarization for requesters
-   Purchase order summarization for requesters
-   Document extraction


</td><td>

On the skill card that you want to activate, select **Activate skill**.

</td></tr><tr><td>

-   Email response for acknowledgement task
-   Email response for negotiation
-   Email response for procurement case
-   Email response for procurement task
-   Email response for purchase requisition
-   Email response for sourcing event
-   Email response for sourcing request
-   Email response for sourcing task
-   Sentiment analysis for procurement case
-   Sourcing request summarization for fulfillers
-   Purchase requisition summarization for fulfillers
-   Procurement case summarization for fulfillers
-   Negotiation summarization for fulfillers
-   Sourcing event summarization for fulfillers


</td><td>

On the skill card that you want to activate, select **Activate skill**.

</td></tr></tbody>
</table>5.  Select **General details** and review the details about the skill and select **Save and continue** to go to the next step in the Guided Setup.

6.  Follow the steps to configure and activate a skill using the Guided Setup.

7.  Select **Choose input** for the skill and review the base input table and input fields, and then select **Save and continue** to go to the next step in the Guided Setup.

8.  Select **Customize and test prompt** to test the prompt on a record.

9.  Select **Save and continue** to go to the next step in the Guided Setup.

10. Select **Define availability** and choose one of the following options.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d189182e690">

Option

</th><th align="left" id="d189182e693">

Description

</th></tr></thead><tbody><tr><td id="d189182e699">

**Skill is always available**

</td><td>

Skill is continuously available to users.

</td></tr><tr><td id="d189182e708">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>11. Select **Save and continue** to go to the next step in the Guided Setup.

12. Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d189182e744">

Option

</th><th align="left" id="d189182e747">

Description

</th></tr></thead><tbody><tr><td id="d189182e753">

**In-product desktop**

</td><td>

Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td id="d189182e764">

**Now Assist panel**

</td><td>

Now Assist skills are available in the Now Assist panel. Now Assist skills are available in the Now Assist panel. Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications. For more information, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

**Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>13. Select **Save and continue** to go to the next step.

14. Review your choices and select **Activate** to complete the configuration for the skill.

15. Select **Return to Sourcing and Procurement Operations.**.

    The skill is activated.


-   **[Customize a Now Assist for Sourcing and Procurement Operations \(SPO\) skill](cust-now-assist-spo-skill.md)**  
If you have the sn\_nowassist\_admin.nsa\_admin role, you can customize a Now Assist for Sourcing and Procurement Operations \(SPO\) skill so that fulfillers and requesters can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and in Core UI.
-   **[Skill inputs for Now Assist for Sourcing and Procurement Operations \(SPO\)](../reference/input-triggers-now-assist-spo.md)**  
You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.

**Parent Topic:**[Now Assist for Sourcing and Procurement Operations \(SPO\)](../concept/now-assist-spo.md)

