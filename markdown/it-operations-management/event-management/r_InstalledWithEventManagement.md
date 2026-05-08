---
title: Components installed with Event Management
description: Activating the Event Management \(com.glideapp.itom.snac\) plugin adds several roles, scheduled jobs, and tables.Roles used by the Event Management application.List of scheduled jobs that are provided with Event Management.Properties provide the metadata to identify the domain.Tables that are provided when Event Management is activated.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Components installed with Event Management

Activating the Event Management \(com.glideapp.itom.snac\) plugin adds several roles, scheduled jobs, and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

**Parent Topic:**[Event Management reference](event-management-reference.md)

## Roles installed with Event Management

Roles used by the Event Management application.

Event Management adds these roles.

<table id="table_dmp_vhb_mt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Event Management Administrator\[evt\_mgmt\_admin\]

</td><td>

Has read and write access to all Event Management features to configure Event Management.**Note:** Exercise caution with the evt\_mgmt\_admin role, as it can be elevated to the admin role. A user with the evt\_mgmt\_admin role has the ability to add and modify scripts that run on a global scope. Ensure proper access control. With this role, the user can create and/or update the following scripts:

-   Alert correlation rules
-   Alert management rules
-   Maintenance rules
-   Advanced scripts
-   Event field mapping
-   Pre- and post-binding scripts

</td><td>

-   evt\_mgmt\_user
-   template\_editor\_global

</td></tr><tr><td>

Event Management Operator\[evt\_mgmt\_operator\]

</td><td>

In addition to the evt\_mgmt\_user permissions, can also activate operations on alerts such as acknowledge, close, open incident, and run remediations.

</td><td>

evt\_mgmt\_user

</td></tr><tr><td>

Event Management User\[evt\_mgmt\_user\]

</td><td>

Has read access to all Event Management features. Has the itil role to be able to manage incidents that are created from alerts.

</td><td>

itil

</td></tr><tr><td>

Event Management Integrator\[evt\_mgmt\_integration\]

</td><td>

Has create access to the Event \[em\_event\] and Registered Nodes \[em\_registered\_nodes\] tables to integrate with external event sources.

</td><td>

 

</td></tr></tbody>
</table>## Scheduled jobs installed with Event Management

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

Calculate [alert priority](../concept/alert-priority.md). Two Alert Priority Queue jobs are active and available and can be run multi-thread. Runs every minute.

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

Calculate [license usage](../task/license-usage.md). Runs once every hour.

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

Event Management — Collect xmlstats

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

## Properties for personalizing domain separation for Event Management connectors

Properties provide the metadata to identify the domain.

You can change the values if you want to use any other table or fields for domain identification but make sure that the table is domain separated.

**Note:** When personalizing domain separation for event management connectors, all the properties can be overridden at the connector level as well.

There are three caches maintained for personalizing domain separation \(main, user\_access, missing\_domain\). You can create a few system properties to control them.

<table id="table_e5g_lsy_nxb"><thead><tr><th align="left">

Property

</th><th>

Description

</th></tr></thead><thead><tr><th align="left">

Property

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

evt\_mgmt. connector\_domain\_info\_table\_name

</td><td>

The table where you store domain information for personalizing domain separation.

-   **Type**: string
-   **Default value**: core\_company

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_info\_column\_name

</td><td>

The field name in the table to identify the provided domain for personalizing domain separation.-   **Type**: string
-   **Default value**: name

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_id\_column\_name

</td><td>

The field to get domain ID from for personalizing domain separation.-   **Type**: string
-   **Default value**: sys\_domain

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_path\_column\_name

</td><td>

The field to get the domain path from for personalizing domain separation.-   **Type**: string
-   **Default value**: sys\_domain\_path

</td></tr></tbody><tbody><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_cache\_expire\_in\_seconds

</td><td>

For personalizing domain separation, if you don’t want your main cache to expire every week.

</td></tr><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_user\_access\_on\_domain\_cache\_size

</td><td>

For personalizing domain separation, if you want to increase the size of the user access cache.

</td></tr><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_missing\_domain\_cache\_expire\_in\_seconds

</td><td>

For personalizing domain separation, if you want to increase the expire time for cache storing information regarding the missing domain.

</td></tr><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_cache\_size

</td><td>

For personalizing domain separation, if you need more main cache size for storing domain information.

</td></tr></tbody>
</table>## Tables installed with Event Management

Tables that are provided when Event Management is activated.

Event Management adds these tables.

<table id="table_trz_yx4_w4"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert \[em\_alert\]

</td><td>

Alerts that Event Management manage.

</td></tr><tr><td>

Alert Correlation Rule \[em\_alert\_correlation\_rule\]

</td><td>

Rules specifying primary and secondary correlated alerts.

</td></tr><tr><td>

Alert Aggregation Group Alerts\[em\_agg\_group\_alert\]

</td><td>

Stores alerts associated with aggregated alert groups.

</td></tr><tr><td>

Alert Aggregation Group\[em\_agg\_group\]

</td><td>

Relationships between aggregated groups and primary alerts.

