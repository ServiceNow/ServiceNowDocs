---
title: Components related to CMDB 360
description: Several types of components are related to CMDB 360 \(included in the com.snc.cmdb plugin\), such as tables and properties.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [CMDB 360/Multisource CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components related to CMDB 360

Several types of components are related to CMDB 360 \(included in the com.snc.cmdb plugin\), such as tables and properties.

## Properties

Open the CMDB 360 Properties page by navigating to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**. You can hover over the '?' icon for a property, to show property names.

You must have the cmdb\_ms\_admin role to modify property values.

<table id="table_cny_5y4_ts"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.identification\_engine.multisource\_enabled

</td><td>

Enables CMDB 360.

 -   Type: true \| false
-   Default value: false
-   Location: CMDB 360 Properties page

</td></tr><tr><td>

glide.identification\_engine.multisource\_cmdb\_ci\_enabled​

</td><td>

Enables capturing CMDB 360 data for CIs from CMDB classes \(derived from the cmdb\_ci class\).

 -   Type: true \| false
-   Default value: true
-   Location: CMDB 360 Properties page

</td></tr><tr><td>

glide.identification\_engine.multisource\_non\_cmdb\_ci\_enabled

</td><td>

Enables capturing CMDB 360 data for CIs from non-CMDB classes \(not derived from the cmdb\_ci class\). For example, the Serial Number \[cmdb\_serial\_number\] class, or the Software instance \[cmdb\_software\_instance\] class.

 -   Type: true \| false
-   Default value: false
-   Location: CMDB 360 Properties page

</td></tr><tr><td>

glide.identification\_engine.multisource.query.batch.limit​

</td><td>

Max number of items to show per query results page, in the CMDB 360 Report Builder. Changing the value of this property, might affect performance when running a query.

 -   Type: numeric
-   Default value: 100
-   Location: CMDB 360 Properties page

</td></tr><tr><td>

glide.identification\_engine.multisource.query.max.limit​

</td><td>

Max number of query results to show when you click **Load All Results** in the CMDB 360 Report Builder. Changing the value of this property, might affect performance when running a query.

 -   Type: numeric
-   Default value: 10000
-   Location: CMDB 360 Properties page

</td></tr><tr><td>

glide.identification\_engine.multisource.recompute.max.ci.limit

</td><td>

Max number of CIs that can be included in a CMDB 360 recompute operation.

 -   Type: numeric
-   Default value: 100000
-   Location: CMDB 360 Properties page

</td></tr><tr><td>

glide.cmdb.logger.source.cmdb\_multisource​

</td><td>

Enable logging for CMDB 360. CMDB 360 logs are stored in the Log \[syslog\] table with **source** set to "cmdb\_multisource".

 -   Type: string
-   Values: info, warn, error, debug, or debugVerbose
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.

</td></tr><tr><td>

sn\_cmdb\_ws.ms.calculate\_cmdb\_only

</td><td>

Limits the scope of data in the [Discovery sources tile in the CMDB 360 dashboard](../concept/cmdb360-exp-cmdb-workspace.md), to CMDB classes only \(derived from the cmdb\_ci class\).

 -   Type: true \| false
-   Default value: true
-   Values:
    -   True: Include data only from CMDB classes.
    -   False: Include data from CMDB and non-CMDB tables.
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

sn\_cmdb\_ws.ms.report\_class\_ci\_count\_max\_threshold

</td><td>

Threshold number of multisource records that when exceeded for a class, CMDB 360 Coverage charts in CMDB Workspaceand in Service Graph Workspace stop populating data for that class \(CMDB or non-CMDB tables\).

 When the specified threshold number is reached for a class, the system creates a record in the CMDB 360 Analytics Skipped Class \[sn\_cmdb\_ws\_ms\_skip\_class\] table causing that class to be skipped in future job runs.

 **Note:** Managing class inclusion in the Coverage charts, by using this system property and the CMDB 360 Analytics Skipped Class \[sn\_cmdb\_ws\_ms\_skip\_class\] table, can greatly decrease or increase performance of the Coverage chart job.

 -   Type: numeric
-   Default value: 10 million
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   Learn more: [CMDB 360 experience in CMDB Workspace and in Service Graph Workspace](../concept/cmdb360-exp-cmdb-workspace.md)

</td></tr></tbody>
</table>## Tables

<table id="table_ugt_x3x_ft"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB 360 Data\[cmdb\_multisource\_data\]

</td><td>

CMDB 360 data store. Contains the raw data sent by all discovery sources.

</td></tr><tr><td>

CMDB MultiSource Column Metadata\[cmdb\_multisource\_column\_metadata\]

</td><td>

Mapping of attributes for each class to floatable columns​. Used to improves performance of queries that involve high volumes of data​.

</td></tr><tr><td>

CMDB Multisource Queries \[cmdb\_multisource\_query\]

</td><td>

CMDB 360 query definitions created by the user in CMDB Workspaceor in Service Graph Workspace.

</td></tr><tr><td>

Query Status\[cmdb\_multisource\_query\_status\]

</td><td>

State of execution, of queries created in CMDB Workspaceor in Service Graph Workspace.

</td></tr><tr><td>

CMDB Multisource Query Results\[cmdb\_multisource\_query\_result\]​ ​

</td><td>

Results for queries created in CMDB Workspaceor in Service Graph Workspace, configured with result type of CI records.​

</td></tr><tr><td>

CMDB Multisource Query Result Multisource Records \[cmdb\_multisource\_query\_result\_ms\_record\]

</td><td>

Results for queries created in CMDB Workspaceor in Service Graph Workspace, configured with result type of CMDB 360 records.

</td></tr><tr><td>

CMDB Multisource Query Result Discovery Sources \[cmdb\_multisource\_query\_result\_disco\_source\]​

</td><td>

Results for queries created in CMDB Workspaceor in Service Graph Workspace, configured with result type of Discovery source records.

</td></tr><tr><td>

CMDB MultiSource Recompute Task CIs\[cmdb\_multisource\_recomp\_task\_ci​\]

</td><td>

All CIs that are involved in a recompute operation.​

</td></tr><tr><td>

CMDB Multisource Recompute Tasks\[cmdb\_multisource\_recomp\_task​\]

</td><td>

Recomputation requests and progress status.

</td></tr><tr><td>

CMDB 360 denied classes\[cmdb\_multisource\_deny\_class\]

</td><td>

Classes that are excluded from CMDB 360 data collection and processing. For any class with an active record, there won't be any data in the CMDB 360 Data \[cmdb\_multisource\_data\] table.

</td></tr><tr><td>

CMDB 360 Analytics Skipped Class\[sn\_cmdb\_ws\_ms\_skip\_class\]

</td><td>

Internally used to store records of classes for which the threshold number of CMDB 360 records, as set in the **sn\_cmdb\_ws.ms.report\_class\_ci\_count\_max\_threshold** property, has exceeded. Classes in this table are excluded from the Coverage charts in CMDB Workspaceand in Service Graph Workspace.

 You can set the **Override class CI records population** column for an excluded class to 'true', to include it in Coverage charts future computations.

 **Note:** Managing class inclusion in the Coverage charts, by using this table and the **sn\_cmdb\_ws.ms.report\_class\_ci\_count\_max\_threshold** system property, can greatly decrease or increase performance of the Coverage chart job.

</td></tr></tbody>
</table>## Roles

|Role|Description|
|----|-----------|
|cmdb\_ms\_read|Can access and run a CMDB 360 query but can't create a query. Contains cmdb\_read role.|
|cmdb\_ms\_editor|Can create and run a query, has full read and write access, but can't do Recompute. Contains cmdb\_ms\_read role.|
|cmdb\_ms\_admin|Can create and run a query, and can modify CMDB 360 properties. Contains cmdb\_ms\_write role.|

