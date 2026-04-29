---
title: Skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\)
description: Get a quick overview of the skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for OTSM, Operational Technology]
---

# Skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\)

Get a quick overview of the skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

## Now Assist for OTSM skill input overview

Depending on the selected skill, you can configure the inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate an incident summary. A trigger initiates an action, such as when the system generates Operational Technology \(OT\) resolution notes.

## OT incident summarization skill

The OT incident summarization skill includes the inputs that identify the table and fields that are used when an OT incident summary is generated.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The following table lists the inputs for the OT incident summarization skill.

<table id="table_case_summary_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

OT incident \[sn\_ot\_incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Priority
-   Site
-   Equipment model entity
-   OT device
-   OT incident task

</td></tr><tr><td>

Input template states

</td><td>

-   New
-   WIP
-   Resolved
-   Closed

</td></tr></tbody>
</table>The following table lists the descriptions for the OT incident summarization skill.

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

OT incident task

</td><td>

-   WIP
-   Resolved
-   Closed

</td></tr></tbody>
</table>## OT resolution notes generation skill

The OT resolution notes generation skill includes the inputs that identify the table and fields that are used when the resolution notes are generated for an OT incident.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The following table lists the inputs for the resolution notes generation skill.

<table id="table_resolution_notes_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

OT Incident \[sn\_ot\_incident\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Priority
-   Site
-   Equipment model entity
-   OT Device

</td></tr></tbody>
</table>**Parent Topic:**[Configure Now Assist for Operational Technology Service Management \(OTSM\)](configuring-now-assist-otsm.md)

