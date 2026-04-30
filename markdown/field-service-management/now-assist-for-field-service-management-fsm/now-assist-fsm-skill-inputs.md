---
title: Skill inputs for Now Assist for Field Service Management \(FSM\)
description: Use the inputs for each skill to configure how a skill is used.
locale: en-US
release: yokohama
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist for Field Service Management \(FSM\), Now Assist for Field Service Management \(FSM\)]
---

# Skill inputs for Now Assist for Field Service Management \(FSM\)

Use the inputs for each skill to configure how a skill is used.

## Skills overview

Depending on the selected skill, you can configure inputs. These settings determine how a skill is used. An input identifies the data that is used for a skill, such as the table and fields used to generate a work order task summary.

## Sidebar discussion summarization skill

For the sidebar discussion summarization skill, select the triggers that determine when a sidebar discussion summary is generated.

The following table lists the triggers that determine when a sidebar discussion summary is generated.

|Trigger|Description|
|-------|-----------|
|User triggered|Sidebar discussion summarization that is generated when the agent manually triggers the skill.|

## Work order task summarization skill

The work order task summarization skill includes the inputs that identify the table and fields that are used when a closure note summary is generated.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the work order task summarization skill.

<table id="table_case_summary_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Work Order Task \[wm\_task\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Affected Product name
-   Part requirement model
-   Part requirement required quantity
-   Part requirement reserved quantity

</td></tr></tbody>
</table>## KB generation skill

The KB generation skill includes the inputs that identify the table and fields that are used when the knowledge article draft is generated for a case.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the knowledge article generation skill.

<table id="table_mnf_45q_1bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Work Order Task \[wm\_task\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Work notes
-   Comments

</td></tr></tbody>
</table>