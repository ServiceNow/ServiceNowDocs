---
title: Configure an Extract Transform Load \(ETL\) consumer
description: Import and process data from your Kafka environment using your existing Robust Transform Engine \(RTE\) configurations.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Configure an Extract Transform Load \(ETL\) consumer

Import and process data from your Kafka environment using your existing Robust Transform Engine \(RTE\) configurations.

## Before you begin

-   Role required: integration\_hub\_admin
-   This consumer requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).
-   The ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin is required.
-   This consumer requires a [robust import set transformer](../../import-sets/concept/robust-import-set-transformers.md).

## About this task

To configure a consumer, you need to create two records.

1.  The consumer record, which specifies how to import and process data.
2.  A record for the Kafka stream, which defines the stream of data to your consumer.

This task covers the consumer creation. For instructions on creating a Kafka stream, see [Create a Kafka stream](create-kafka-stream.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Consumers** &gt; **ETL Consumer**.

2.  Select **New**.

3.  In the form, fill in the fields.

<table id="table_wvt_wgq_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ETL consumer.

</td></tr><tr><td>

Robust import set transformer

</td><td>

Name of the robust import set transformer to use to process data.

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

Data in single column

</td><td>

Option to have the import set table store data in single column.

</td></tr><tr><td>

Column mapping

</td><td>

Option to specify whether the message's JSON key maps the data to the column's name or label in the import set table. Select one of the following.-   **Label**
-   **Column name**
This field appears only when the **Data in a single column** check box is cleared.

</td></tr><tr><td>

Application

</td><td>

Application scope for the ETL Consumer.

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

