---
title: Coalesce columns in Instance Data Replication
description: The coalesce columns feature is used to identify records when you perform data inserts, updates, and deletions across instances using Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Explore, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Coalesce columns in Instance Data Replication

The coalesce columns feature is used to identify records when you perform data inserts, updates, and deletions across instances using Instance Data Replication \(IDR\).

By default, the **sys\_id** field is used to coalesce records in IDR. Beginning with the San Diego release, you can choose to use a different field.

Use the coalesce columns feature when records on the consumer instance have a different sys\_id than the same record on the producer instance. For example, when the record is created by Discovery and loaded into multiple instances. You select the **Coalesce** field in the [Replication Entry form on the producer](../task/create-p-replication-set.md).

When you select the **Coalesce** field, you must verify the following:

-   The field that you selected is in the Included Fields on the Replication Entry form on the producer instance.
-   The field exists with the same name, length, and type on the consumer instance.

    **Note:** The **Coalesce** field can be different on the consumer instance if you create a valid transform for the field.

-   The **Unique** column value for the field that you selected is set to **true** in the Dictionary Entry \[sys\_dictionary\] table.

Don’t change the value of the field after it’s set as the **Coalesce** field.

To change the **Coalesce** field after it has been set, you must delete the Replication Entry on the producer instance and create a new Replication Entry.

If the **Coalesce** field doesn’t exist on the consumer instance, the following error is displayed on the Consumer Replication Set form. `The consumer instance does not recognize the <column_name> coalesce field as a valid member of the <table_name> table. Create this field or enable a transformation with this table to receive updates from the producer table to the consumer instance.`

## Transforms

If transform is enabled on the producer instance, the **Coalesce** field on the target table must have the same name, type, and length. If any of those parameters don’t match, an error is displayed.

If transform is enabled on the producer instance, the mapping is invalid for the **Coalesce** field, and the consumer syncs entries, the system displays an error on the Consumer Replication Set form.

If transform is enabled for a replication entry with a valid mapping of the **Coalesce** field and then the table schema for the target table is updated so that the mapping is no longer valid, the system displays an error on the Replication Entry form.

If a replication entry attempts to enable transform and a valid mapping for the **Coalesce** field doesn’t exist from the source table to the target table, the system displays an error on the Replication Entry form.

