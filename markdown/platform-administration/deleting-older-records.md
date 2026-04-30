---
title: Deleting older or unwanted records
description: Delete older, expired, or unwanted records from tables automatically.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Managing the growth of data on your instance, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Deleting older or unwanted records

Delete older, expired, or unwanted records from tables automatically.

Delete older, inactive records in core tables such as the Task \[task\] table and records in custom tables that you create on the ServiceNow AI Platform using table cleanup rules.

There are several table cleanup rules included in the base system by default.

-   You can view a list of all the table cleaner rules in the Auto Flush \[sys\_auto\_flush\] table by entering `sys_auto_flush.list` in the filter navigator. The Auto Flush table displays rules for base system tables and their corresponding record ages.
-   You can view a list of table cleaner rules defined on a single table by navigating to **All** &gt; **Data Management Policies** and selecting the data management policy record for the table, if it exists. The system automatically creates a data management policy record for any table that has an archive rule or table cleaner rule.

## Slow rule handling

The table cleaner scheduled job runs once per hour \(by default\). When the table cleaner job runs, each table cleaner rule runs several queries as part of the process. If there's no index on a rule's match field or on significant portions of its condition, rule processing can be slow because its queries are running inefficiently on large amounts of data.

If a table cleaner rule has a query that takes longer than 30 seconds to complete, the entire table cleaner job is stopped. By default, table cleaner waits two days before including that rule in the table cleaner job again, which enables the table cleaner job to run without disruption in the meantime. You can configure the duration of the waiting period by adding a system property. See [Table cleaner properties](../reference/table-cleaner-properties.md).

## Disabling table cleanup

You can prevent an administrator from creating a table cleanup rule or running the table cleaner on a specific table by adding the Disable Table Cleaner attribute to the table's dictionary record. Some internal system tables have the Disable Table Cleaner attribute added by default.

## Table cleanup limitations

-   As of Xanadu patch 5, table cleaner rules defined in the Auto Flush \[sys\_auto\_flush\] table are supported for extension and shard tables. However, table cleaner rules aren't supported for tables configured with table rotation.

    When using the GlideTableCleaner scriptable directly, table cleaner rules aren’t supported for tables configured with table rotation or table extension. Some tables in your instance might have legacy table cleaner rules that were established before table rotation was enabled. These legacy rules can be safely ignored.

-   Performance depends on the size of the table and the conditions that you specify. For example, if you use a custom column without an index in a large table, performance is severely degraded. Performance also depends on the number of rows to be deleted.
-   Table cleaner spends a maximum of 20 minutes to delete records from a single table. If queries are slow, the volume of records deleted in the 20-minute period may be small.
-   Table cleaner doesn't call `DBDelete.setWorkflow()`. This means `DBDelete` objects run with `workflow=false` \(false is the default value for a Java Boolean\). As a result, business rules, workflows, and flows that you expected to trigger on record deletion won’t trigger in the context of table cleaner. This is important to consider if you have business logic that depends on this type of functionality.

-   **[Create a table cleanup rule](../task/activate-table-cleanup.md)**  
Define the criteria for deleting unwanted records in a table cleanup rule.

**Parent Topic:**[Managing the growth of data on your instance](data-management-policies.md)

