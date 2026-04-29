---
title: Configure a script consumer
description: Use a script to import and process data from your Kafka environment.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Configure a script consumer

Use a script to import and process data from your Kafka environment.

## Before you begin

-   Role required: integration\_hub\_admin
-   This consumer requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).
-   The ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin is required.

## About this task

To configure a consumer, you need to create two records.

1.  The consumer record, which specifies how to import and process data.
2.  A record for the Kafka stream, which defines the stream of data to your consumer.

This task covers the consumer creation. For instructions on creating a Kafka stream, see [Create a Kafka stream](create-kafka-stream.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Consumers** &gt; **Script Consumer**.

2.  Select **New**.

3.  In the form, fill in the fields.

<table id="table_utt_jmq_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Script consumer.

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

Event consumer

</td><td>

Script to use to consume the messages received from the Kafka topic.

</td></tr><tr><td>

Application

</td><td>

Application scope for the Script Consumer.

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


## Example

This example shows a sample script for processing messages. It includes the **utc\_timestamp** field, a string-type field in UTC timezone, and the **metadata** field, which includes the following:

-   **timestampEpoch**, data type: long
-   **partition**, data type: int
-   **offset**, data type: long
-   **dataCenter**, data type: string

```
(function process(messages) {
  for (var i = 0; i < messages.length; i++) {
    var m = messages[i];

    var headerParts = [];
    for (var j = 0; j < m.headers.length; j++) {
      headerParts.push('header[' + j + ']_key=' + m.headers[j].key + ' | header[' + j + ']_value=' + m.headers[j].value);
    }

    var line = [
      'message_key='     + m.key,
      'message_body='    + m.message,
      'partition='       + m.metadata.partition,
      'offset='          + m.metadata.offset,
      'datacenter_id='   + m.metadata.datacenter_id,
      'utc_timestamp='   + m.utc_timestamp,
      'timestamp_epoch=' + m.metadata.timestamp_epoch
    ].concat(headerParts).join(' | ');

    gs.info('[Kafka Message] ' + line);
  }
})(messages);

```

To convert the **utc\_timestamp** field to GlideDateTime, see the following examples.

```

// Example 1
var timestamp = new GlideDateTime("2025-08-19 23:31:45");
console.log(timestamp.getValue());

// Example 2 
var timestamp2 = new GlideDateTime();
timestamp2.setNumericValue(1755646305218);
console.log(timestamp2.getValue());

// Example 3
var timestamp3 = new GlideDateTime("1970-01-01 00:00:00");
timestamp3.add(1755646305218);
console.log(timestamp3.getValue());

```

## What to do next

[Create a Kafka stream](create-kafka-stream.md) for this consumer. After the stream is activated, you can start receiving messages from your Kafka environment.

**Parent Topic:**[Using Stream Connect for Apache Kafka](../concept/stream-connect-apache-kafka.md)

