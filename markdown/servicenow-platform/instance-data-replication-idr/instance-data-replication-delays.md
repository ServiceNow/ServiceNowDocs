---
title: Delays in replicating data with Instance Data Replication
description: Delays in replicating data from the producer instance to the consumer instance can occur with Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Delays in replicating data with Instance Data Replication

Delays in replicating data from the producer instance to the consumer instance can occur with Instance Data Replication \(IDR\).

After IDR has been set up on the producer instance, the **IDRProducerJob** job runs on producer instances to detect data updates. When there are updates to replicate, the producer instance sends the updates to consumer instances.

The IDRConsumerJob job runs on the consumer instances to detect the data updates from a producer. When the IDRConsumerJob job detects updates, it updates the data in consumer tables.

![Data lag.](../image/data-lag.png "IDR data updates flow")

It takes some time for the data updates in a producer replication set to appear in consumer replication sets. You can look on the [monitoring dashboard](instance-data-replication-dashboard.md) to see how long data updates take from a producer replication set to consumer replication sets. Look at the [queue dashboard](idr-queue-dashboard.md) to see the replication record queue, message queue, and messages processed for all replications sets.

If you have significant data delays, contact Customer Service and Support.

**Parent Topic:**[Administering Instance Data Replication](administering-instance-data-replication.md)

**Related topics**  


[Comparing replicated data between instances in Instance Data Replication](comparing-replicated-data.md)

[Deploying a replication configuration from one instance to another in Instance Data Replication](copying-replication-configuration.md)

[Cloning with Instance Data Replication](cloning-with-instance-data-replicaton.md)

[Monitoring Instance Data Replication](instance-data-replication-dashboard.md)

[Monitoring queues in Instance Data Replication](idr-queue-dashboard.md)

[Avoiding insert and update errors in Instance Data Replication](preventing-insert-update-errors.md)

[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

