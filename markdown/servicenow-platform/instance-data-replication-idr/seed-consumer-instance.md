---
title: Seed a consumer instance for Instance Data Replication
description: Seed all or some of the tables in your Instance Data Replication \(IDR\) replication sets depending on the needs of your consumer instance.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Seed a consumer instance for Instance Data Replication

Seed all or some of the tables in your Instance Data Replication \(IDR\) replication sets depending on the needs of your consumer instance.

## Before you begin

Role required: idr\_admin or admin

## About this task

Seeding replicates existing records from the producer instance to the consumer instance. You can initiate seeding requests on a consumer instance while you are activating a consumer replication set. Seeding options are not available in bi-directional or discrete replication sets by design.

You can select either full seeding or partial seeding.

-   Full seeding replicates all existing records from a table in the producer instance. Perform a full seeding when you want to replicate all existing records.
-   Partial seeding enables you to filter and replicate specific records from the producer. Perform a partial seeding when you want to replicate only some of the records from the producer.

The producer instance handles one seeding request at a time. When the producer instance is busy with a seeding request, subsequent seeding requests are queued and initiated in the order that they are received.

-   Records that exist on the producer instance and not on the consumer instance are copied to the consumer instance.
-   If the sys\_id on the producer matches an existing record on the consumer instance, the entire record on the consumer instance is updated to match the producer.
-   The sys\_id of the record identifies the record on both instances. If you use the custom coalesce option, the field you select is used to coalesce records in both instances.
-   If a replication set changes and no longer includes a table, IDR does not alter the records in the corresponding table on the consumer instances.

If you encounter an error during seeding, see [Fix seeding errors](fix-seeding-errors.md).

-   Seeding continues even if errors occur on some consumer tables. You can restart seeding specifically on the tables that have errors or on all tables in a replication set.
-   The maximum for a retry reseeding request is 10,000 errors. If you have more errors, perform a [full seeding](seed-consumer-instance.md).

Do not retry full seeding if the data set exceeds any of the following limitations:

-   Record size exceeds 32 MB
-   Seeding request exceeds 3 million records
-   Replication takes longer than seven days to complete

**Note:** Seeding is not a replacement for cloning. Do not use IDR to clone instances.

## Procedure

1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets** and click a consumer replication set.

2.  On the **Inbound Entries** tab, select the entry or entries that you want to initiate seeding for.

3.  To initiate a full seeding, click **Full Seeding**.

    A dialog box opens stating that the system is requesting all matching records.

4.  To configure a partial seeding, click **Partial Seeding**.

    1.  If you selected more than one entry, select the Replication entry that you want to configure and select **Configure Seeding**.

    2.  Configure one or more Custom Filter conditions, operators, and values.

    3.  To download the current field values and to replicate the files that are associated with the records, select **Include Attachments**.

    4.  To download the current field values and the history of all field updates, select **Include History**.

    5.  In the Included Fields columns, use the arrows to move table fields into the Selected column to replicate them or into the Available column to prevent replicating them.

    6.  Click **Save Configuration**.

    7.  Configure other Replication entries as needed.

    8.  When you are ready to initiate seeding, click **Request Partial Seeding**.

    **Note:** The Custom Filter determines which records to include in the partial seeding request.

    The system must replicate some fields, such as **Sys ID**. The system cannot replicate some fields, such as **Edge Encrypted** and **Password**. They do not appear in either column.

5.  To discard your seeding request before you click **Request Partial Seeding**, click **Cancel**.


## Result

In a successful seeding, all selected data on a producer instance is replicated on a consumer instance. After seeding, the consumer instance maintains a history of all field updates.

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

