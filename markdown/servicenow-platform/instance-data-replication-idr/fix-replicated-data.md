---
title: Reseed missing or mismatched records in Instance Data Replication
description: Synchronize data between instances by reseeding records missing from the consumer instance or mismatched records between the producer and consumer instance in Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Comparing replicated data, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Reseed missing or mismatched records in Instance Data Replication

Synchronize data between instances by reseeding records missing from the consumer instance or mismatched records between the producer and consumer instance in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin

## About this task

Data comparison results and logs are purged after five days.

## Procedure

1.  On the producer instance, navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select a producer replication set with data that you want to reseed to the consumer.

3.  View the data comparison results.

    1.  Navigate to the IDR Data Comparison Requests related list.

    2.  Select a data comparison.

4.  Synchronize the data between the producer and the consumer instance by reseeding.

    -   Reseed all records by selecting **All** in the **Reseed mismatched records** field.
    -   Reseed only the mismatched or missing records by selecting **Mismatched** in the **Reseed mismatched records** field.
5.  Select **Reseed**.


## Result

Records are reseeded from the producer to the consumer and the results are displayed when the job is finished.

## What to do next

If records are still missing or mismatched, contact Customer Service and Support for assistance.

**Parent Topic:**[Comparing replicated data between instances in Instance Data Replication](../concept/comparing-replicated-data.md)

