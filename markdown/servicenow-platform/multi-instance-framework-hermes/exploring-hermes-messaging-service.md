---
title: Exploring Hermes Messaging Service
description: Learn about the Hermes Messaging Service and how it helps you manage the flow of data between your Kafka environment and your instance.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exploring Hermes Messaging Service

Learn about the Hermes Messaging Service and how it helps you manage the flow of data between your Kafka environment and your instance.

## Hermes Messaging Service overview

Apache Kafka is an open-source data streaming platform that provides a single integration point for exchanging data across business systems in your organization. The Hermes Messaging Service enables you to integrate your Apache Kafka environment with your ServiceNow® instance to exchange data with these business systems.

The Hermes Messaging Service is a multi-tenant, multi-cluster, data transport, and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events.

-   Simplify and standardize asynchronous data transport between your Kafka environment and your ServiceNow instance.
-   Publish and process Kafka events at scale. Publish events to your Kafka environment from your ServiceNow instance and consume Kafka events from your external systems at a high volume with low latency.
-   Effectively process spikes and bursts in message volume to minimize performance impacts on your instance.
-   Manage the health and performance of message delivery using Hermes diagnostic tools.

## Components

Hermes uses the following components.

-   **Event**

    A record of something that happened, such as the creation of a log entry. Kafka uses events to transmit data between systems in near real time. An event includes a key and a value.

-   **Topic**

    A logical group of events. In Kafka, these events are transmitted as messages. Topics are used to group related events together. Events in a topic are organized using partitions.

-   **Partition**

    A topic is divided into partitions to support scalability and parallel processing. Each event is assigned to a partition based on its key. Events with the same key are always written to the same partition in order of arrival.

-   **Namespace**

    A logical grouping of topics. You can organize topics by namespace to indicate which Kafka cluster they come from. In a domain-separated instance, you can create a namespace for each domain to control access to specific topics.

-   **Hermes Kafka cluster**

    A Kafka cluster hosted in a ServiceNow data center. Hermes uses Kafka clusters to manage the delivery of messages between producers and consumers.

-   **Producer**

    A system or component that creates and sends events to a topic in the Hermes Kafka cluster. The producer sets the event key, which determines the partition where the event is stored.

-   **Consumer**

    A system or component that reads events from one or more topic partitions. Consumers process events in the order they appear within each partition. Consumers can read from multiple partitions simultaneously.


## Hermes Messaging Service users

|User|Description|
|----|-----------|
|Hermes administrator|The Hermes admin defines namespaces for each Kafka cluster or domain and creates topic records in the instance or through the command-line interface \(CLI\). The Hermes admin monitors topics and views the payload of a message in a Hermes topic using the Hermes Messaging Service topic inspector.|

## Hermes Messaging Service workflow

1.  In a domain-separated instance, the Hermes admin creates namespace records for different domains.
2.  The Hermes admin creates topic records in the instance or through the CLI.
3.  The Hermes admin updates or rescans topic records as needed in the instance.
4.  The Hermes admin monitors topics and views message payloads using the Hermes Messaging Service topic inspector.

## Benefits

Different integration points and applications in the ServiceNow platform can use the Hermes Messaging Service to publish and ingest events.

The Hermes Messaging Service is a ServiceNow AI Platform capability that is available as part of Stream Connect, Log Export Service \(LES\), and Instance Data Replication \(IDR\).

|Benefit|Application|Users|
|-------|-----------|-----|
|Export data from your ServiceNow instance to an external application using the Hermes Messaging Service with Workflow Studio.|Flow Designer|Administrator|
|Export log data securely from your instance to your external data lake for reporting, auditing, or regulatory purposes by using the Hermes Messaging Service with the Log Export Service.|Exploring Log Export Service \(LES\)|Administrator|
|Trigger flows from incoming Kafka events and trigger outgoing messages to your Kafka environment using the Hermes Messaging Service with Stream Connect.|Using Stream Connect for Apache Kafka|Administrator|
|Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading replication sets that you created prior to the Utah release to use the Hermes Messaging Service.|[Instance Data Replication](../../instance-data-replication/concept/instance-data-replication.md)|Administrator|

## Limitations

-   Maximum message size: 2 MB
-   Maximum message size per second: 2 MB \(produced or consumed\)
-   Number of topics: No limit
-   Maximum number of partitions per topic: 32 partitions
-   Maximum number of partitions: 960 \(across all external topics and internal topics used by Stream Connect, Log Export Service, and other ServiceNow® apps\)
-   Retention policy: 36 hours
-   Supported compression types for producing messages to Hermes: GZIP, LZ4, and NONE.

## What to explore next

To learn more about configuring and using the Hermes Messaging Service, see:

-   [Configuring Hermes Messaging Service](configuring-hermes-messaging-service.md)
-   [Exchanging data using Hermes](exchanging-data-hermes-messaging-service.md)
-   [Managing namespaces and topics in Hermes](managing-namespaces-topics-hermes.md)
-   [Administering Hermes Messaging Service](hermes-messaging-service-administration.md)
-   [Hermes Messaging Service reference](hermes-messaging-service-reference.md)

