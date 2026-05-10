---
title: Viewing Kafka subscriptions and statistics
description: View detailed information about a Kafka consumer and its performance, including the number of records added to the topic, the number of records processed, and the number of records remaining to be processed.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Viewing Kafka subscriptions and statistics

View detailed information about a Kafka consumer and its performance, including the number of records added to the topic, the number of records processed, and the number of records remaining to be processed.

A subscription is a record associated with a consumer. It stores configuration and performance details about the consumer. A subscription is created when a Kafka stream is activated.

Each subscription page includes the following sections.

-   Kafka subscription
-   Metrics
-   Kafka subscription partition groups
-   Stream Connect logs
-   Kafka consumer statistics

To view a subscription record, navigate to **IntegrationHub** &gt; **Stream Connect** &gt; **Subscriptions**. Select the info icon \(![info icon](../images/info-icon.png)\) for the subscription you want to view, then select **Open Record**.

![The Kafka subscription page with subscription details, metrics, and information on partition groups, consumer logs, and consumer statistics.](../images/kafka-subscription-statistics.png "Sample subscription page for a Kafka consumer")

## Kafka subscription

The Kafka subscription section shows configuration details for the consumer and subscription.

<table id="table_scz_xzg_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the subscription record.

</td></tr><tr><td>

State

</td><td>

State of the consumer. Options are:-   ACTIVE
-   REFRESHING
-   STOPPING

</td></tr><tr><td>

Topic alias

</td><td>

Topic alias for the topic the consumer is processing messages from.

</td></tr><tr><td>

Consumer ID

</td><td>

Unique identifier for the consumer.

</td></tr><tr><td>

Kafka Auto Position Policy

</td><td>

Specifies where the consumer starts reading messages from the topic. Options are:-   earliest: The consumer starts reading from the earliest available message in the topic.
-   latest: The consumer reads only the messages delivered to the topic after the consumer started.

</td></tr><tr><td>

Serialization format

</td><td>

Serialization format for the message. Options are:-   Plain Text
-   Encoded

</td></tr><tr><td>

Has Error

</td><td>

Indicates if the subscription has any errors.

</td></tr><tr><td>

Max Concurrency

</td><td>

Maximum number of parallel processors used to consume messages and the number of partition groups.

</td></tr><tr><td>

Partition group timeout

</td><td>

Maximum time, in milliseconds, allocated to each partition group in the subscription.

</td></tr><tr><td>

Kafka partitions

</td><td>

Number of partitions in the topic.

</td></tr><tr><td>

Max Batch Size

</td><td>

Maximum number of messages processed per run. Options are:-   automatically optimized: The system chooses the number of messages.
-   a number: The user manually selected a number.

</td></tr></tbody>
</table>## Metrics

Each metric is measured over three time intervals: the previous five minutes, the previous hour, and the previous 24 hours.

-   Topic Input Rate: The average number of records added to the topic per second.
-   Topic Queue Depth: The average number of records remaining to be processed in the topic.
-   Consumer Processing Rate: The average number of records processed per second. The **Estimated time to process the current queue** shows the time required to process the messages currently in the queue. It's calculated based on the queue depth and the consumer processing rate. The time estimate is formatted as HH:MM:SS.

## Related Links

View the record for the consumer that is processing the messages by selecting **Open consumer processing record**.

## Kafka subscription partition groups

The Kafka subscription partition groups tab shows the following details.

<table id="table_m42_ckn_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number for the partition group.

</td></tr><tr><td>

Owner of this partition group

</td><td>

Ownership state of the partition group. Options are:-   NONE: The partition group isn't owned by any Kafka consumer jobs. It's available to pick up and process.
-   PROCESSING: The partition group is owned by a Kafka consumer job and is processing messages.
-   LOCKED: The partition group isn’t owned by a Kafka consumer job and isn’t available to pick up.

 When a Kafka consumer job is activated, it checks for the earliest updated record with an owner of NONE and picks one.

 Then the consumer job changes the owner to PROCESSING and processes it for 10 seconds.

 When it's done processing, the state is changed back to NONE, so it can be picked up and processed again later.

 If the consumer job processes all the messages, it sets the owner to LOCKED for 10 seconds, after which it's set to NONE again.

