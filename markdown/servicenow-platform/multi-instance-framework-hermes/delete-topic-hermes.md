---
title: Delete a topic in Hermes
description: Remove a topic and its messages by deleting it from Hermes. Deleting a topic record deletes it from your instance and from the Hermes Kafka cluster.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing topics, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delete a topic in Hermes

Remove a topic and its messages by deleting it from Hermes. Deleting a topic record deletes it from your instance and from the Hermes Kafka cluster.

## Before you begin

Role required: kafka\_admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Topics**.

2.  Select the topic that you want to delete.

3.  Select **Delete**.


## Result

The topic record is deleted from the Kafka Topics \[sys\_kafka\_topic\] table. The corresponding Kafka topic is deleted from the Hermes Kafka cluster.

**Parent Topic:**[Managing topics in Hermes](../concept/managing-topics-hermes.md)

