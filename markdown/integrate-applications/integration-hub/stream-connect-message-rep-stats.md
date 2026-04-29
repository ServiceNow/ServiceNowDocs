---
title: Viewing Stream Connect Message Replication statistics
description: When message replications are running, the system creates a metrics record for each active topic replication every 60 seconds. Metrics records provide information about topic replications. You can view metrics records on the Message Replication Statistics \[sys\_sc\_channel\_replication\_metric\] table. You can also view metrics records for a topic by checking the Message Replication Statistics on its Kafka Topic Replication record.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Message replication, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Viewing Stream Connect Message Replication statistics

When message replications are running, the system creates a metrics record for each active topic replication every 60 seconds. Metrics records provide information about topic replications. You can view metrics records on the Message Replication Statistics \[sys\_sc\_channel\_replication\_metric\] table. You can also view metrics records for a topic by checking the Message Replication Statistics on its Kafka Topic Replication record.

|Metric|Description|
|------|-----------|
|Collection time|Time the metric collection ended. Formatted as yyyy-MM-dd and HH:mm:ss.|
|Collection interval|Duration of the collection interval, given in seconds.|
|Channel replication|Reference to the Kafka topic replication record.|
|Message count|Number of messages replicated during the collection interval.|
|Byte count|Number of bytes replicated during the collection interval.|
|Lag messages|At the end of the collection interval, the number of messages remaining to be processed at the source.|
|Source|Name of the topic used as the source.|
|Destination|Name of the topic used as the destination.|
|Direction|Direction of the replication, either **To ServiceNow** or **From ServiceNow**.|
|MID Server|Reference to the MID Server responsible for replication.|

**Parent Topic:**[Stream Connect Message Replication](../concept/stream-connect-message-replication.md)

