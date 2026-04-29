---
title: Create a Kafka stream
description: Define a data stream for an Extract Transform Load \(ETL\), Transform Map, or Script consumer. A Kafka stream defines the stream of data to your consumer.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Create a Kafka stream

Define a data stream for an Extract Transform Load \(ETL\), Transform Map, or Script consumer. A Kafka stream defines the stream of data to your consumer.

## Before you begin

-   Role required: integration\_hub\_admin
-   Kafka streams are part of Stream Connect which requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

## About this task

You must create a Kafka stream to use an ETL, Transform Map, or Script consumer. After you configure a consumer, and create and activate a stream, you can start receiving messages from your Kafka environment.

## Procedure

1.  Open the record for your ETL, Transform Map, or Script consumer.

    To find a consumer record, navigate to **All** &gt; **IntegrationHub** &gt; **Consumers** and select **ETL Consumer**, **Transform Map Consumer**, or **Script Consumer**.

2.  Locate the Kafka Streams section and select **New**.

3.  In the form, fill in the fields.

<table id="table_yww_13q_hvb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Kafka stream.

</td></tr><tr><td>

Topic Alias

</td><td>

Name of the topic alias for the topic to monitor for messages.

</td></tr><tr><td>

Max concurrency

</td><td>

Maximum number of parallel processors to use to consume messages, and the number of partition groups to create.

 Default value: 1

</td></tr><tr><td>

Relative weight

</td><td>

For each cycle, the maximum amount of time allocated to the consumer for processing messages, relative to other consumers. For example, a consumer with a relative weight that's twice as high as another consumer's gets twice as much time. Consumers that have the same relative weight get the same amount of time.

The minimum value is 5. The maximum value is 2000. The default value is equal to the max concurrency multiplied by the value of the **glide.ih.kafka.consumer.max\_seconds\_per\_partition\_group** property. The **glide.ih.kafka.consumer.max\_seconds\_per\_partition\_group** property specifies the maximum time, in seconds, allocated to each partition group. Its default value is 10.

The system uses the relative weight to calculate the partition group timeout for the subscription. The partition group timeout specifies the maximum time, in milliseconds, allocated to each partition group in a specific subscription.

This field appears only when **Advanced** is selected.

</td></tr><tr><td>

Start consuming

</td><td>

Option to specify where to begin consuming messages from the topic. Select one of the following.-   **Messages received after the first activation**: Only consumes messages the topic received after the stream was activated.
-   **All the messages stored in the topic**: Consumes all the messages in the topic, even messages received before the stream was activated.


</td></tr><tr><td>

Message handling

</td><td>

Option to specify the number of messages processed per run or let the system decide the number of messages. Select one of the following.-   **Automatically optimize**: The system determines the number of messages to process per run.
-   **Manually override**: You specify the number of messages to process per run.
This field appears only when **Advanced** is selected.

</td></tr><tr><td>

Maximum messages

</td><td>

Maximum number of messages to process per run.

 This field appears only when **Manually override** is selected from **Message handling**.

</td></tr><tr><td>

Run as

</td><td>

Option to run the consumer with the credentials of a specified user.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer to stream data to. This field is automatically set to the name of the consumer from which you started adding the stream.

</td></tr><tr><td>

Active

</td><td>

Option to make the stream active.

</td></tr><tr><td>

Advanced

</td><td>

Option to view the advanced fields **Relative weight** and **Message handling**.

</td></tr></tbody>
</table>4.  Under Related Links, select **Activate**.

    After the stream is activated, the system automatically creates a Kafka subscription for the associated consumer.

5.  Select **Submit**.


## Result

When you activate the stream, the consumer begins looking for messages to process in the specified topic. You can view detailed information about the consumer and its performance by visiting its subscription page. For details, see [Viewing Kafka subscriptions and statistics](../concept/kafka-subscriptions-statistics.md).

**Parent Topic:**[Using Stream Connect for Apache Kafka](../concept/stream-connect-apache-kafka.md)

