---
title: Skill inputs and triggers for Now Assist for Public Sector Digital Services \(PSDS\)
description: Use the inputs and triggers for each skill to configure how and when a skill is used.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-23"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Skill inputs and triggers for Now Assist for Public Sector Digital Services \(PSDS\)

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

The following table lists the inputs for the case summarization skill.

|Input|Description|
|-----|-----------|
|Chat conversations|Virtual Agent chat conversations are input data by default.|
|Portals|Portals to use as the source of the input data. You can't deselect the default product portal, and portals that are already in use by other products can't be selected.|

The following table lists the property that you can select to control how a chat summary is displayed.

|Property|Description|
|--------|-----------|
|Bulleted list|Chat summary as an unordered list. When this option is set to Off, the chat summary can be viewed in paragraph form.|

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
</table>