</td></tr><tr><td>

Alerts History\[em\_alert\_history\]

</td><td>

History of alerts. Used for impact calculation.

</td></tr><tr><td>

Alert Rule \[em\_alert\_rule\]

</td><td>

Mappings of alert fields to the Incident \[incident\] table.

</td></tr><tr><td>

Alert Template\[em\_alert\_template\]

</td><td>

Alert templates. This table extends the Template \[sys\_template\] table.

</td></tr><tr><td>

Event Management SLA \[em\_ci\_severity\_task\]

</td><td>

Event Management SLA tasks for CIs and services.

</td></tr><tr><td>

Connector Definition \[em\_connector\_definition\]

</td><td>

Settings for gathering events from external event sources.

</td></tr><tr><td>

Connector Instance \[em\_connector\_instance\]

</td><td>

Connection details for external event sources.

</td></tr><tr><td>

MID Server to Connector Instance\[em\_connector\_instance\_to\_mid\]

</td><td>

Mappings of MID Servers to connector instances.

</td></tr><tr><td>

Event Management License Usage\[em\_unique\_nodes\]

</td><td>

When events are received by ITOM AIOps, an entry is added or updated in this table based on the monitored target specified in the received message. The entry links to its corresponding CMDB CI. If none is found, the entry is assigned **Type = Unknown**.

</td></tr><tr><td>

Event \[em\_event\]

</td><td>

Events received by Event Management.

</td></tr><tr><td>

Event Filter \[em\_event\_filter\]

</td><td>

Storage for defined event filters.

</td></tr><tr><td>

Event Match Rule \[em\_match\_rule\]

</td><td>

Updated events for alert processing. Used by event rules.

</td></tr><tr><td>

Event Match Field \[em\_match\_field\]

</td><td>

Mappings of event fields to alert fields. Simple mapping. Used by Event Rules.

</td></tr><tr><td>

Event Compose Field\[em\_compose\_field\]

</td><td>

Mappings of event fields to alert fields. Composite mapping. Used by Event Rules.

</td></tr><tr><td>

Event Mapping Rule \[em\_mapping\_rule\]

</td><td>

Updated event fields for alert processing.

</td></tr><tr><td>

Event Processing Statistics \[em\_event\_stats\]

</td><td>

Statistics on Event Management performance.

</td></tr><tr><td>

Event Type \[em\_event\_type\]

</td><td>

Event types.

</td></tr><tr><td>

Task Template \[em\_incident\_template\]

</td><td>

Templates that define how to populate new tasks. For example, how fields of an incident that is being created from an alert, must be populated. This table extends the Template \[sys\_template\] table.

</td></tr><tr><td>

Registered Nodes \[em\_registered\_nodes\]

</td><td>

Registered nodes data.

</td></tr><tr><td>

Threshold Rule \[em\_threshold\_rule\]

</td><td>

Alert threshold rules.

</td></tr><tr><td>

Binding Device Map \[Em\_binding\_device\_map\]

</td><td>

Event binding to network paths and storage paths.

</td></tr><tr><td>

Process to CI Type Mappings \[Em\_binding\_process\_map\]

</td><td>

Event binding to specific processes.

</td></tr><tr><td>

CI Remediation \[em\_ci\_remediation\]

</td><td>

Remediation rule definitions.

</td></tr><tr><td>

Impact Graph \[em\_impact\_graph\]

</td><td>

Impact tree of CIs containing CI hierarchy and impact rules to be used for impact calculation.

</td></tr><tr><td>

Impact Graph History \[em\_impact\_graph\_history\]

</td><td>

History of changes in impact tree.

</td></tr><tr><td>

Impact Rule Definitions \[em\_impact\_rule\_definition\]

</td><td>

Definition of rules used for impact calculation.

</td></tr><tr><td>

Impact Rule instance \[em\_impact\_rule\]

</td><td>

Rules based on impact rule definitions.

</td></tr><tr><td>

Impact Inclusion Classes\[em\_impact\_inclusion\_class\]

</td><td>

Specifies the classes to be used for impact calculation.

</td></tr><tr><td>

Impact Filter Services\[em\_impact\_filter\_service\]

</td><td>

Specifies services to be included or excluded from impact calculation.

</td></tr><tr><td>

Infrastructure Relations \[em\_impact\_infra\_rel\_def\]

</td><td>

Child-parent pairs or CI types. CIs matching these definitions are added to impact trees.

</td></tr><tr><td>

Impact Maintenance CIs \[em\_impact\_maint\_ci\]

</td><td>

CIs that are in maintenance and therefore are excluded from impact calculation.

</td></tr><tr><td>

Impact Status \[em\_impact\_status\]

</td><td>

Calculated status of CIs and services to be displayed in the dashboard and service maps for dynamic CI groups.

</td></tr><tr><td>

SLA Configuration \[em\_sla\_configuration\]

</td><td>

SLA configuration records that identify the CIs that SLAs can run on.

</td></tr><tr><td>

Service Analytics Metric Type Registration\[sa\_metric\_registration\]

</td><td>

