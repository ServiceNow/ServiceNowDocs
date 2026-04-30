---
title: Fix seeding errors in Instance Data Replication
description: Retry Instance Data Replication \(IDR\) seeding on tables with seeding errors, which occur from network problems and failed inserts, so that you don't have to do a full seeding.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-01-30"
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
-   Replication takes longer than seven days to complete

**Note:** To avoid these limitations, reduce the number of tables in the seeding request, reduce the size of the records, or use partial seeding.

## Procedure

1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

2.  On the **Seeding Requests** tab of the Consumer Replication Set pane, select a seeding request that failed.

    ![Seeding failure notification.](../image/failed-seeding-request.png)

3.  In the Seeding Request details, select the Payload Errors related list and examine the values in the Message column.

4.  Retry the seeding request.Click or select specific errors, and then click **Retry Selected Errors**.

    -   Retry seeding for all errors by selecting **Retry All Errors**.
    -   Retry seeding for specific errors by selecting the check box next to each error and then selecting **Retry Selected Errors**.

**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

