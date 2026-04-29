---
title: Restore access to replication data for Instance Data Replication
description: Restore Instance Data Replication \(IDR\) access to replicated data by sending a request to the producer replication set admin.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage consumer access, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Restore access to replication data for Instance Data Replication

Restore Instance Data Replication \(IDR\) access to replicated data by sending a request to the producer replication set admin.

## Before you begin

Role required: admin

## About this task

When the producer replication set administrator generates a new encryption key, consumer sets with a status of Approved automatically receive the new key and data replication is uninterrupted. Consumer sets with a status of Denied or Pending Approval do not receive the new encryption key and replication stops.

## Procedure

1.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

2.  Select the consumer replication set to restore access to.

3.  Click the **Request Shared Key** related link.

    The system sends a request to the producer replication set administrator. If you are granted access, the consumer Approval Status changes to Approved.

4.  If the producer replication set has changed, click the **Synchronize Replication Entries** related link.

5.  To get the latest data in the producer replication set, on the **Inbound Entries** tab, select all the tables and click **Activate**.


**Parent Topic:**[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

