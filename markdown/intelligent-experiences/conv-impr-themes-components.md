---
title: Components installed with Conversation Improvement Themes
description: Several types of components are part of Conversation Improvement Themes, including scheduled jobs, tables, system properties, and flows.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-10"
reading_time_minutes: 2
breadcrumb: [Reference, Conversation Improvement Themes, Enable AI experiences]
---

# Components installed with Conversation Improvement Themes

Several types of components are part of Conversation Improvement Themes, including scheduled jobs, tables, system properties, and flows.

## Roles added

|Role|Description|
|----|-----------|
|sn\_na\_thematic.theme\_admin|Primary role to access dashboard and tables installed with the application.|

## Scheduled jobs installed

<table id="table_bps_dyg_ngc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create thematic executions

</td><td>

This scheduled job runs once a month and creates Themes Execution Staging Records that create themes and their description and tags knowledge articles, catalog items, VA topics, AI Agents, and conversations to these themes.

</td></tr><tr><td>

Themes - Create Daily Primary Request Executions

</td><td>

Runs daily and creates Themes Execution Staging Records that tags conversations to the existing themes, and if necessary, creates new themes

</td></tr><tr><td>

Update Theme Effective and Ineffective Scores

</td><td>

Runs daily and populates number of effective conversations and number of ineffective conversations for every theme.

</td></tr></tbody>
</table>## Tables installed

<table id="table_xmn_qj4_hgc"><thead><tr><th>

Label

</th><th>

Name

</th></tr></thead><tbody><tr><td>

Themes Configurations \[sn\_na\_thematic\_themes\_configuration\]

</td><td>

Contains various configurations for Conversation Improvement Themes.Configuration Name - Last scan date: Contains the last scanned date of the theme creation. After the first run, theme extraction and theme description update will only run on content updated or created after the last run date.

</td></tr><tr><td>

Themes \[sn\_na\_thematic\_themes\]

</td><td>

Contains the themes created along with their descriptions.

</td></tr><tr><td>

Themes associations \[sn\_na\_thematic\_associates\]

</td><td>

Contains the relationship between themes and different content types tagged to that theme.

</td></tr><tr><td>

Primary Requests \[sn\_na\_thematic\_primary\_request\]

</td><td>

Contains all the primary requests extracted from evaluated chats.

</td></tr></tbody>
</table>## System properties installed

<table id="table_nby_14p_hgc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_na\_thematic.dataChunkSize

</td><td>

The default chunk size, used for Azure Open AI provider and as a backup. The default chunk size is 100.

 If you see Themes Execution staging record is either in a failed state or stuck on processing for a long time, reduce the chunk size and change the state of the Execution staging record to draft and then again to processing.

</td></tr><tr><td>

sn\_na\_thematic.fallbackDataChunkSize

</td><td>

If any of the theme skills are not part of the Azure Open AI provider, the fallback size is used to create execution staging records.

 If you see Themes Execution staging record is either in a failed state or stuck on processing for a long time, reduce the chunk size and change the state of the Execution staging record to draft and then again to processing.

 The default chunk size is 25. But it should be set differently for different LLMS.

-   Gemini: 25
-   Claude: 10
-   Now LLM: 1

</td></tr></tbody>
</table>## Business rules installed

|Name|Description|
|----|-----------|
|Theme tagging|An asynchronous business rule that runs the state of the Themes Execution Staging record changes to processing. It invokes the Theme Tagging subflow.|
|Themes Update next record to processing|Runs state of the Themes Execution Staging record changes to Classification Complete, Complete or Failed.|

## Subflows installed

|Flow|Description|
|----|-----------|
|Theme Tagging|Executes when the state of the Themes Execution Staging record changes to processing. The subflow creates themes, updates their description, and then tags knowledge articles, catalog items, VA Topics, AI agents, and conversations with the themes and moves the state of the Themes Execution staging record to complete.|
|Primary Theme Tagging|The subflow is called from Theme Tagging subflow. It tags conversations to the existing themes and if necessary, creates new themes.|

## Script includes installed

|Script includes|Description|
|---------------|-----------|
|themesUtil|Primary utility function for Conversation Evaluator.|

**Parent Topic:**[Reference for Conversation Improvement Themes](conv-impr-themes-reference.md)

