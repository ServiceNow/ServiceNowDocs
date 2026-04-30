---
title: Domain separation and Stream Connect
description: Domain separation is supported for Stream Connect. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub reference, Integration Hub, Data and Automation]
---

# Domain separation and Stream Connect

Domain separation is supported for Stream Connect. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Message replication

Records in the following Stream Connect Message Replication tables are domain separated.

-   Message Replications \[sys\_sc\_message\_replication\]
-   Channel Replications \[sys\_sc\_channel\_replication\]
-   Message Replication Statistics \[sys\_sc\_channel\_replication\_metric\]
-   Kafka Topic Replications \[sys\_kafka\_topic\_replication\]

The domain for a message replication record is specified in the record's **sys\_domain** field.

For channel replication and replication metrics records, the domain is determined by the **domain\_master** attribute. The **domain\_master** attribute uses a reference field's domain to determine the domain for the current record. A channel replication record gets its domain from the referenced message replication record. A replication metrics record gets its domain from the referenced channel replication record.

A Kafka topic replication record has the same domain as its associated channel replication record because the Channel Replications table is a parent of the Kafka Topic Replications table.

## Topic namespaces

You can use topic namespaces to configure which domains can access a Kafka topic on a domain-separated instance. In ServiceNow, Kafka topics are linked to a namespace. Namespaces can be linked to ServiceNow domains. When a namespace is assigned to a specific domain, all the topics created with that namespace are also assigned to the namespace's domain. Users can only see and interact with the topics they have access to, based on domain visibility and access control lists \(ACLs\).

For more information, see [Managing namespaces and topics in Hermes](https://www.servicenow.com/docs/access?context=managing-namespaces-topics-hermes&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Producers and consumers

Stream Connect producers and consumers are also domain separated. For producers, you can produce data only to topics that are visible to the domain.

For consumers, all the tables used to keep runtime data are domain separated. These tables include the following.

-   Kafka Streams \[sys\_kafka\_stream\]
-   Kafka Subscriptions \[sys\_kafka\_subscription\]
-   Kafka Subscription Partition Groups \[sys\_kafka\_partition\_group\]
-   Kafka Consumer Statistics \[sys\_kafka\_consumer\_statistics\]
-   Kafka Unprocessed Messages \[sys\_kafka\_unprocessed\_messages\]

Domain users can create domain-specific Kafka streams with the topics that are visible to the domain. When activating a Kafka stream, the subscription and partition groups are created within the same domain. At runtime, the domain of the partition group is set by the consumer thread so that all the data is imported to the correct domain. For more information on producers, consumers, and Kafka streams, see [Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md).

## Schema management

Tables for schemas and schema registries are domain separated. These include the following.

-   Stream Connect Schemas \[stream\_connect\_schema\]
-   Standalone Stream Connect Schema \[standalone\_stream\_connect\_schema\]
-   Confluent Stream Connect Schema \[confluent\_stream\_connect\_schema\]
-   Stream Connect Schema Registry \[stream\_connect\_schema\_registry\]
-   Confluent Stream Connect Schema \[confluent\_stream\_connect\_schema\]
-   Standalone Stream Connect Schema \[standalone\_stream\_connect\_schema\]

**Parent Topic:**[Integration Hub reference](integration-hub-reference.md)

