---
title: Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)
description: Get a quick overview of the skill inputs and triggers for Now Assist for IT Service Management \(ITSM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)

Get a quick overview of the skill inputs and triggers for Now Assist for IT Service Management \(ITSM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

## Now Assist for IT Service Management \(ITSM\) overview

Depending on the selected skill, you can configure the inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate an incident summary. A trigger initiates an action, such as when the system generates a chat summary.

## Incident sentiment analysis skill

<table id="table_rbs_gbj_l2c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Priority
-   State
-   Created
-   Additional comments
-   Task SLA

</td></tr></tbody>
</table><table id="table_lm1_qcj_l2c"><thead><tr><th>

Output

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sentiment values

</td><td>

-   Positive
-   Neutral
-   Negative

</td></tr><tr><td>

Sentiment trend

</td><td>

-   Improving
-   Declining
-   Stable

</td></tr><tr><td>

Sentiment reasoning

</td><td>

Reasons for providing the sentiment value.

</td></tr></tbody>
</table>|Scheduled job name|Default value|Description|
|------------------|-------------|-----------|
|Sentiment analysis scheduled job \(incident\)|True|Refreshes sentiments based on the trigger frequency.|

## Suggested steps generation skill

<table id="table_mjh_wxc_t2c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Input field

</td><td>

Short descriptionThe skill uses this field to cluster incidents based on similar incidents closed in the past.

</td></tr><tr><td>

Conditions

</td><td>

Filter conditions to generate the suggested steps.Similar incidents closed within the last 6 months are used by default to create the incident clusters.

</td></tr></tbody>
</table>## Major Incident email content recommendation skill

**Note:**

-   When you create a Major Incident email content recommendation using the default templates, you can use the corresponding Gen AI variables to compose the content.
-   For information on generating Major Incident email content recommendation, see [Major Incident Management email content recommendation](https://www.servicenow.com/docs/access?context=major-incident-management-email-content-recommendation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

<table id="table_cfn_tpt_t2c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Additional comments
-   Work notes
-   Activities

</td></tr><tr><td>

Additional fields

</td><td>

-   Business impact
-   Resolution notes

</td></tr></tbody>
</table>## Chat summarization skill

For the chat summarization skill, select the triggers that determine when a chat summary is generated. You can also select the properties that control how a chat summary is displayed.

The following table lists the triggers that determine when a chat summary is generated and how a chat summary is displayed.

|Trigger|Description|
|-------|-----------|
|Virtual Agent to Live Agent handoff|Chat summary that is generated when the chat handoff is done from Virtual Agent to a live agent.|
|Quick action|Chat summary that is generated when the live agent performs the `/summarize` quick action.|
|Chat wrap-up|Chat summary that is generated when the live agent ends the chat. The **Chat Summary** field is updated for the interaction.|
|Short description|**Short description** field that is updated for the interaction when the live agent ends the chat.|
|Task creation|**Short description** and **Description** fields that are auto-populated on the task record when a task is created.|

The following table lists the property for the chat summarization skill.

|Property|Description|
|--------|-----------|
|Bulleted list|If selected, the chat summary is displayed as an unordered list.|

## Chat reply recommendation skill

For the chat reply recommendation skill, select the triggers that determine when a chat reply recommendation is generated.

The following table lists the triggers that determine when a chat reply recommendation is generated.

|Trigger|Description|
|-------|-----------|
|User triggered|Chat reply recommendation that is generated when the agent manually triggers the skill.|

The following table lists the fields for the Now Assist icon for the chat reply recommendation skill.

<table id="table_k51_3ph_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Button Props

</td><td>

Trigger button properties, for example:-   Variant
-   Size
-   Icon

</td></tr><tr><td>

Refine Actions

</td><td>

Action options shown when the **Refine** button is selected, for example:-   Shorten
-   Elaborate

</td></tr><tr><td>

Recommendation Dialog Props

</td><td>

Recommendation dialog window properties, for example: headerLabel.

</td></tr><tr><td>

WWNA Component ID

</td><td>

Component ID that supports the Now Assist icon, for example: agent-chat.

</td></tr><tr><td>

Default Preset Action

</td><td>

Default action when the trigger button is selected with no text in the chat window.

</td></tr><tr><td>

Table

</td><td>

Table used for the interaction.

</td></tr><tr><td>

Timeout Error Message

</td><td>

Error that displays after a timeout.

</td></tr><tr><td>

Preset Actions

</td><td>

Action options shown when text is entered in the chat window and the trigger button is selected, for example:-   Shorten
-   Elaborate

</td></tr></tbody>
</table>## Sidebar discussion summarization skill

For the Sidebar discussion summarization skill, select the triggers that determine when a Sidebar discussion summary is generated.

The following table lists the triggers that determine when a Sidebar discussion summary is generated.

|Trigger|Description|
|-------|-----------|
|Quick action|Sidebar discussion summary that is generated when the live agent performs the `/summarize` quick action.|

|Property|Description|
|--------|-----------|
|Bulleted list|If selected, the Sidebar discussion summary is displayed as an unordered list.|

## Incident summarization skill

The incident summarization skill includes the inputs that identify the table and fields that are used when an incident summary is generated.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

|Trigger|Description|
|-------|-----------|
|Assign modal|Open assign modal during save action when assignment group or assigned to is changed.|

The following table lists the inputs for the incident summarization skill.

<table id="table_case_summary_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Email

</td></tr><tr><td>

Input template states

</td><td>

-   New
-   WIP
-   Resolved
-   Closed

</td></tr></tbody>
</table>The following table lists the descriptions for the incident summarization skill.

<table id="table_ayc_blh_bcc"><thead><tr><th>

Description

</th><th>

Mandatory for input state

</th></tr></thead><tbody><tr><td>

Issue

</td><td>

-   New
-   WIP
-   Resolved
-   Closed

</td></tr><tr><td>

Key Actions Taken

</td><td>

-   WIP
-   Resolved
-   Closed

</td></tr><tr><td>

Resolution

</td><td>

-   Resolved
-   Closed

</td></tr><tr><td>

Affected CIs and Impacted Services

</td><td>

-   WIP
-   Resolved
-   Closed

</td></tr><tr><td>

Service Level Agreement

</td><td>

-   WIP
-   Resolved
-   Closed

</td></tr><tr><td>

Child Incidents

</td><td>

-   WIP
-   Resolved
-   Closed

</td></tr></tbody>
</table>## Incident assist skill

The incident assist skill includes the incident topics to be available in the Now Assist panel.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

Incident assist topics:

-   Find similar resolved incidents
-   Consult on-call experts from support groups
-   Retrieve caller's assets
-   Retrieve caller's recent incidents

## Resolution notes generation skill

The resolution notes generation skill includes the inputs that identify the table and fields that are used when the resolution notes are generated for an incident.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the triggers that determine when and how the resolution notes for an incident are generated.

<table id="table_pmf_v3g_ddc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User triggered

</td><td>

If selected, user input is required before resolution notes are generated.

 Otherwise, resolution notes are generated automatically by default when certain conditions are met.

</td></tr></tbody>
</table>The following table lists the fields for the Now Assist icon for the resolution notes generation skill.

<table id="table_unk_3jh_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refine Actions

</td><td>

Action options shown when the **Refine** button is selected, for example:-   Shorten
-   Elaborate

</td></tr></tbody>
</table>The following table lists the inputs for the resolution notes generation skill.

<table id="table_resolution_notes_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Knowledge article generation skill

The knowledge article generation skill includes the inputs that identify the table and fields that are used when the knowledge article draft is generated for an incident.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the knowledge article generation skill.

<table id="table_ob5_lzl_cbc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Resolution notes
-   Work notes
-   Comments

</td></tr><tr><td>

State

</td><td>

-   Resolved
-   Closed

</td></tr></tbody>
</table>## Change request summarization skill

The change request summarization skill includes the inputs that identify the table and fields that are used when a change request summary is generated.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the change request summarization skill.

<table id="table_mjv_wmz_xbc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

change\_request

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Work notes
-   Additional comments
-   Risk
-   Impact
-   Justification
-   Implementation plan
-   Risk and impact analysis
-   Test plan
-   Backout plan
-   Close code
-   Close notes
-   Service offering
-   State
-   Conflict status
-   Type

</td></tr><tr><td>

Input template states

</td><td>

-   Assess
-   Authorize &amp; Scheduled
-   Implement &amp; Review
-   Closed

</td></tr></tbody>
</table>The following table lists the descriptions for the change request summarization skill.

<table id="table_uwx_hnh_bcc"><thead><tr><th>

Description

</th><th>

Mandatory for input state

</th></tr></thead><tbody><tr><td>

Objective

</td><td>

-   Assess
-   Authorize &amp; Scheduled
-   Implement &amp; Review
-   Closed

</td></tr><tr><td>

Plan

</td><td>

-   Assess
-   Authorize &amp; Scheduled
-   Implement &amp; Review
-   Closed

</td></tr><tr><td>

Risk

</td><td>

-   Assess
-   Authorize &amp; Scheduled
-   Implement &amp; Review
-   Closed

</td></tr><tr><td>

Affected CIs

</td><td>

-   Assess
-   Authorize &amp; Scheduled
-   Implement &amp; Review
-   Closed

</td></tr><tr><td>

Impacted services

</td><td>

-   Assess
-   Authorize &amp; Scheduled
-   Implement &amp; Review
-   Closed

</td></tr><tr><td>

Close notes

</td><td>

Closed

</td></tr><tr><td>

Incidents caused by change

</td><td>

Closed

</td></tr></tbody>
</table>## Change request risk explanation skill

The change request risk explanation skill includes the inputs that identify the table and fields that are used when the change risk explanation is generated.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the change request risk explanation skill.

<table id="table_fbq_fmf_bdc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

change\_request

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Implementation plan
-   Assignment group
-   Risk
-   Description
-   Blackout plan
-   Model type
-   Similar change requests and the incidents caused by those changes
-   Risk condition that was met

</td></tr></tbody>
</table>