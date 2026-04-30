---
title: Warning and error messagesInstance Data Replication
description: Understand error and warning messages related to schema definitions. You can then troubleshoot or fix Instance Data Replication \(IDR\) replication issues.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Transform replication data for Instance Data Replication, Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Warning and error messagesInstance Data Replication

Understand error and warning messages related to schema definitions. You can then troubleshoot or fix Instance Data Replication \(IDR\) replication issues.

|Message|Type|Action|
|-------|----|------|
|`The consumer instance does not recognize the [specified] table from the associated IDR schema.`|Error|The replication entry cannot process any messages. Please enable a transformation with this table to receive updates from this table to the consumer instance.|
|`The consumer instance does not recognize the [specified] column from the associated IDR schema.`|Warning|The replication entry cannot process any of the specified columns. Please enable a transformation with this table in order to receive updates from this column to the consumer instance.|
|`The consumer instance does not recognize the column type or length from the associated IDR schema for these columns: [specified columns].`|Warning|The consumer instance might lose data for those columns. Please enable a transformation with this table in order to receive updates from these table columns.|

**Parent Topic:**[Transform replication data for Instance Data Replication](../task/modify-replicated-data.md)

