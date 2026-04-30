---
title: Components installed with AIOps LEAP
description: Several types of components are installed with activation of the plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: reference
last_updated: "2025-04-25"
reading_time_minutes: 1
breadcrumb: [AIOps LEAP reference, AIOps Learning Enhanced Automation Playbook \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Components installed with AIOps LEAP

Several types of components are installed with activation of the  plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_rz5_1pw_cfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AIOps LEAP admin \[sn\_itom\_leap.leap\_admin\]

</td><td>

You have full control over AIOps LEAP capabilities, including the following:

-   Turn features on and off
-   Execute scheduled jobs
-   Manage AIOps LEAP tables and the AIOps LEAP Workspace
-   Generate and update resolution steps
-   Create and view problems and generate AIOps LEAP playbooks from automation opportunities \(AO\)

</td></tr><tr><td>

AIOps LEAP viewer \[sn\_itom\_leap.leap\_viewer\]

</td><td>

You can access and view data related to AIOps LEAP, including tables, the workspace, and problems originating from AOs.

</td></tr><tr><td>

AIOps LEAP agent \[sn\_itom\_leap.leap\_agent\]

</td><td>

You can access the AIOps LEAP menu from the Service Operations Workspace \(SOW\) and trigger AIOps LEAP executions directly from within SOW.

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Populate Record Metrics Aggregate Records|Runs once per day and populates LEAP aggregate metrics table by time periods.|
|Update Record Metrics Table with Calculated Metrics|Runs daily, calculates and updates the records in the LEAP Record Metrics table for all those records to which the metrics has not yet been calculated.|
|GAF- Run Offline Flow|Runs monthly to group the tasks using the task data provided in the skill config while activating the LEAP skill.|

## Tables installed

|Table|Description|
|-----|-----------|
|LEAP aggregate metrics|Contains metrics like cost savings, time savings, record count and so on for each time period. This data is used in the LEAP report page in the workspace.|
|LEAP feedback|Stores the feedback given by the agent to the playbooks that are run to fix the tasks.|
|LEAP GAF mapping|Maintains a map between the GAF groups and the published LEAPs to retain information in the subsequent GAF clustering runs.|
|LEAP group|Stores the LEAP group details like group description, resolution steps and whether the LEAP is automated or not.|
|LEAP group ranking|Maintains data like business impact, projected cost savings, problem record, status used in Automation Opportunities page in the workspace.|
|LEAP properties|Sets custom values to the properties that are used in AIOps LEAP.|
|LEAP record metrics|Maintains data that's used in Published LEAP page in the workspace. It contains calculated data like time saved, tickets resolved, rating trend etc.|

