---
title: Update a topic in Hermes
description: Update a Kafka topic in Hermes by modifying the topic record.
locale: en-US
release: xanadu
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing topics in Hermes, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update a topic in Hermes

Update a Kafka topic in Hermes by modifying the topic record.

## Before you begin

Role required: kafka\_admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Topics**.

2.  Select the topic record that you want to update.

3.  Change the number of partitions in the topic.

    Note the following restrictions:

    -   You can only increase the number of partitions.
    -   A topic can have up to 32 partitions.
4.  Change the topic's activation status.

5.  Select **Update**.


## Result

The topic record and the Kafka topic in the Hermes Kafka cluster are updated.

If an error occurs when updating the partition count, you can synchronize the topic's partition count across Hermes Kafka clusters by selecting **Synchronize Partition Count**.

**Parent Topic:**[Managing topics in Hermes](../concept/managing-topics-hermes.md)

