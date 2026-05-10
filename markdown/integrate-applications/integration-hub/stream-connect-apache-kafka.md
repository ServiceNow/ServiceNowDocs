---
title: Using Stream Connect for Apache Kafka
description: Connect your Apache Kafka environment to your ServiceNow instance with Stream Connect for Apache Kafka.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Using Stream Connect for Apache Kafka

Connect your Apache Kafka environment to your ServiceNow instance with Stream Connect for Apache Kafka.

Apache Kafka is a distributed event-streaming platform that provides a unified way to exchange data across multiple systems. Stream Connect for Apache Kafka links your Kafka environment to your ServiceNow instance, enabling you to stream data between your instance and your external systems.

**Note:** Stream Connect requires an Workflow Data Fabric subscription and a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

## Benefits

-   Publish and process Kafka events at scale. Publish events to your Kafka environment from your ServiceNow instance and consume Kafka events from your external systems at a high volume with low latency.

-   Build flows that produce and consume Kafka events. Stream Connect is integrated with Workflow Studio, providing a low-code way to publish and process Kafka messages.
-   Import data from your Kafka environment and process that data using your existing Robust Transform Engine \(RTE\) or transform map configurations.
-   Configure a consumer that uses your own scripts to process data from a Kafka topic.
-   Monitor your consumers' performance with detailed reporting of statistics and performance metrics.
-   Integrate your on-premise ServiceNow instance with your local Kafka environment with Direct Kafka.

## Terminology

Stream Connect uses the following terms.

-   **Producers**

    A producer publishes events to a Kafka environment. Stream Connect has two producers.

    -   Kafka Producer step in Workflow Studio
    -   ProducerV2 API
-   **Consumers**

    A consumer reads and processes events from a Kafka environment. Stream Connect has several consumers.

    -   Kafka Message trigger in Workflow Studio
    -   Extract Transform Load \(ETL\) Consumer
    -   Transform Map Consumer
    -   Script Consumer
-   **Topics and topic namespaces**

    Events are organized and stored in topics. A topic stores events of the same type. Topics are partitioned. Events have a key. Events with the same key are stored in the same partition.

    Topics link to a topic namespace. You can use namespaces to organize topics in logical ways. For example, you can group topics together based on which Kafka cluster they come from. You can also use namespaces to configure which domains can access which topics on a domain-separated instance. For more information, see [Managing namespaces and topics in Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/managing-namespaces-topics-hermes.md).

