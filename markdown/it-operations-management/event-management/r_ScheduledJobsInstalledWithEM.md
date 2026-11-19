---
title: Scheduled jobs installed with Event Management
description: List of scheduled jobs that are provided with Event Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/r\_ScheduledJobsInstalledWithEM.html
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Scheduled jobs installed with Event Management

List of scheduled jobs that are provided with Event Management.

To review the list of scheduled jobs, navigate to **System Scheduler** &gt; **Scheduled Jobs**. Event Management adds the following scheduled jobs.

<table id="table_xc3_dbt_x5"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event Management — Connector execution job

</td><td>

Compares current time with time when active connector instances were last run and sets relevant connectors to execute. Runs every 10 seconds.

</td></tr><tr><td>

Event Management — Handle Impact Stuck Service

</td><td>

Releases stuck services and marks them as requiring rebuilding in the Impact Changes table to rebuild the impact tree. Runs every 2 minutes, 31 seconds.

</td></tr><tr><td>

Event Management — Impact Calculator Trigger

</td><td>

Trigger the impact calculation. The Event Management dashboard and impact tree are refreshed using the calculated figures.Runs every 6 seconds.

</td></tr><tr><td>

Event Management — Impact Topology Consumer

</td><td>

Consumes topology changes and marks the related services as ‘require rebuilding’ in the Impact Changes table to rebuild their impact trees.Runs every 19 seconds.

</td></tr><tr><td>

Event Management — Update stuck connectors

</td><td>

Release connector instances that are stuck. Runs every 2 minutes.

</td></tr><tr><td>

Event Management — Alert Priority Queue

</td><td>

Calculate [alert priority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/alert-priority.md). Two Alert Priority Queue jobs are active and available and can be run multi-thread. Runs every minute.

</td></tr><tr><td>

Event Management — Auto Close Alerts

</td><td>

Alerts that are idle longer than 7 days \(default time period\) are closed. Modify the default using the `evt_mgmt.alert_auto_close_interval` property. Runs every 10 minutes.

</td></tr><tr><td>

Event Management — Calculate Alert Priority Grouping

</td><td>

Runs and calculates the priority groups: urgent, high, moderate and low for the alerts according to the highest and lowest priority score in the system.Runs every 30 minutes.

</td></tr><tr><td>

Event Management — Close Flapping Alerts

</td><td>

Close flapping alerts. Runs every 5 minutes.

</td></tr><tr><td>

Event Management — Close Threshold Alerts

</td><td>

Close threshold alerts. Runs every 2 minutes.

</td></tr><tr><td>

Event Management — Evaluate Scoped Alert Rules Management0

</td><td rowspan="2">

Execute alert management rules. Two separate jobs run to ease the load on the system.Runs every 11 seconds.

</td></tr><tr><td>

Event Management — Evaluate Scoped Alert Rules Management1

</td></tr><tr><td>

Event Management — Filter Services for Impact - Queue Handler

</td><td>

Process changes from em\_impact\_inclusion\_class and em\_impact\_filter\_service.Runs every minute.

</td></tr><tr><td>

Event Management — Impact Tree Builder

</td><td>

Handles all services with changes from the em\_impact\_changes table and rebuilds their impact trees.Runs every 11 seconds.

</td></tr><tr><td>

Event Management — Insert Health Monitor

</td><td>

Job to produce the **ServiceNow Event Management** application services. Runs once every hour.

</td></tr><tr><td>

Event Management — Maintenance Calculator

</td><td>

Calculate the maintenance for CIs. Runs every minute.

</td></tr><tr><td>

Event Management — Node Count

</td><td>

Calculate [license usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/license-usage.md). Runs once every hour.

</td></tr><tr><td>

Event Management — Populate Impacted Services Table

</td><td>

Scan cmdb\_ci\_service\_auto and copy all services to em\_impacted\_service, along with all related classes to em\_impact\_inclusion\_class.Runs once after upgrade.

</td></tr><tr><td>

Event Management — Process Events

</td><td>

Job that runs and processes each Ready event \(apply event rule, mapping rule, and create or update alert\)Runs every 5 seconds.

</td></tr><tr><td>

Event Management — Process Metric Binding

</td><td>

Process metric binding.Runs every 5 seconds.

</td></tr><tr><td>

Event Management — Process Records in em\_extra\_data\_json

</td><td>

Creates events for log analytics anomalies.Runs every 13 seconds.

</td></tr><tr><td>

Event Management — Queue Connector Processor

</td><td>

Bi-directional functionality. Processes all pending alerts in the Update Queue and sends them to the MID Server. By default, this dequeue process is performed in batches of 1,000 alerts. Runs every 30 seconds.

