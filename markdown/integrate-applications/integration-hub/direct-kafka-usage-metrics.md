---
title: Direct Kafka usage metrics
description: Direct Kafka Usage metrics table provides administrators with visibility into data usage between your instance and Direct Kafka systems. This read-only table tracks usage metrics on an hourly, daily, and monthly basis. Usage records are automatically retained for 13 months, with a scheduled cleaner job removing records older than this threshold on a monthly basis.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Integration Hub, Workflow Data Fabric]
---

# Direct Kafka usage metrics

Direct Kafka Usage metrics table provides administrators with visibility into data usage between your instance and Direct Kafka systems. This read-only table tracks usage metrics on an hourly, daily, and monthly basis. Usage records are automatically retained for 13 months, with a scheduled cleaner job removing records older than this threshold on a monthly basis.

|Column|Description|
|------|-----------|
|Kafka Cluster|The name of the Kafka cluster being monitored.|
|Megabytes Per Hour|The amount of data transferred, measured in megabytes per hour.|
|Metric Name|The type of metric being tracked. Values: BytesProduced, BytesConsumed|
|Period Start|The timestamp indicating when the measurement period begins.|
|Roll Up Type|The aggregation level for the metric. Values: HOURLY, DAILY, MONTHLY|
|Topic|The specific Kafka topic associated with the usage metric.|

**Parent Topic:**[Integration Hub reference](../concept/integration-hub-reference.md)

