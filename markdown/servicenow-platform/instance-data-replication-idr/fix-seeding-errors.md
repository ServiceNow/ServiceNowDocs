---
title: Fix seeding errors in Instance Data Replication
description: Retry Instance Data Replication \(IDR\) seeding on tables with seeding errors, which occur from network problems and failed inserts, so that you don't have to do a full seeding.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Fix seeding errors in Instance Data Replication

Retry Instance Data Replication \(IDR\) seeding on tables with seeding errors, which occur from network problems and failed inserts, so that you don't have to do a full seeding.

## Before you begin

Role required: idr\_admin or admin

## About this task

The maximum for a retry reseeding request is 10,000 errors. If you have more errors, perform a [full seeding](seed-consumer-instance.md).

**Note:** Seeding is not a replacement for cloning. Do not use IDR to clone instances.

Do not retry full seeding if you exceed any of the following limitations:

-   Record size exceeds 10 MB
-   Seeding request exceeds 3 million records
-   Replication takes longer than seven days to complete

**Note:** To avoid these limitations, reduce the number of tables in the seeding request, reduce the size of the records, or use partial seeding.

## Procedure

1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

2.  On the **Seeding Requests** tab of the Consumer Replication Set pane, click a seeding request that failed.

    ![Seeding failure notification.](../image/failed-seeding-request.png)

3.  On the Seeding Request pane, click the **Payload Errors** tab and examine the values in the Message column.

4.  Click **Retry All Errors** or select specific errors, and then click **Retry Selected Errors**.

    The image shows areas where you can retry errors.

    ![Retry some or all errors.](../image/partial-seeding.png)


**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

