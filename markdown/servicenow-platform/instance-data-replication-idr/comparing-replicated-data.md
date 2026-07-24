---
title: Comparing replicated data between instances in Instance Data Replication
description: Find missing or mismatched records by comparing replication data between instances in Instance Data Replication \(IDR\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/instance-data-replication-idr/comparing-replicated-data.html
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Comparing replicated data between instances in Instance Data Replication

Find missing or mismatched records by comparing replication data between instances in Instance Data Replication \(IDR\).

IDR synchronizes data between a producer instance and one or more consumer instances. After you activate a producer replication set and subscribe at least one consumer, you can send existing records from the producer to the consumer by seeding records. After seeding is finished, IDR maintains data synchronization between the instances by replicating new and changed records from the producer to the consumer.

If an insert fails on the consumer or when producer and consumer records don’t match after replication, you can use the data comparison feature in IDR to find these records and reseed them from the producer to the consumer.

## Key benefits

-   Identify records missing from the consumer instance after seeding.
-   Identify mismatched records and view their differences.
-   Keep data synchronized between instances by reseeding records.

## Comparing transformed data

When comparing transformed data, note the following details:

-   The data comparison can return mixed results if records are added to a table on the producer and then a transformation replicates to a different table on the consumer instance.
-   Mapped fields with different field definitions are skipped. For example, if a field on the producer has a different column type or column length than the mapped field on the consumer, the field is skipped.
-   All fields that are modified by an adapter are skipped except for modifications made by the Task number adapter. For example, if a string is appended using the Concatenate String adapter, the data comparison can't undo the concatenation and compare the data using the original string, so the field is skipped.

## Compatibility

Beginning in the Washington DC release, you can compare replicated data in bidirectional replication sets, discrete replication sets, and replication sets with transformations configured on either the producer or the consumer.

When comparing data on different family releases, note the following compatibility options.

<table id="table_xxy_wtg_lzb"><thead><tr><th>

Data comparison

</th><th>

Producer

</th><th>

Consumer

</th><th>

Supported replication sets

</th></tr></thead><tbody><tr><td>

Producer to consumer

</td><td>

Washington DC or later

</td><td>

Utah and earlier

</td><td>

None

</td></tr><tr><td>

Producer to consumer

</td><td>

Washington DC or later

</td><td>

Vancouver

</td><td>

Supports unidirectional replication sets, but not the following:-   bidirectional replication sets
-   discrete replication sets
-   replication sets configured with transformations

</td></tr><tr><td>

Producer to consumer

</td><td>

Washington DC or later

</td><td>

Washington DC or later

</td><td>

All replication sets

</td></tr></tbody>
</table><table id="table_mt5_fs2_nzb"><thead><tr><th>

Data comparison

</th><th>

Consumer

</th><th>

Producer

</th><th>

Supported replication sets

</th></tr></thead><tbody><tr><td>

Consumer to producer

</td><td>

Washington DC or later

</td><td>

Utah and earlier

</td><td>

None

</td></tr><tr><td>

Consumer to producer

</td><td>

Washington DC or later

</td><td>

Vancouver

</td><td>

Supports bidirectional replication sets, but not the following:-   unidirectional replication sets
-   discrete replication sets
-   replication sets configured with transformations

</td></tr><tr><td>

Consumer to producer

</td><td>

Washington DC or later

</td><td>

Washington DC or later

</td><td>

All replication sets, but not unidirectional replication sets

</td></tr></tbody>
</table>## Limitations

-   Journal fields are excluded from the comparison due to the potential size of their content.
-   Sys Audit \[sys\_audit\] table records are excluded from the comparison.

-   **[Find missing or mismatched records in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/compare-replicated-data.md)**  
Find records missing from the consumer instance or mismatched records after data has been replicated by creating a data comparison request in Instance Data Replication \(IDR\).
-   **[Reseed missing or mismatched records in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/fix-replicated-data.md)**  
Synchronize data between instances by reseeding records missing from the consumer instance or mismatched records between the producer and consumer instance in Instance Data Replication \(IDR\).

**Parent Topic:**[Administering Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication]()

[Deploying a replication configuration from one instance to another in Instance Data Replication]()

[Cloning options with Instance Data Replication]()

[Monitoring replication status in Instance Data Replication]()

[Monitoring queues in Instance Data Replication]()

[Avoiding insert and update errors in Instance Data Replication]()

[Resolving data replication errors in Instance Data Replication]()

