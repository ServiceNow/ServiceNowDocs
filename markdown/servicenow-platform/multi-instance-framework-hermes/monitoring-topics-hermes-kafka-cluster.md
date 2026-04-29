---
title: Monitoring topics in the Hermes Kafka cluster
description: Monitor message processing and view topics in the Hermes Kafka cluster that belong to you using the Hermes Messaging Service topic inspector.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Monitoring topics in the Hermes Kafka cluster

Monitor message processing and view topics in the Hermes Kafka cluster that belong to you using the Hermes Messaging Service topic inspector.

## Topics partitions

Events are stored in one or more partitions within a topic. Dividing a topic into partitions helps distribute the processing load across multiple brokers in the Hermes Kafka cluster. Each broker can handle messages from different partitions of the same topic, ensuring that no single broker is responsible for processing all the messages for a single topic. This distribution improves scalability and fault tolerance.

Events in a partition are immutable. One event can't overwrite another event in the same partition. If the same event is sent to a partition more than once, it is appended to the list of events in the partition.

## Tracking messages in partitions

You can track messages in the Hermes Kafka cluster by viewing partition information.

-   Determine whether your messages are reaching the Hermes Kafka cluster by checking whether the end offset value changes when you produce messages to a topic.
-   Determine whether messages have expired by noting the beginning offset value, which increases as messages expire. If you send messages to a topic but the beginning offset is higher than you expect, some of the messages have already expired. Messages expire in the Hermes Kafka cluster after 36 hours.

## Tracking consumer progress

You can track the progress of processing messages for each consumer by viewing consumer information.

-   View the consumers for each partition in a topic, including the group ID and consumer ID for each consumer.
-   Determine which message a consumer is processing by viewing the **Current Offset** column.
-   Determine whether the consumer is delayed by checking the **Lag** column. The lag is the difference between the current offset and the end offset that indicates how many messages remain.

## Inspecting message details

You can detect problems with consuming messages using the topic inspector. For example, if a message that you produced isn't consumed from the Hermes Kafka cluster, you can validate the payload and message key by inspecting the topic. You can also download the full payload and save it as a file on your local machine.

You can view messages as binary data in base-64 encoding instead of UTF8 strings by adding a system property. See [Hermes Messaging Service system properties](../reference/hermes-messaging-service-properties.md).

-   **[View a message in a Hermes topic](../task/view-messages-hermes-topic.md)**  
View the payload of a message in a Hermes topic using the Hermes Messaging Service topic inspector.

**Parent Topic:**[Managing namespaces and topics in Hermes](managing-namespaces-topics-hermes.md)

**Related topics**  


[Managing namespaces in Hermes](managing-namespaces-hermes.md)

[Managing topics in Hermes](managing-topics-hermes.md)

