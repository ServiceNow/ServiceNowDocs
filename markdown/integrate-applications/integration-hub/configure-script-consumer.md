---
title: Configure a script consumer
description: Use a script to import and process data from your Kafka environment.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Data and Automation]
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


## Example

This example shows a sample script for processing messages.

```
(function process(messages) {
 // Add your code here to consume kafka messages 
 // sample message [ { 'key' : 'message_key' , 'message' : 'message' , 'headers' : [ { 'key' : 'header_key' , 'value' : 'header_value' } ] } ] 

 for (var i = 0; i < messages.length; i++) {
     var message = JSON.parse(messages[i].message);
     gs.info('Number ' + message.number + ', short description ' + message.short_description +
         ', headers ' + JSON.stringify(messages[i].headers));
 }
})(messages);
```

## What to do next

[Create a Kafka stream](create-kafka-stream.md) for this consumer. After the stream is activated, you can start receiving messages from your Kafka environment.

**Parent Topic:**[Using Stream Connect for Apache Kafka](../concept/stream-connect-apache-kafka.md)

