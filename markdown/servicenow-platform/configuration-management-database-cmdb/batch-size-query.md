---
title: Batch size for CMDB Query Builder queries
description: In a base system, a global batch size of 100 is allocated for every Query Builder query run. If needed, you can use a system property to override the default global batch size, or optimize the batch size value per saved query.Configure a custom batch size for a CMDB Query Builder saved query that takes a long time to complete or that times out. A custom batch size overrides the global batch size in the base system and the value of the glide.cmdb.query.batch.size system property.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Batch size for CMDB Query Builder queries

In a base system, a global batch size of 100 is allocated for every Query Builder query run. If needed, you can use a system property to override the default global batch size, or optimize the batch size value per saved query.

Queries can differ widely as they can be configured to query a wide variety of classes. Therefore, the batch size in the base system might not be optimal for every query, and some queries might time out or take a long time to complete. The optimal batch size for running queries depends on system load such as amount of data and number of relationships in your system. Contact Support for assistance in calculating the batch size for your query.

Batch size is applicable and behaves the same in all query run scenarios, regardless of how the run was initiated:

-   Query Builder user interface \(ad hoc or saved query\)
-   Query Builder Scriptable API
-   Scheduled jobs
-   [CMDB groups](cmdb-groups.md#)

The batch size for query runs is allocated in the following priority order:

1.  The value in the **Execution Batch Size** field in the Saved Queries table, for a specific saved query. If set, this value applies only to the saved query, and has priority over the global value of 100 and the value of the [glide.cmdb.query.batch\_size](../reference/cmdb-querybldr-sysproprties.md) system property.
2.  The value of the system property [glide.cmdb.query.batch\_size](../reference/cmdb-querybldr-sysproprties.md), if exists, determines globally the batch size that is allocated to all query runs. If you add and set this property, the value applies to all queries, other than saved queries with **Execution Batch Size** value set.
3.  A global value of 100, if the previous two options are not configured.

## Modifying batch size for queries

If you are experiencing performance problems when running queries, you can modify the batch size value:

-   Globally for all queries: By adding \(if necessary\) and setting the value of the system property [glide.cmdb.query.batch\_size](../reference/cmdb-querybldr-sysproprties.md).
-   Per saved query: [Set batch size for a specific saved query](batch-size-query.md#).

## Set batch size for a specific saved query

Configure a custom batch size for a CMDB Query Builder saved query that takes a long time to complete or that times out. A custom batch size overrides the global batch size in the base system and the value of the **glide.cmdb.query.batch.size** system property.

### Before you begin

Role required: sn\_cmdb\_admin or admin

### About this task

Contact Support for assistance in calculating the batch size for your query.

### Procedure

1.  In the Filter navigator, enter `qb_saved_query.list` and press Enter to navigate to the Saved Queries table.

2.  In the Saved Queries list view, locate the saved query for which you want to change batch size.

3.  Set or modify the value in the **Execution Batch Size** field.

    Set the value to be greater than the global value in the [glide.cmdb.query.batch.size](../reference/cmdb-querybldr-sysproprties.md) property, or increase any existing value.


