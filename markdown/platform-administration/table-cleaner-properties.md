---
title: Table cleaner properties
description: These system properties control table cleaner behavior.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Management reference, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table cleaner properties

These system properties control table cleaner behavior.

To set table cleaner system properties, navigate to the System Properties \[sys\_properties\] table and add the property.

<table id="table_pkw_2hy_mxb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure the number of days table cleaner must wait before attempting to reprocess a slow rule.

 `glide.db.tablecleaner.days_before_slow_rule_reattempt`

</td><td>

When a table cleaner rule has a query that takes longer than 30 seconds to complete, the entire table cleaner job is stopped. By default, table cleaner waits two days before including that rule in the table cleaner job again.You can change the default waiting period by adding this property.

-   Type: integer
-   Default value: 2

</td></tr><tr><td>

Configure a time limit for a table cleaner rule.

 `glide.db.tablecleaner.chunk_delete_max_time_spent`

</td><td>

Limits how long the cleaner spends trying to batch-delete records per rule during a single run. The value is given in seconds and defaults to 1200 \(20 minutes\), which means the table cleaner runs hourly for a maximum of 20 minutes.You can change the default time limit by adding this property.

-   Type: integer
-   Default value: 1200

</td></tr></tbody>
</table>**Parent Topic:**[Data Management reference](data-management-reference.md)

