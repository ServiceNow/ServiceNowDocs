---
title: Configure a Transform Map consumer
description: Import and process data from your Kafka environment using your existing transform map configurations.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Configure a Transform Map consumer

Import and process data from your Kafka environment using your existing transform map configurations.

## Before you begin

-   Role required: integration\_hub\_admin
-   This consumer requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).
-   The ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin is required.
-   This consumer requires a [transform map](../../../script/server-scripting/concept/c_CreatingNewTransformMaps.md).

## Formatting Kafka message payloads

Use simple JSON payloads for Kafka messages. Each Kafka message should have just one, flat JSON object. Complex JSON payloads, such as those with lists and nested objects, are not supported.

Example of simple, valid JSON input, using a flat map of key-value pairs.

```
{"key1": "value1", "key2": "value2"}
```

Examples of complex, invalid JSON input. The first uses a list. The second uses nested objects.

```
[{"key1": "value1", "key2": "value2"}, {"key1": "value3", "key2": "value4"}]
```

```
{"key1": "value1", "key2": {"key3": "value3", "key4": "value4"}}
```

## About this task

To configure a consumer, you need to create two records.

1.  The consumer record, which specifies how to import and process data.
2.  A record for the Kafka stream, which defines the stream of data to your consumer.

This task covers the consumer creation. For instructions on creating a Kafka stream, see [Create a Kafka stream](create-kafka-stream.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Consumers** &gt; **Transform Map Consumer**.

2.  Select **New**.

3.  In the form, fill in the fields.

<table id="table_v2m_wlq_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Transform Map consumer.

</td></tr><tr><td>

Transform Map

</td><td>

Name of the transform map to use to process data.

</td></tr><tr><td>

Delivery guarantee

</td><td>

If there's a node failure, option to specify the delivery guarantee for incoming messages. Select one of the following.-   **No lost but duplicates**: All messages are delivered at least once. Some messages might be delivered more than once.
-   **Once or not at all**: A message isn’t delivered more than once. Some messages might not be delivered at all.


</td></tr><tr><td>

Serialization format

</td><td>

The serialization format for the message. Select one of the following. -   **Plain Text**: Select this option for any plain-text messages. This is the default format.
-   **Encoded**: Select this option for messages in an Apache Avro format. Converting plain-text messages to an Avro format requires a schema. Select the schema registry in the **Schema registry** field. For more information on schemas, see [Schema management in Stream Connect](../concept/schema-management.md).


</td></tr><tr><td>

Column mapping

</td><td>

Option to specify whether the message's JSON key maps the data to the column's name or label in the import set table. Select one of the following.-   **Label**
-   **Column name**


</td></tr><tr><td>

Synchronize Inserts

</td><td>

Option to guarantee there's only one record with unique coalesce field values by synchronizing record inserts.

</td></tr><tr><td>

Application

</td><td>

Application scope for the Transform Map Consumer.

</td></tr><tr><td>

Schema registry

</td><td>

Registry for the selected schema. Select one of the following.

-   **Standalone Schema Registry**
-   **Confluent Schema Registry**
 This field appears only when the **Serialization format** is set to **Encoded**.

 For the Confluent Schema Registry, if the received message's schema ID isn't in the schema table, the system imports the schema dynamically, using the configured REST connection.

</td></tr></tbody>
</table>4.  Select **Save**.


## What to do next

[Create a Kafka stream](create-kafka-stream.md) for this consumer. After the stream is activated, you can start receiving messages from your Kafka environment.

**Parent Topic:**[Using Stream Connect for Apache Kafka](../concept/stream-connect-apache-kafka.md)

