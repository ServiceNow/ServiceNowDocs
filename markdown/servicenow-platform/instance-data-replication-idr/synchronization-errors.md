---
title: Review synchronization errors in Instance Data Replication
description: Review the status field to check if synchronization is working correctly on the Instance Data Replication \(IDR\) consumer instance.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Review synchronization errors in Instance Data Replication

Review the status field to check if synchronization is working correctly on the Instance Data Replication \(IDR\) consumer instance.

## Before you begin

Before identifying synchronization errors, complete the tasks in [check for common issues](../reference/common-issues-idr.md).

Role required: idr\_admin or admin

## About this task

Synchronization errors occur when a producer instance doesn't send data or a consumer instance doesn't receive data. Synchronization errors appear in the **Status** field on the consumer instance as **Replication Error**.

## Procedure

1.  Determine if the consumer successfully sent the synchronize request to the producer:

    1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

    2.  Select a consumer replication set.

    3.  Click the **Replication Metadata Logs** related link.

    4.  Sort the logs in a descending order in the Log Sequence column.

    5.  Find the most recent payload with the REPL\_SET\_DETAIL\_REQUEST type and open it.

        If you do not see this payload type, refresh the log until you see a payload with the REPL\_SET\_DETAIL\_REQUEST type.

    6.  Verify that you see the correct producer instance ID in the To column.

        If the producer instance ID is incorrect, [update the ID](create-c-replication-set.md) and click **Activate**.

    7.  Verify that you see Sent in the Status column.

        If you don't see Sent in the Status column, the producer didn't send any updates.

2.  Determine if the producer received the synchronize request from the consumer:

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select a producer replication set.

    3.  Click the **Replication Metadata Logs** related link.

    4.  Sort the logs in a descending order in the Log Sequence column.

    5.  Find the most recent payload with the REPL\_SET\_DETAIL\_REQUEST type and open it.

        If you don't see this payload type, refresh the log until you see the REPL\_SET\_DETAIL\_REQUEST type.

    6.  Verify that you see the correct consumer instance ID in the From column.

        If the consumer instance ID is incorrect, [update the ID](create-c-replication-set.md).

    7.  Verify that you see Received in the Status column.


**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

