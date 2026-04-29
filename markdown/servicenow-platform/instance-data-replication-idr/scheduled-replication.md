---
title: Scheduled replication
description: Replicate historical inserts and updates from a producer instance to one or more consumer instances on a scheduled basis in Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Scheduled replication

Replicate historical inserts and updates from a producer instance to one or more consumer instances on a scheduled basis in Instance Data Replication \(IDR\).

Instead of continuously replicating data as it's created or changed on your producer instance, you can schedule replication from the producer to one or more consumers at regular intervals each day. Consider scheduling replication for frequently updated, larger tables when immediate data replication to the consumer isn't required.

For example, you should avoid continuous replication of CMDB tables. Replicating CMDB data as changes occur can create performance issues or unforeseen consequences with replication due to the number of records involved. Instead, you can use scheduled replication to periodically replicate CMDB data that accumulates on the producer instance.

For more information, see [Set up scheduled replication](../task/set-up-scheduled-replication-idr.md).

