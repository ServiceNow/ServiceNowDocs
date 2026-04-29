---
title: Cancel scheduled replication
description: Cancel scheduled replication by deactivating or deleting a producer replication set.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up scheduled replication, Replicate data, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Cancel scheduled replication

Cancel scheduled replication by deactivating or deleting a producer replication set.

## Before you begin

Role required: admin

## About this task

Once set, you can't disable scheduled replication on a producer replication set; the option becomes read-only. You can either deactivate the set or delete and recreate it.

## Procedure

1.  Navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select the producer replication set for which you want to stop scheduled replication.

3.  Stop scheduled replication before another run occurs.

    -   Pause scheduled replication indefinitely by selecting **Deactivate**. This option stops replication before the next schedule run.
    -   Stop scheduled replication by selecting **Delete**. This option deletes the producer replication set. If you plan to recreate the producer replication set, record the settings you configured before you delete the replication set.

## Result

Scheduled replication ends. After deactivating the producer replication set, any in progress seeding requests will complete, but pending requests will not be processed.

## What to do next

If you intend to resume scheduled replication, you can sync records that weren't replicated during the deactivation period by running a data comparison request. See [Comparing replicated data between instances in Instance Data Replication](../concept/comparing-replicated-data.md). Alternatively, you can replicate missing records by performing a partial seeding request from the Inbound Entries related list on the consumer replication set.

**Parent Topic:**[Set up scheduled replication](set-up-scheduled-replication-idr.md)

