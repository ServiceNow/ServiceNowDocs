---
title: Continuous replication
description: Replicate inserts and updates from a producer instance to one or more consumer instances in near-real time in Instance Data Replication \(IDR\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/instance-data-replication-idr/continuous-replication.html
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Continuous replication

Replicate inserts and updates from a producer instance to one or more consumer instances in near-real time in Instance Data Replication \(IDR\).

Continuous replication in IDR enables syncing of specified tables and columns between instances. With continuous replication, inserts and updates are replicated in one direction from a producer instance to one or more consumer instances.

After you set up continuous replication, the IDRProducerJob job runs on the producer instance to detect data updates. When there are updates to replicate, the producer instance sends the updates to each subscribed consumer instance.

The IDRConsumerJob job runs on the consumer instances to detect the data updates from the producer. When the IDRConsumerJob job detects updates, it updates the data in consumer tables.

\[Omitted image "data-lag.png"\] Alt text: Data flows from the producer to the message queue and then to a consumer.

Inserts and updates on the producer instance are replicated in near-real time.

-   Monitor how long updates from the producer to the consumer are taking in the Monitoring Dashboard. See [Monitoring replication status in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/instance-data-replication-dashboard.md).
-   Monitor the replication record queue, message queue, and messages processed for all replications sets by in the Queue Dashboard. See [Monitoring queues in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/idr-queue-dashboard.md).

For more information, see [Set up continuous replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/set-up-continuous-replication-idr.md).