Source registration details for processing raw data.

</td></tr><tr><td>

Health monitor scripts\[em\_monitor\_scripts\]

</td><td>

These scripts determine how to monitor or check, for example, when using the Connectors Monitor script. You can create customized script to monitor a device or an entity. The scripts provided with the base instance are:-   Check delay in event processing
-   Connectors Monitor
-   Get Event Processing state
-   MID Server Threshold Alerts

</td></tr><tr><td>

Monitoring configuration\[em\_monitor\_conf\]

</td><td>

Use this table to configure what to monitor according to the scripts that are listed.Configure how often to run each script. If a script has a threshold, it determines what alert severity to display. Threshold values are in units of minutes and specify the delay time. Navigate to **Event Management** &gt; **Settings** &gt; **Self-Health configuration** to see the list of Monitoring Configurations or to create a new one. Use this script to test Data Center Monitoring.

The scripts provided with the base instance are:-   Connector's idle state monitoring-monitor to verify whether any of the connectors was in idle state that surpassed the threshold \[in minutes\] that was configured.
-   Connectors Status- monitor to track the active status of the connectors.
-   Delay in event processing-monitor to track the duration \[in minutes\] of events that remained in 'ready' state and were not processed.
-   Event Processing job-monitors the state of the event processing jobs.
-   MID Server Threshold Alert-monitors MID Server health.

</td></tr><tr><td>

Monitoring Event Management Jobs\[em\_monitor\_jobs\_state\]

</td><td>

Monitor Event Management jobs by adding the relevant jobs to the table. **Note:** The following jobs are not monitored by this table:

-   Event Management - Process Events
-   Event Management - Impact Tree Builder
-   Event Management - Recover Stuck Events
-   Event Processing

</td></tr><tr><td>

Monitoring state\[em\_monitor\_state\]

</td><td>

Use this table to set the threshold for each connector. When there is a value above the threshold, an alert is generated.

</td></tr><tr><td>

EM XMLStats Data\[em\_xmlstats\_data\]

</td><td>

Self-health statistics and diagnostic details for Metric Intelligence and Event Management, which are used to produce the XMLStats page.

</td></tr></tbody>
</table>Event Management adds the following tables to support alert aggregation and RCA.

<table id="table_of5_yv5_vs"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SA RCA Status \[sa\_rca\_status\]

</td><td>

Information \(such as IDs\) for the latest messages that were sent to the ECC Queue for a service during RCA.

</td></tr><tr><td>

SA RCA Output\[sa\_rca\_output \]

</td><td>

RCA learner output data.

</td></tr><tr><td>

SA RCA Group\[sa\_rca\_group\]

</td><td>

Automated alert groups for the RCA query.

</td></tr><tr><td>

SA Analytics Alert Staging\[sa\_analytics\_alert \]

</td><td>

Staging table for alerts used for analytics.

</td></tr><tr><td>

SA RCA Input\[sa\_rca\_input\]

</td><td>

Input data for the RCA learner.

</td></tr><tr><td>

SA Analytics Status\[sa\_analytics\_status\]

</td><td>

Last run information to be used for alert aggregation and RCA.

</td></tr><tr><td>

SA RCA Group Alert\[sa\_rca\_group\_alert \]

</td><td>

Alerts associated with automated alert groups.

</td></tr><tr><td>

SA RCA Service Configuration Item Association\[sa\_rca\_svc\_ci\_assoc\]

</td><td>

Associations between CIs and services.

</td></tr><tr><td>

SA Alert Aggregation Learned Pattern \[sa\_agg\_pattern\]

</td><td>

Learned patterns from alert aggregation.

</td></tr><tr><td>

SA Alert Aggregation Learned Pattern Elements\[sa\_agg\_pattern\_element\]

</td><td>

CI/Metric Name pairs associated with learned patterns.

</td></tr><tr><td>

SA Alert Aggregation Query Group Patterns\[sa\_agg\_group\_pattern\]

</td><td>

Relationships between groups discovered in alert aggregation queries and patterns found in learning.

</td></tr><tr><td>

SA Alert Aggregation Query -- Staged \(Recent\) Alerts\[sa\_agg\_group\_alert\_staging\]

</td><td>

A staging table for alerts that have not yet been associated with any aggregated alert group.

</td></tr><tr><td>

SA Agg Pattern Attribute\[sa\_agg\_pattern\_attribute table\]

</td><td>

CI/alert attributes to be used for finding patterns for alert aggregation.

</td></tr><tr><td>

SA Alert Attribute Populator Status \[sa\_alert\_attribute\_populator\_status table\]

</td><td>

State and statistics for attribute populator job.

</td></tr><tr><td>

SA Alert Aggregation Learned Pattern Elements Pair wise Mutual Information and Joint Probability \[sa\_agg\_pattern\_element\_pair\]

</td><td>

Pairwise probabilities for pattern elements.

</td></tr><tr><td>

EM Agg Group Prediction\[em\_agg\_group\_prediction\]

</td><td>

Alert predictions for alert groups.

</td></tr></tbody>
</table>