---
title: Viewing producer statistics
description: View detailed information about a Stream Connect producer and its performance, including the producer type and ID, and the total number of bytes and messages produced to a topic.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Viewing producer statistics

View detailed information about a Stream Connect producer and its performance, including the producer type and ID, and the total number of bytes and messages produced to a topic.

Stream Connect producers, including the Kafka Producer step and the ProducerV2 API, publish messages from ServiceNow to a Kafka topic. You can view detailed information and statistics for each producer.

Each producer has a record that stores information about that producer, such as its type and ID. A producer might also have an associated statistics record with information about the producer's performance, including the number of bytes and messages it's produced to a topic.

Producer details and statistics are covered in two tables.

-   Kafka Producers \[sys\_kafka\_producer\] table
-   Kafka Producer Statistics \[sys\_kafka\_producer\_statistics\] table

Both tables require the Kafka Admin \[kafka\_admin\] role to view. These tables are read only and the records in them can't be manually created, updated, or deleted.

## Stream Connect logs

Producer logs are stored in the Consumer Logs \[sys\_consumer\_log\] table. Each log entry shows when it was created; its level, message, and source; and links to any related Alert.

You can enable more detailed logging by [adding the system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) **glide.ih.kafka.stream\_connect.debug** and setting it to **true**. To avoid filling up the logs, this property is automatically disabled after 24 hours. If you need detailed logging for longer than 24 hours, you can re-enable the property manually.

Use the **glide.ih.kafka.producer.message\_bytes\_to\_log** property to specify how many bytes of a message to display in the logs. This property only impacts logging for producers. The default value is 0, meaning no message content is logged.

## Kafka Producers table

The Kafka Producers \[sys\_kafka\_producer\] table captures producer information per topic. You can view the Kafka Producers table by navigating to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Producers**.

<table id="table_zjf_kmm_pdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifier for the producer. Links to the producer record.

</td></tr><tr><td>

Producer Type

</td><td>

Type and version number for the producer.

 Each producer type is followed by the version number of the producer. For example, if the producer is the ProducerV2 API, the type listed is SCRIPT\_V2.

 Options are:

-   ACTION: Kafka Producer step.
-   SCRIPT\_ACTION: A producer called from within a scripted step in Workflow Studio.
-   SCRIPT: Producer API or ProducerV2 API.
-   SYSTEM: Any server-side execution in the ServiceNow Platform where the system can't identify any record associated with the execution.

</td></tr><tr><td>

Producer Table

</td><td>

Name of the table producing the record.

 For example, if the record is produced by a business rule, the table is Business Rule \[sys\_script\]. If it's produced by the Kafka Producer step, it's Action Type \[sys\_hub\_action\_type\_definition\].

</td></tr><tr><td>

Producer ID

</td><td>

Reference to the record that produces the messages.

</td></tr><tr><td>

Topic Alias

</td><td>

The topic alias for the topic associated with the producer. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic.

</td></tr><tr><td>

Topic

</td><td>

Reference to the Kafka topic record for the producer.

</td></tr><tr><td>

Domain

</td><td>

Name of the domain for the record producing the event.

</td></tr><tr><td>

Created

</td><td>

Date the producer was created. Formatted as YYYY-MM-DD hh:mm:ss.

</td></tr><tr><td>

Created by

</td><td>

Name of the person that created the producer.

</td></tr><tr><td>

Updated

</td><td>

Date the producer was update. Formatted as YYYY-MM-DD hh:mm:ss.

</td></tr></tbody>
</table>## Kafka Producer Statistics

The Kafka Producer Statistics \[sys\_kafka\_producer\_statistics\] table captures producer statistics for each producer. Statistics are collected once per hour.

|Field|Description|
|-----|-----------|
|Collection Time|Time the producer statistics were collected. Statistics are collected and reported every hour.|
|Produced bytes|Total number of bytes produced during the collection period.|
|Produced messages|Total number of messages produced during the collection period.|
|Producer|Reference to the producer record.|
|Domain|Name of the domain for the producer.|

You can also view the statistics for a specific producer by selecting the producer's record from the table.

![A producer record showing producer statistics at the bottom.](../images/kafka-producer-statistics.png "Sample producer record with statistics")

**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

