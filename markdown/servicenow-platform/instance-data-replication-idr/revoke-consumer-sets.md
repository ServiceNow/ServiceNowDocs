---
title: Revoke access to replicated data for Instance Data Replication
description: Revoke a consumer's access to replicated data if you believe that consumer instance should no longer receive data in Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage consumer access, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Revoke access to replicated data for Instance Data Replication

Revoke a consumer's access to replicated data if you believe that consumer instance should no longer receive data in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin, idr\_admin

## About this task

When you generate a new, shared encryption key, approved consumer sets automatically receive the new key and data replication is not interrupted. Any consumer set with a status of Denied or Pending Approval does not receive the new encryption key, and replication ceases.

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select the producer replication set that has consumers whose access needs to be revoked.

    The instance identifies the consumers under the **Consumer Subscriptions** tab.

    ![Revoke access](../image/revoke-consumer.png)

3.  On the **Consumer Subscriptions** tab, select the option for the consumer instance whose permissions you want to revoke.

4.  In the Actions on selected rows list, select **Revoke**.

    Instance Data Replication generates a new encryption key and shares it with all approved consumer sets. All other consumer sets stop receiving replication data. Admins of those consumer replication sets must [reapply to restore access to the replication data](restore-access.md).


**Parent Topic:**[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

