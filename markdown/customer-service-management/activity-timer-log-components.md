---
title: Activity timer log components
description: The activity timer log feature is available with the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\). This plugin adds user tables, user roles, UIB page properties, a script include, and a scheduled job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/activity-timer-log-components.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [Activity timer log, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Activity timer log components

The activity timer log feature is available with the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\). This plugin adds user tables, user roles, UIB page properties, a script include, and a scheduled job.

## Tables

The activity timer log feature adds the following tables.

|Table|Description|
|-----|-----------|
|Time Entry \[sn\_at\_time\_entry\]|Records the time that an agent spends working on case and interaction records. Each start and stop transaction has a time associated with it.|
|Time Entry Aggregated \[sn\_at\_time\_entry\_aggregated\]|Aggregates the data stored in the Time Entry table. This aggregation records the time spent per case, agent, and record type.|

|Field|Description|
|-----|-----------|
|Attributes|Attributes for the entry, such as the record state and short description.|
|Record|Record type and number.|
|Session|Session ID.|
|Source| |
|Table|The table that stores the record in the **Record** field.|
|Timer running|Start and stop times.|
|Timestamp|The timestamp for the start and stop times.|
|Transaction|The transaction ID for a start/stop pair.|
|User|The name or role of the user who worked on a record.|

|Field|Description|
|-----|-----------|
|User|The name or role of the user who worked on a record. This is a reference to the sys\_user table.|
|Record|Record number.|
|Record Type|Record type, such as case or interaction.|
|Short Description|Short description of the record.|
|Start Time|Time that the agent started working on the record.|
|End Time|Time that the agent stopped working on the record.|
|Total Time Logged|Total time that the user spent working on the record.|

## User roles

The activity timer log feature adds the following user roles:

-   sn\_at.admin
-   sn\_at.agent

## Script include

The `ActivityTimerAggregator` script include:

-   Runs every 24 hours and records all the transactions from the Timer Entries table.
-   Is invoked by the `Activity Timer Reporting Aggregator` scheduled job.
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

**activity\_timer**

</td><td>

Enables the activity timer component in the workspace.-   True: Activity timer is active.
-   False: Activity timer is inactive.

</td></tr><tr><td>

**activity\_timer\_custom\_tables**

</td><td>

Specifies custom tables for the activity timer log feature.

</td></tr><tr><td>

**activity\_timer\_case\_type\_exclusion**

</td><td>

Specifies case types excluded from the activity timer log feature.

</td></tr></tbody>
</table>