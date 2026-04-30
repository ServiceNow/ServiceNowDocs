---
title: View a message in a Hermes topic
description: View the payload of a message in a Hermes topic using the Hermes Messaging Service topic inspector.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Monitoring topics, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a message in a Hermes topic

View the payload of a message in a Hermes topic using the Hermes Messaging Service topic inspector.

## Before you begin

Role required: hermes\_admin, kafka\_namespace\_admin, or admin

**Important:** Administrators with the kafka\_namespace\_admin role can view message data across different domains.

## About this task

**Note:** Messages expire after 36 hours.

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Topic inspector**.

2.  Select a cluster set with topics that you want to view in the **Select Service** drop-down list.

3.  Select **List Topics**.

    The primary cluster, the secondary cluster, and the number of topics on the instance are listed above the table of topics.

4.  View messages from all partitions.

    1.  Select a topic row in the table.

    2.  Retrieve messages from all clusters or a specific cluster using the **Select Data center** drop-down list.

    3.  Retrieve messages received in a specific date range using the **Message start date \(UTC\)** and **Message end date \(UTC\)** fields.

    4.  Search for a specific message in the partition by entering a keyword or regular expression in the **Message body filter** field.

        **Note:** The message filter only supports string searches of text data. You can't search for messages with binary payloads.

    5.  Select **Inspect Topic**.

5.  View messages in a specific partition.

    1.  View the list of partitions by selecting **Load Partition Info**.

    2.  Select a partition with messages that you want to retrieve in the **Read from Partition** drop-down list.

    3.  Retrieve messages from all clusters or a specific cluster using the **Select Data center** drop-down list.

    4.  Retrieve messages received in a specific date range using the **Message start date \(UTC\)** and **Message end date \(UTC\)** fields.

    5.  Search for a specific message in the partition by filtering the **Message body filter** field using a keyword or regular expression.

        **Note:** The message filter only supports string searches of text data. You can't search for messages with binary payloads.

    6.  Select **Inspect Topic**.

6.  Track message processing for each consumer by selecting **View Consumer Info**.

7.  View audit history for a topic by selecting **Audit Info**.

    The Hermes Topic Audit Records \[hermes\_topic\_audit\_records\] table displays an audit trail of topic changes, including the type of operation performed, the originating instance as Principal Name, and the timestamp for each change. Audit history is refreshed every 30 minutes.

8.  View the message details and payload.

    **Note:** To view headers, keys, or messages that are greater than 20 characters, select the **View** link or download the data.

<table id="table_bdn_zlv_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Offset

</td><td>

The Hermes Kafka cluster's datacenter identifier and the position of the message in the partition.

</td></tr><tr><td>

Partition

</td><td>

Partition of the topic where the message is stored.

</td></tr><tr><td>

Timestamp

</td><td>

Date and time when the message was created.

</td></tr><tr><td>

Headers

</td><td>

Message header.

</td></tr><tr><td>

Key

</td><td>

Message key.

</td></tr><tr><td>

Payload

</td><td>

Message body contents. Note the following information about the message payload:-   The topic inspector automatically replaces some characters with escape characters in message payload text data.
-   The message size that is displayed is the size of the payload as viewed in the topic inspector and not necessarily the size of the message as it exists in the Hermes Kafka cluster.


</td></tr></tbody>
</table>
**Parent Topic:**[Monitoring topics in the Hermes Kafka cluster](../concept/monitoring-topics-hermes-kafka-cluster.md)

