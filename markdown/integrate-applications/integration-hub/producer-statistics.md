---
title: Viewing producer statistics
description: View detailed information about a Stream Connect producer and its performance, including the producer type and ID, and the total number of bytes and messages produced to a topic.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Data and Automation]
---

# Viewing producer statistics

View detailed information about a Stream Connect producer and its performance, including the producer type and ID, and the total number of bytes and messages produced to a topic.

Stream Connect producers, including the Kafka Producer step and the ProducerV2 API, publish messages from ServiceNow to a Kafka topic. You can view detailed information and statistics for each producer.

Each producer has a record that stores information about that producer, such as its type and ID. A producer might also have an associated statistics record with information about the producer's performance, including the number of bytes and messages it's produced to a topic.

Producer details and statistics are covered in two tables.

-   Kafka Producers \[sys\_kafka\_producer\] table
-   Kafka Producer Statistics \[sys\_kafka\_producer\_statistics\] table

Both tables require the Kafka Admin \[kafka\_admin\] role to view. These tables are read only and the records in them can't be manually created, updated, or deleted.

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

Topic

</td><td>

Reference to the Kafka topic record for the producer.

</td></tr><tr><td>

Domain

</td><td>

Name of the domain for the record producing the event.

</td></tr></tbody>
</table>## Kafka Producer Statistics

The Kafka Producer Statistics \[sys\_kafka\_producer\_statistics\] table captures producer statistics for each producer. Statistics are collected once per hour.

|Field|Description|
|-----|-----------|
|Topic|Reference to the topic record for the producer.|
|Collection Time|Time the producer statistics were collected. Statistics are collected and reported every hour.|
|Produced bytes|Total number of bytes produced during the collection period.|
|Produced messages|Total number of messages produced during the collection period.|
|Domain|Name of the domain for the producer.|

You can also view the statistics for a specific producer by selecting the producer's record from the table.

![A producer record showing producer statistics at the bottom.](../images/kafka-producer-statistics.png "Sample producer record with statistics")

**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

