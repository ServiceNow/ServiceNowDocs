---
title: Skill inputs and triggers for Now Assist for Customer Service Management \(CSM\)
description: Use the inputs and triggers for each skill to configure how and when a skill is used.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure Now Assist for Customer Service Management \(CSM\), Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Skill inputs and triggers for Now Assist for Customer Service Management \(CSM\)

Use the inputs and triggers for each skill to configure how and when a skill is used.

## Overview of skills and triggers

Depending on the selected skill, you can configure inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a case summary. A trigger initiates an action, such as when the system generates a chat summary.

## Chat summarization skill

For the chat summarization skill, select the triggers that determine when a chat summary is generated. You can also select the properties that control how a chat summary is displayed.

The following table lists the triggers that you can configure for the chat summarization skill of the Chat Assist feature.

|Trigger|Description|
|-------|-----------|
|Virtual Agent to Live Agent handoff|Chat summary that is generated when the chat handoff is done from Virtual Agent to a live agent.|
|Live Agent to Live Agent handoff|Chat summary that is generated when the chat handoff is done from a live agent to a live agent.|
|Quick action|Chat summary that is generated when the live agent performs the `/summarize` quick action.|
|Chat wrap-up|Chat summary that is generated when the live agent ends the chat. The **Chat Summary** field is updated for the interaction.|
|Short description|**Short description** field that is updated for the interaction when the live agent ends the chat.|
|Task creation|**Short description** and **Description** fields that are auto-populated on the task record when a task is created from an interaction.|

The following table lists the inputs for the chat summarization skill.

|Input|Description|
|-----|-----------|
|Chat conversations|Virtual Agent chat conversations are input data by default.|
|Portals|Portals to use as the source of the input data. You can't deselect the default product portal, and portals that are already in use by other products can't be selected.|

The following table lists the property that you can select to control how a chat summary is displayed.

|Property|Description|
|--------|-----------|
|Bulleted list|Chat summary as an unordered list.|

## Chat reply recommendation skill

For the chat reply recommendation skill, select the triggers that determine when a chat reply recommendation is generated.

The following table lists the triggers that determine when a chat reply recommendation is generated.

|Trigger|Description|
|-------|-----------|
|User triggered|Chat reply recommendation that is generated when the agent manually triggers the skill.|

<table id="table_cd5_1ln_bcc"><thead><tr><th>

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

Action options shown when the Refine button is selected, for example:-   Shorten
-   Elaborate

</td></tr><tr><td>

Recommendation Dialog Props

</td><td>

Recommendation dialog window properties, for example: headerLabel.

</td></tr><tr><td>

WWNA Component ID

</td><td>

Component ID that supports Now Assist context menu, for example: agent-chat.

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

For the sidebar discussion summarization skill, select the triggers that determine when a sidebar discussion summary is generated.

The following table lists the triggers that determine when a sidebar discussion summary is generated.

|Trigger|Description|
|-------|-----------|
|User triggered|Sidebar discussion summarization that is generated when the agent manually triggers the skill.|

## Case summarization skill

The case summarization skill includes the inputs that identify the table and fields that are used when a case summary is generated.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the case summarization skill.

<table id="table_case_summary_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Email
-   Service level agreement \(SLA\)

</td></tr></tbody>
</table>## Resolution notes generation skill

The resolution notes generation skill includes the inputs that identify the table and fields that are used when the resolution notes are generated for a case.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the resolutions notes generation skill.

<table id="table_resolution_notes_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Email

</td></tr></tbody>
</table><table id="table_nst_1qw_52c"><thead><tr><th>

Output

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Output table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Output fields

</td><td>

Resolution notes**Note:** The available output fields are all the multi-text fields of the table. By default it is the Resolution notes field.

</td></tr></tbody>
</table>## Email response skill

For the email response skill, select the triggers that determine when an email response is generated.

The following table lists the triggers that determine when an email response is generated.

| | |
|---|---|
|User triggered|Email response that is generated when the agent manually triggers the skill.|

<table id="table_mgk_ymn_bcc"><thead><tr><th>

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

Default Preset Action

</td><td>

Default action when the trigger button is selected with no text in the email window.

</td></tr><tr><td>

Preset Actions

</td><td>

Action options shown when text is entered in the chat window and the trigger button is selected, for example:-   Shorten
-   Elaborate

</td></tr><tr><td>

Recommendation Dialog Props

</td><td>

Recommendation dialog window properties, for example: headerLabel.

</td></tr><tr><td>

Refine Actions

</td><td>

Action options shown when the Refine button is selected, for example:-   Shorten
-   Elaborate

</td></tr><tr><td>

Table

</td><td>

Table used for the interaction.

</td></tr><tr><td>

Timeout Error Message

</td><td>

Error that displays after a timeout.

</td></tr><tr><td>

WWNA Component ID

</td><td>

Component ID that supports Now Assist context menu, for example: agent-chat.

</td></tr></tbody>
</table>## Knowledge article generation skill

The knowledge article generation skill includes the inputs that identify the table and fields that are used when the knowledge article draft is generated for a case.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the knowledge article generation skill.

<table id="table_mnf_45q_1bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Resolution notes \(for cases and incidents\)
-   Work notes
-   Comments

</td></tr></tbody>
</table>## Call summarization skill

For the call summarization skill, select the triggers that determine when a call summary is generated. You can also select the properties that control how a call summary is displayed.

The following table lists the triggers that you can configure for the call summarization skill of the Chat Assist feature.

|Trigger|Description|
|-------|-----------|
|Live Agent to Live Agent handoff|Call summary that is generated when the call handoff is done from a live agent to a live agent.|
|Call wrap-up|Call summary that is generated when the live agent or the user ends the chat. The **Chat summary** field is updated for the interaction.|
|Short description|**Short description** field that is updated for the interaction when the live agent or the user ends the call.|
|Task creation|**Short description** and **Description** fields that are auto-populated on the task record when a task is created from an interaction.|

The following table lists the property that you can select to control how a call summary is displayed.

|Property|Description|
|--------|-----------|
|Bulleted list|Call summary as an unordered list.|

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

## Case sentiment analysis skill

The case sentiment analysis skill includes the inputs and outputs that identify the table and fields that are used when a case sentiment is generated.

The following table lists the inputs for the case sentiment analysis skill.

<table id="table_apt_5cv_52c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[Case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Priority
-   State
-   Task creation date
-   Activities
-   Task SLA

</td></tr></tbody>
</table>The following table lists the outputs for the case sentiment analysis skill.

<table id="table_ffk_hfv_52c"><thead><tr><th>

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

Reasons for provide the sentiment value.

</td></tr></tbody>
</table>The following table lists the scheduled job for the sentiment analysis skill

|Scheduled job name|Default value|Description|
|------------------|-------------|-----------|
|Sentiment analysis scheduled job \(case\)|True|Refreshes sentiments on the Trigger frequency screen for the Sentiment analysis skill.|
|Update sentiment historical records|False|When active, calculates sentiment and sentiment trends for historical records.|

## Suggested steps generation skill

The following table lists the suggested steps generation skill

<table id="table_id3_4qw_52c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

sn\_customerservice\_case

</td></tr><tr><td>

Input field

</td><td>

Short description

 The skill uses this field to cluster cases based on similar cases closed in the past.

</td></tr><tr><td>

Conditions

</td><td>

Filter conditions to generate the suggested steps.

 Similar cases closed or resolved within the last 6 months are used by default to create the case clusters.

</td></tr></tbody>
</table>