-   **Topic aliases**

    A [topic alias](manage-topic-alias.md#) is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and connected to a different underlying topic on each instance.

-   **Subscriptions**

    A subscription is a record associated with a consumer. It stores configuration information about the consumer, such as the name of the Kafka topic to consume messages from and the number of partitions the topic has. The subscription record is created when a Kafka stream is activated.

    Each subscription record has several metrics that enable you to view the performance of the consumer reading from the topic. For more information, see [Viewing Kafka subscriptions and statistics](kafka-subscriptions-statistics.md).

-   **Partition groups**

    A partition group is a set of topic partitions. For example, if a topic has six partitions, they can be divided into three partition groups, with two partitions in each group.

-   **Kafka consumer job**

    A job that regularly checks Hermes for any new events in a topic. The job picks a free partition group and retrieves its subscription. The subscription gives the topic name, and the job checks the partitions for messages for that topic.

-   **Kafka streams**

    A Kafka stream is a record that defines the data stream for a consumer. If you're using the Kafka Message trigger in Workflow Studio, the Kafka stream is automatically created for you. If you're using a different consumer, you’ll need to create one manually.


To link your Kafka environment to your ServiceNow instance, Stream Connect uses the Hermes Messaging Service. The Hermes Messaging Service enables your instance to produce and consume large volumes of Kafka events. It manages the flow of data between your Kafka environment and your instance. For more information, see [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service.md).

The following diagram shows some of the key components of Stream Connect.

![Diagram showing an overview of Stream Connect components.](../images/stream-connect.png "Stream Connect overview")

## Using Guided Setup for Stream Connect

Guided Setup provides a sequence of tasks that can help you configure Stream Connect. To open Guided Setup, navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Guided Setup**.

For more information about using the guided setup interface, see [Using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-setup.md).

## Stream Connect and Workflow Studio

Build flows that produce and consume Kafka events with Stream Connect and Workflow Studio. Stream Connect has a flow trigger for consuming Kafka events and an action step for producing them.

Use the [Kafka Message trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow-kafka.md) to create flows that process Kafka events. You can build a flow that consumes data from Kafka and inserts it into a table, or uses spokes to communicate the data to third-party environments.

The trigger is enabled when the flow is activated. After it's activated, the trigger starts the flow whenever there's a message in the specified Kafka topic. When you use the Kafka Message trigger, you don't need to create a Kafka stream or subscription record. The system automatically creates both when the flow is activated. Messages are read from the topic as long as the flow is active.

Use the [Kafka Producer step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/kafka-producer-action-designer.md) to create actions that publish events to a topic in your Kafka environment. For example, you can use the step to create a message about an update on an incident in ServiceNow, then push the message to a topic in your Kafka environment.

## Direct Kafka

Integrate your on-premise ServiceNow instance with your local Kafka environment with [Direct Kafka](direct-kafka.md#). Build efficient integrations between your enterprise systems, enabling high-volume and robust integrations to exchange data between applications, and reduce data loss with the queuing mechanism if one environment is temporarily offline.

With Direct Kafka, you can configure a custom Kafka connection to integrate Stream Connect on your on-premise instance with your local Kafka environment. This connection enables you to use Stream Connect and its features directly, without requiring the Hermes Messaging Service or a separate message replicator.

## Stream Connect alerting

Receive alerts and alert notifications for Stream Connect integrations. Stream Connect uses both active and scheduled monitoring to detect events across multiple components. If an issue is detected, the system creates an alert, logs a message to the Stream Connect Log, and sends out an alert notification. For details, see [Stream Connect alerting](stream-connect-alert.md).

## Support for messages in an Avro format

Import and create schemas to send and receive messages in an Apache Avro format. Using an Avro format can reduce the size of the payload and simplify your integration to your local Kafka instance.

You can import Avro schemas directly from the Confluent Registry, or you can create your own schemas using a JSON file or a JSON-formatted string. The schemas are stored in ServiceNow and enable your producers and consumers to convert plain-text messages to an Avro format and back. For details, see [Schema management in Stream Connect](schema-management.md).

## ETL, Transform Map, and Script Consumers

Import data from your Kafka environment using your existing RTE or transform map configurations. The Extract Transform Load \(ETL\) and Transform Map consumers simplify your data imports by providing an efficient way to take a payload from a Kafka message, transform the data, and insert or update a record in a table. You can switch from a scheduled data import to one using Stream Connect and process the data with the same configurations.

You can also use the Script Consumer to process data from your Kafka environment. The Script consumer is for more advanced use cases, such as when the data in the message isn't structured, or it requires data lookups using code.

When you [Configure an Extract Transform Load \(ETL\) consumer](../tasks/configure-etl-consumer.md), [Configure a Transform Map consumer](../tasks/configure-transform-map-consumer.md), or [Configure a script consumer](../tasks/configure-script-consumer.md), you also need to [Create a Kafka stream](../tasks/create-kafka-stream.md).

## ProducerV2 API

Publish events to a Kafka topic with the [ProducerV2 API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ProducerV2ScopedAPI.md).

## Stream Connect Message Replication

You can replicate data between your Kafka environment and ServiceNow with Stream Connect Message Replication.

Stream Connect Message Replication enables you to configure and manage message replications directly from your ServiceNow instance. It uses a MID Server or MID Server cluster to run the data replications, so you don't need to configure or host additional replication services. It also simplifies the message replication setup by automatically generating the required certificates.

For more information, see [Stream Connect Message Replication](stream-connect-message-replication.md).

## Stream Connect logs

Log messages for producers and consumers are stored in the Stream Connect Logs \[sys\_consumer\_log\] table. Each log entry shows when the log was created; its level, message, and source; and links to any related Alert or Subscription records.

You can enable more detailed logging by [adding the system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) **glide.ih.kafka.stream\_connect.debug** and setting it to **true**. To avoid filling up the logs, this property is automatically disabled after 24 hours. If you need detailed logging for longer than 24 hours, you can re-enable the property manually.

## Unprocessed and undelivered messages

If a message can't be delivered, it’s stored in the Kafka Undelivered Messages \[sys\_kafka\_undelivered\_messages\] table. A scheduled job, Kafka Producer Retry, regularly reads this table and tries to redeliver any messages.

If a batch of messages can't be processed because it has timed out, it’s stored in the Kafka Unprocessed Messages \[sys\_kafka\_unprocessed\_messages\] table. The time-out for a message batch can be set with the **com.glide.kafka\_consumer.timeout** property. The default value is 60 seconds. This table is a rotated table, so it cleans records automatically.

## Producer compression formats

Specify a compression format for Stream Connect producers with the **com.glide.kafka\_producer.compression\_type** system property. It supports the following values:

-   NONE
-   GZIP
-   LZ4

This property is not in the System Properties \[sys\_properties\] table by default, so it must be [added manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md). This property sets the compression format for all Stream Connect producers.

**Note:** To consume a compressed message, it must have been compressed using GZIP or LZ4.

## Domain separation

Use Stream Connect topic namespaces to configure which domains can access a Kafka topic on a domain-separated instance. Group topics into ServiceNow namespaces, then link the namespaces to specific domains. For more information, see [Domain separation and Stream Connect](domain-separation-stream-connect.md).

## Architecture diagram

The following diagram shows key components of Stream Connect, how they relate to ServiceNow and third-party applications, and how they connect to your Kafka environment through Hermes.

![Diagram showing Stream Connect components and how they relate to Kafka, ServiceNow, and the Hermes Messaging Service.](../images/stream-connect-architecture.png "Stream Connect architecture diagram")

## Plugin

Stream Connect requires the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin. This plugin enables the licensed components for working with message-based streaming data in Stream Connect.

## Example use case

A telecommunications company monitors millions of networks, devices, and facilities-operations systems and equipment. The monitoring systems generate millions of alerts that need to be processed and responded to in order to maintain fully operational networks.

The messages are internally pushed from the monitoring sources to their Kafka environment. From there, they are replicated to the ServiceNow Hermes Kafka cluster. This triggers script consumers that read in the messages and parse the data in the headers, keys, and payloads to efficiently enter new records into the Event table.

The related TSOM product capabilities process the event data, quickly and efficiently creating incidents and field work orders for resolution of the issue, resulting in reduced time to resolution of the issue.

![Stream Connect example import diagram.](../images/sc-example-import.png)

-   **Key assumptions and decision criteria**
    -   The data volume is incremental and frequent.
    -   The data includes messages about a variety of devices from a variety of tools.
    -   Clarify if the data only includes elements from the primary record, or if it also includes elements from related records.
    -   Confirm if the data import is associated with a process automation.
-   **Guidance**
    -   Define topics with a naming convention to clearly direct the processing of the messages. For example, if the data is coming from a Solarwinds monitoring tool source, the topic might be named sn\_streamconnect.solarwinds. Topics can be found in the navigator under **Hermes Messaging Service** &gt; **Topics**.

        ![Stream Connect example screenshot that shows a Kafka topic named sn_streamconnect.solarwinds.](../images/sc-example-name.png)

    -   When producing messages to Kafka \(and replicating to Hermes\), define and utilize keys to ensure the order of delivery and processing of messages. For example, to ensure messages are kept in order, use the device ID as the key value to keep them together for processing.
    -   Utilize headers, keys, and payload attributes to enable scaling and effective parsing of incoming messages from multiple sources.
    -   Utilize a Script Consumer or Flow Trigger Consumer for the ingest of transactional data. Following the example, the script consumer could be named similarly, such as “Solarwinds script consumer”. Script consumers can be found in the navigator under **IntegrationHub** &gt; **Consumers** &gt; **Script Consumers**.

        ![Stream Connect example screenshot showing a Kafka script consumer record.](../images/sc-example-script.png)

    -   The script consumer script parses the message content to identify what device the message was related to and processes it accordingly.

        ![Stream Connect example screenshot showing code creating a ServiceNow Event table record.](../images/sc-example-code.png)

        **Note:** The above code is a partial, representative example focused on ingesting and parsing the message data to populate table records. It's intended to be helpful in guiding an implementation.


-   **[Stream Connect Message Replication](stream-connect-message-replication.md)**  
Replicate data between your Apache Kafka environment and ServiceNow.
-   **[Stream Connect alerting](stream-connect-alert.md)**  
Receive alerts and alert notifications for Stream Connect integrations.
-   **[Using the Stream Connect Dashboard](stream-connect-dashboard.md)**  
View detailed statistics for your Stream Connect integrations. Manage producers and consumers, view data usage, and create or edit topics and replicators with the ServiceNow® Stream Connect dashboard.
-   **[Schema management in Stream Connect](schema-management.md)**  
Import and create schemas to send and receive messages in an Apache Avro format. Using an Avro format can reduce the size of the payload and simplify your integration to your local Kafka instance.
-   **[Configure an Extract Transform Load \(ETL\) consumer](../tasks/configure-etl-consumer.md)**  
Import and process data from your Kafka environment using your existing Robust Transform Engine \(RTE\) configurations.
-   **[Configure a Transform Map consumer](../tasks/configure-transform-map-consumer.md)**  
Import and process data from your Kafka environment using your existing transform map configurations.
-   **[Configure a script consumer](../tasks/configure-script-consumer.md)**  
Use a script to import and process data from your Kafka environment.
-   **[Create a Kafka stream](../tasks/create-kafka-stream.md)**  
Define a data stream for an Extract Transform Load \(ETL\), Transform Map, or Script consumer. A Kafka stream defines the stream of data to your consumer.
-   **[Viewing Kafka subscriptions and statistics](kafka-subscriptions-statistics.md)**  
View detailed information about a Kafka consumer and its performance, including the number of records added to the topic, the number of records processed, and the number of records remaining to be processed.
-   **[Viewing producer statistics](producer-statistics.md)**  
View detailed information about a Stream Connect producer and its performance, including the producer type and ID, and the total number of bytes and messages produced to a topic.

**Parent Topic:**[Importing and streaming data in Integration Hub](importing-streaming-data-ih.md)

