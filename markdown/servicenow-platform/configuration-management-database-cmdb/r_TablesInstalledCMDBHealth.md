---
title: Components installed with CMDB Health
description: Several types of components are installed with CMDB Health \(included in the com.snc.cmdb plugin\), such as tables, properties, and scheduled jobs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with CMDB Health

Several types of components are installed with CMDB Health \(included in the com.snc.cmdb plugin\), such as tables, properties, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Properties installed

<table id="table_ocn_1rn_3xb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.cmdb.services\_hierarchy\_limit

</td><td>

Maximum number of service CIs that can appear in the CMDB service dashboard. This limit applies to any child class of the Service Instance \[cmdb\_ci\_service\_auto\] class.

 -   Type: integer
-   Default: 10,000
-   Range: 0-100,000
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.
-   Learn more: [View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

</td></tr><tr><td>

glide.cmdb.services\_query\_limit

</td><td>

Maximum number of application services \(any class extending the Service \[cmdb\_ci\_service\] class\) that can be processed for the Service View of the CMDB Health Dashboard. Use this property to manage performance when there are large numbers of application services to process.

 -   Type: integer
-   Default: 1,000
-   Range: 1-10,000 \(If set lower than 1, defaults to 1\)
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.
-   Learn more: [View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

</td></tr><tr><td>

glide.cmdb.service\_associated\_ci\_query\_limit

</td><td>

Maximum number of CIs associated with application services \(any class extending the \[cmdb\_ci\_service\] class\) that can be processed for the Service View of the CMDB Health Dashboard. Use this property to manage performance when there are large numbers of such CIs to process.

 -   Type: integer
-   Default: 1,000
-   Range: 1-10,000 \(If set lower than 1, defaults to 1\)
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.
-   Learn more: [View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|CMDB Health Dashboard - Completeness Score Calculation|Script for calculating the completeness KPI of CMDB health.|
|CMDB Health Dashboard - Compliance Score Calculation|Script for calculating the compliance KPI of CMDB health.|
|CMDB Health Dashboard - Correctness Score Calculation|Script for calculating the correctness KPI of CMDB health.|
|CMDB Health Dashboard - Relationship Score Calculation|Script for calculating the CI relationships KPI of CMDB health.|
|CMDB Health Dashboard - Relationship Compliance Processor|Script for calculating compliance of relationships with suggested relationships, and with hosting and containment rules.|
|Add Identifier Fields In Recommended Rules|Sets all criterion attributes from all active identifier entries from all active identification rules, as recommended fields. These added recommended fields are then checked by the CMDB Health Dashboard - Completeness Score Calculation scheduled job when evaluating the recommended health metric.|
|Remove Identifier Fields In Recommended Rules|Identifies any recommended field that is a criterion attribute in any active identifier entry in any active identification rule. Then removes the recommended setting for that field.|

## Tables installed

<table id="table_nbl_m32_d2b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Health Metric\[cmdb\_health\_metric\]

</td><td>

Details such as if a KPI or metric is enabled, maximum failure threshold, and other settings for all CMDB Health KPIs and metrics.

</td></tr><tr><td>

CMDB Health Result\[cmdb\_health\_result\]

</td><td>

Results from the most recent CMDB Health processing cycle.

</td></tr><tr><td>

CMDB Health Scorecard \[cmdb\_health\_scorecard\]

</td><td>

Current and historic health scores. Status of historic score records is 'Historic', and of latest score records is 'Complete’.

</td></tr><tr><td>

CMDB Health Orphan Rule \[cmdb\_health\_orphan\_rule\]

</td><td>

Rules for calculating orphan records per class.

</td></tr><tr><td>

CMDB Recommended Fields \[cmdb\_recommended\_fields\]

</td><td>

Recommended fields per class.

</td></tr><tr><td>

CMDB Health Metric Status \[cmdb\_health\_metric\_status\]

</td><td>

Internal table that tracks the status of each KPI and metric that is being processed. Includes status, processing time, and processing start date. State for a KPI or metric changes from 'In Progress' to either of:

-   Complete
-   MaxFailures
-   Daily Processing Time Out

 Processing of a timed out KPI or metric continues on the following day.

</td></tr><tr><td>

CMDB Health Processor Status\[cmdb\_health\_processor\_status\]

</td><td>

Internal table that tracks the processing progress of each KPI and metric. Contains a list of tables that are processed for each KPI and metric, and processing status. Classes are processed sequentially, changing status from Draft -&gt; In Progress -&gt; Complete.

</td></tr><tr><td>

CMDB Relationship All Rules Health Results\[cmdb\_health\_result\_rel\_all\]

</td><td>

Stores results about relationship health, to be used by the All Relationships report.

</td></tr></tbody>
</table>