---
title: Tables installed with Event Management
description: Tables that are provided when Event Management is activated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/event-management/r\_TblsinstldwithEventMgmt.html
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Tables installed with Event Management

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
</table>**Parent Topic:**[Event Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/event-management/event-management-reference.md)

