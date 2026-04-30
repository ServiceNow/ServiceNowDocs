---
title: Skill inputs for Now Assist for Public Sector Digital Services \(PSDS\)
description: Use the inputs and triggers for each skill to configure how and when a skill is used.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Skill inputs for Now Assist for Public Sector Digital Services \(PSDS\)

Use the inputs and triggers for each skill to configure how and when a skill is used.

## Overview of skills

Depending on the selected skill, you can configure inputs. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a case summary.

## Chat summarization skill



The following table lists the inputs for the chat summarization skill.

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

Case \[sn\_gsm\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>