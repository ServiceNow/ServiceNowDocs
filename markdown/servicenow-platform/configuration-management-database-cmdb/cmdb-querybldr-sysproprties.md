---
title: Property settings for CMDB Query Builder
description: Set property values to configure query processing.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Property settings for CMDB Query Builder

Set property values to configure query processing.

## Access and Role required

The admin role is required to view and edit Query Builder properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_y4d_htz_mhb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Limits the number of results for a scheduled query and in the results section in the Query Builder when you select **Load All Results**.glide.cmdb.query.max\_results\_limit

</td><td>

-   Type: integer
-   Default value: 10000
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**

</td></tr><tr><td>

Time limit \(in seconds\) for running one batch to get one batch of query results \(100 results\).glide.cmdb.query.batch\_time\_limit\_in\_sec

</td><td>

-   Type: integer
-   Default value: 300
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**

</td></tr><tr><td>

Time limit \(in seconds\) for running an entire query to get all results.glide.cmdb.query.query\_time\_limit\_in\_sec

</td><td>

-   Type: integer
-   Default value: 1800
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**

</td></tr><tr><td>

Exclude list of non-CMDB tables. The specified tables will not appear in the CMDB Query Builder when a user creates a query.glide.cmdb.query.non\_cmdb.black\_listed\_tables

</td><td>

-   Type: string
-   Default value: empty
-   Other values: Comma-separated list of table names \(not labels\). Can include '\*abc' to exclude all tables containing 'abc' in their table name.
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**

</td></tr><tr><td>

glide.cmdb.query.batch\_size

</td><td>

Batch size allocated globally when saved queries run.

 -   Type: integer
-   Default value: 100
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.

</td></tr><tr><td>

glide.cmdb.query.execution\_mode

</td><td>

Default execution engine to use when running a saved query when the query's execution mode isn't set \(Query Execution Mode is 'None'\). Used in combination with the **glide.cmdb.query.or\_execution\_mode** system property.

 -   Type: string
-   Values:
    -   v1: Use the legacy query execution engine.
    -   v2: Use an enhanced query execution engine which is designed for improved performance and scalability.
-   Default value: v2
-   Location: System Properties \[sys\_properties\] table.
-   Learn more: [Set execution mode for running a query](../task/config-query-builder-engine-mode.md)

</td></tr><tr><td>

glide.cmdb.query.or\_execution\_mode

</td><td>

Default execution engine to use, applying only to queries that contain at least one logical OR condition. Used in combination of the **glide.cmdb.query.execution\_mode** system property.

 -   Type: string
-   Values:
    -   v1: Use the legacy query execution engine.
    -   v2: Use an enhanced query execution engine which is designed for improved performance and scalability.
-   Default value: v2
-   Location: System Properties \[sys\_properties\] table.
-   Learn more: [Set execution mode for running a query](../task/config-query-builder-engine-mode.md)

</td></tr></tbody>
</table>