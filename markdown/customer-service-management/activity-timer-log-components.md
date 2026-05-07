---
title: Activity timer log components
description: The activity timer log feature is available with the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\). This plugin adds user tables, user roles, UIB page properties, a script include, and a scheduled job.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-22"
reading_time_minutes: 2
breadcrumb: [Activity timer log, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Activity timer log components

The activity timer log feature is available with the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\). This plugin adds user tables, user roles, UIB page properties, a script include, and a scheduled job.

## Tables

The activity timer log feature adds the following tables.

<table id="table_ynb_rsw_z3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time Entry\[sn\_at\_time\_entry\]

</td><td>

Records the time that an agent spends working on case and interaction records. Each start and stop transaction has a time associated with it.

</td></tr><tr><td>

Time Entry Aggregated\[sn\_at\_time\_entry\_aggregated\]

</td><td>

Aggregates the data stored in the Time Entry table. This aggregation records the time spent per case, agent, and record type.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Attributes|Shows the attributes for the entry, such as the record state and short description.|
|Record|Displays the record type and number.|
|Session|Displays the session ID.|
|Source| |
|Table|The table that stores the record in the **Record** field.|
|Timer running|Records the start and stop times.|
|Timestamp|The timestamp for the start and stop times.|
|Transaction|The transaction ID for a start/stop pair.|
|User|The name or the role of the user who worked on a record.|

|Field|Description|
|-----|-----------|
|End Time|The time that the agent stopped working on the record.|
|Record|Displays the record number.|
|Record Type|Displays the record type, such as case or interaction.|
|Short Description|The short description of the record.|
|Start Time|The time that the agent started working on the record.|
|Total Time Logged|The total time that the user spent working on the record.|
|User|The name or the role of the user who worked on a record.|

## User roles

The activity timer log feature adds the following user roles:

-   sn\_at.admin
-   sn\_at.agent

## Script include

The **ActivityTimerAggregator** script include:

-   Runs every 24 hours and records all the transactions from the Timer Entries table.
-   Is invoked by the **Activity Timer Reporting Aggregator** scheduled job.
-   For each record, calculates the time between each start and stop on the record.

## Scheduled job

The **Activity Timer Reporting Aggregator** scheduled job runs once every 24 hours and generates a report. It creates an aggregation of the records stored in the Time Entry table and stores this data in the Time Entry Aggregated table. The aggregated data is displayed in the agent's My Timelog list view.

## Page properties

The activity timer log feature adds the following UI Builder page properties:

<table id="table_d4c_1wd_cjc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

activity\_timer

</td><td>

Enables the activity timer component in the workspace.-   True: Activity timer is active.
-   False: Activity timer is inactive.

</td></tr><tr><td>

activity\_timer\_custom\_tables

</td><td>

Specifies custom tables for the activity timer log feature.

</td></tr><tr><td>

activity\_timer\_case\_type\_exclusion

</td><td>

Specifies case types excluded from the activity timer log feature.

</td></tr></tbody>
</table>