</td></tr><tr><td>

Updated

</td><td>

Date and time the partition group was last updated.

</td></tr><tr><td>

When is the ownership lost

</td><td>

Date and time that ownership is lost.

</td></tr><tr><td>

First partition

</td><td>

Number of the first partition for the partition group.

</td></tr><tr><td>

Last partition \(inclusive\)

</td><td>

Number of the last partition for the partition group.

</td></tr><tr><td>

Input rateGiven for the last five minutes, last hour, and last 24 hours.

</td><td>

Average number of records added to the partition group per second.

</td></tr><tr><td>

Consumer processingGiven for the last five minutes, last hour, and last 24 hours.

</td><td>

Average number of messages consumed from the partition group per second.

</td></tr><tr><td>

Queue depthGiven for the last five minutes, last hour, and last 24 hours.

</td><td>

Average number of records remaining to be processed in the partition group.

</td></tr></tbody>
</table>## Stream Connect logs

The Stream Connect Logs tab displays the log entries for the associated consumer. Each log entry shows when it was created; its level, message, and source; and links to any related Alert or Subscription records. Stream Connect logs are stored in the Stream Connect Logs \[sys\_consumer\_log\] table. This table also includes logging for [producers.](producer-statistics.md)

You can enable more detailed logging in the Stream Connect logs by [adding the system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) **glide.ih.kafka.stream\_connect.debug** and setting it to **true**. To avoid filling up the logs, this property is automatically disabled after 24 hours. If you need detailed logging for longer than 24 hours, you can re-enable the property manually.

Use the **glide.ih.kafka.producer.message\_bytes\_to\_log** property to specify how many bytes of a message to display in the logs. This property only impacts logging for producers. The default value is 0, meaning no message content is logged.

## Kafka consumer statistics

The Kafka Consumer Statistics tab shows the following details.

<table id="table_s2d_ygn_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time the consumer statistics record was created.

</td></tr><tr><td>

Partition group

</td><td>

Record for the partition group.

</td></tr><tr><td>

Topic Alias

</td><td>

The topic alias for the topic associated with the consumer. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic.

</td></tr><tr><td>

Topic

</td><td>

The Hermes or Direct Kafka topic associated with the consumer.

</td></tr><tr><td>

Interval

</td><td>

Duration for the consumer statistics record, given in seconds. You can change the length of the interval with the **glide.ih.kafka.consumer.log\_interval** property. The default value is 60 seconds.

 You can specify whether to log messages to the consumer log when there are no produced or consumed Kafka messages during the interval with the **glide.ih.kafka.consumer.log\_empty\_stats** property. The default value is true.

</td></tr><tr><td>

Offset

</td><td>

Sum of all the offsets for the partition group.

</td></tr><tr><td>

End offset

</td><td>

Sum of all the end offsets for the partition group.

</td></tr><tr><td>

Lag messages

</td><td>

Difference between the end offset and the current offset.

</td></tr><tr><td>

Consumed messages

</td><td>

Number of messages processed by the consumer during the interval time.

</td></tr><tr><td>

Produced messages

</td><td>

Number of messages produced to the topic during the interval time.

</td></tr><tr><td>

Consumed bytes

</td><td>

Number of bytes processed by the consumer during the interval time.

</td></tr><tr><td>

Consumer ID

</td><td>

Unique identifier for the consumer.

</td></tr><tr><td>

Consumer Table

</td><td>

Name of the underlying consumer table. One of the following:-   Kafka Stream \[sys\_kafka\_stream\]
-   Kafka Flow Trigger \[sys\_kafka\_flow\_trigger\]

</td></tr></tbody>
</table>**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

