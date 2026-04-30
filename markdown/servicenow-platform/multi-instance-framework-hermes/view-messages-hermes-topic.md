---
title: View a message in a Hermes topic
description: View the payload of a message in a Hermes topic using the Hermes Messaging Service topic inspector.
locale: en-US
release: xanadu
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Monitoring topics in the Hermes Kafka cluster, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
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

2.  View topics in a different cluster by selecting a cluster set in the **Select Service** drop-down list.

    The primary cluster, the secondary cluster, and the number of topics on the instance are listed above the table of topics.

3.  View messages in a specific partition.

    1.  Select **Load Partition Info**.

    2.  In the **Read from Partition** drop-down list, select a partition.

4.  Retrieve messages from a topic that you want to inspect.

    1.  Select **Inspect Topic**.

    2.  Select a topic in the table.

    3.  Select the number of messages that you want to view in the **Number of messages** list.

    4.  Enter a date in the past to use a starting point for retrieving messages in the **Message start date \(UTC\)** field.

5.  View the message details and payload.

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