</td></tr><tr><td>

Event Management — Recalculate Impact for Groups

</td><td>

By default, this job is not active. Can be run on demand to correct the impact on service groups.Runs on demand.

</td></tr><tr><td>

Event Management — Recover Stuck Events

</td><td>

Handle all events that are in queued state and switch back to Ready to handle events from the beginning.Runs at system startup.

</td></tr><tr><td>

Event Management — Update Health Monitor

</td><td>

Update the **ServiceNow Event Management** application services. Runs once every hour.

</td></tr><tr><td>

Event Management — Update SLA Configuration Result

</td><td>

Synchronizes the CIs that match the SLA configuration filter with the Event Management SLA \[em\_ci\_severity\_task\] table. Runs every 10 minutes.

</td></tr><tr><td>

Event Management — Update SLA Severity

</td><td>

Updates Event Management SLA \[em\_ci\_severity\_task\] table with the new severity. Runs once every minute.

</td></tr><tr><td>

Event Management — Convert IT Service

</td><td>

Run this property on demand to convert manual services to application services.Runs every 30 minutes.

</td></tr><tr><td>

Event Management – Collect xmlstats

</td><td>

Collect event processing statistics.

 Runs once every minute.

</td></tr><tr><td>

Event Management — Impact Calculator for Alert Groups and SLA

</td><td>

Calculates the effect of alerts on alert group services.

</td></tr><tr><td>

Event Management — Manual Impact Calculator Trigger

</td><td>

Manually trigger of Impact Calculation on all operational Services.

</td></tr><tr><td>

4x Event Management — Impact Calculator for BS\_0

</td><td rowspan="4">

Calculates the impact of alerts on application services, and builds the impact tree on the Event Management dashboard. Four separate jobs run to ease the load on the system.

</td></tr><tr><td>

4x Event Management — Impact Calculator for BS\_1

</td></tr><tr><td>

4x Event Management — Impact Calculator for BS\_2

</td></tr><tr><td>

4x Event Management — Impact Calculator for BS\_3

</td></tr><tr><td>

Event Management — Backfill Alert History table

</td><td>

Locates redundant records in the em\_alert\_history table and cancels them.

</td></tr><tr><td>

Event Management — Backfill Impact Status table

</td><td>

Locates redundant records in the em\_impact\_status table and cancels them.

</td></tr><tr><td>

Event Management — Impact for Groups

</td><td>

Calculates the impact of alerts on service groups.

</td></tr><tr><td>

Event Management — Clean Alert History Table

</td><td>

Cleans the Alert History \(em\_alert\_history\) table by removing records more than 90 days old.You can customize the amount of time after which alerts are removed by configuring **evt\_mgmt.impact\_calculation.cleanup\_age\_seconds.em\_alert\_history** in the sys\_properties.list table.

</td></tr><tr><td>

Event Management — Clean Impact Status Table

</td><td>

Cleans the Impact Status \(em\_impact\_status\) table by removing records more than 90 days old.You can customize the amount of time after which alerts are removed by configuring **evt\_mgmt.impact\_calculation.cleanup\_age\_seconds.em\_impact\_status** in the sys\_properties.list table.

</td></tr></tbody>
</table>Event Management adds the following scheduled jobs to support alert aggregation and RCA.

|Name|Description|
|----|-----------|
|Service Analytics Purge Old Observation Data — Daily|Cleans the staging data.|
|Service Analytics Prepare RCA Learner Input Data — Daily|Prepares RCA input data. Stores and probes MID Server to learn statistical information about alerts.|
|Service Analytics group alerts using RCA/Alert Aggregation|Applies RCA and alert aggregation to open alerts and prepares automated alert groups.|
|Service Analytics Alert Aggregation Learner — Daily|Learns information about existing alerts and groups new open alerts.|
|Service Analytics RCA Configuration|Configures root cause analysis.|
|Service Analytics Check File System Space on Analytics MID — Daily|Checks disk usage on the dedicated MID Server, and generates an event if it exceeds the threshold set in the **sa\_analytics.rca.mid\_max\_allowed\_space** property.|
|Service Analytics Gather Value Report Data — Daily|Gathers data for the Value Report.|
|Service Analytics — Update virtual alerts for aggregation groups|Update the virtual alerts that were created to represent alert aggregation groups, with any changes to alerts belonging to that group. Runs every minute.|
|Service Analytics Attribute Populator for Historical Alerts|Populate attributes used in feature identifier for historical alert data using event rules. Runs on demand.|
|Event Management - Analytics Alert Syncer|Gathers alert data that is used by grouping job.|

**Parent Topic:**[Event Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-management-reference.md)

