---
title: Automation finding definition form from Classic view
description: Use the Automated Finding definition form to create a finding definition from the Classic view.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Process Mining reference, Process Mining, Platform Analytics]
---

# Automation finding definition form from Classic view

Use the Automated Finding definition form to create a finding definition from the Classic view.

<table id="table_lwy_lvq_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Title for the improvement opportunity. This text appears at the top of the Insights card on the Summary and Insights page.

</td></tr><tr><td>

Type

</td><td>

Type of finding. You can select from the list available. Three options are available:-   Rework: Refers to a repeating step or activity in the process. It happens when a process step must be redone or revisited.
-   Ping-Pong: Refers to a repetitive pattern where a record bounces between two process steps or activities without interruption, indicating a loop.
-   Extra step: Compares each route to identify the existence of different routes that deviate in only one step, thus pinpointing process steps where unnecessary transitions occur.
-   Repeating patterns: Detects unnecessary repeating sequence of steps.
-   Extreme duration: Finds records with a very long transition time compared to other transition records.
-   Extreme repetition: Finds records with a very high number of arc repetitions compared to other records on the same arc.
-   Slow transition: Identifies situations where there is a cluster of records with similar durations, and this cluster has a higher average duration compared to other group of records. This detector also offers a breakdown of the significance of the identified cluster, providing further insights into the root cause.

</td></tr><tr><td>

Category

</td><td>

Category for this finding definition.-   Quality
-   Automation
-   Conformance
-   Performance

</td></tr><tr><td>

Field

</td><td>

A field on which the finding definition is used.

</td></tr><tr><td>

Active

</td><td>

Whether the finding definition is active.

</td></tr><tr><td>

Process Configuration

</td><td>

Name of the process table that you have selected to create the finding definition for.

</td></tr><tr><td>

Table

</td><td>

Name of the table. This field is non-editable.

</td></tr><tr><td>

Select impacted KPIs

</td><td>

Select the KPIs most likely impacted by the findings. Choosing the affected KPIs enables you to assess the business impact. You can view the KPI-related findings in the insights panel of the Process Mining workspace.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)

