---
title: Apache Kafka Consumer Connector
description: The Apache Kafka Consumer connector instance enables you to create events from messages collected from the Apache Kafka topic as a JSON payload that contains essential information in a data block.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Apache Kafka Consumer Connector

The Apache Kafka Consumer connector instance enables you to create events from messages collected from the Apache Kafka topic as a JSON payload that contains essential information in a data block.

Apache Kafka is a distributed publish-subscribe messaging system that receives data from disparate source systems and makes the data available to target systems in real time.

You can use this connector to create ServiceNow events from Kafka messages. Messages in the Kafka topic must be in JSON format.

Like other message broker systems, Kafka facilitates the asynchronous data exchange between processes, applications, and servers.

Kafka software runs on one or more servers. Each node, called a broker, in a Kafka cluster helps producer applications write data to topics, which are where records are stored and published. Consumer applications read from topics. Topics are divided into partitions to make them more manageable and Kafka guarantees strong ordering for each partition.

-   **[Configure the Apache Kafka Consumer connector](../task/configure-kafka-consumer-connector.md)**  
Configure the Apache Kafka Consumer connector instance to create events from streaming messages collected by the Apache Kafka connector.
-   **[Map Kafka message payload attributes to alert fields](../task/map-kafka-message-payload-attributes-to-alert-fields.md)**  
Map Kafka message attributes to alert fields to make alerts based on the messages more meaningful. Use event field mapping to map Kafka severity values to appropriate ServiceNow values.

**Parent Topic:**[Configure a pull connector](../task/t_EMConfigureConnectorInstance.md)

