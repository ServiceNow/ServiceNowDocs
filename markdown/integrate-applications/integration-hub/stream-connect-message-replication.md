---
title: Stream Connect Message Replication
description: Replicate data between your Apache Kafka environment and ServiceNow.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Stream Connect Message Replication

Replicate data between your Apache Kafka environment and ServiceNow.

With Stream Connect Message Replication, you can configure and manage message replications directly from your ServiceNow instance.

Stream Connect Message Replication uses a MID Server or MID Server cluster to run the data replications, so you don't need to configure or host additional replication services. It also simplifies the message replication setup by automatically generating the required certificates.

## Enabling a MID Server to replicate data

Stream Connect Message Replication uses a MID Server with a replicator extension to replicate data to and from your local Kafka. For instructions on how to configure the MID Server, see [Configuring MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

The MID Server must be able to access Hermes endpoints through the firewall. Work with your network administrator to make sure that the following port ranges are open.

-   Producer: 4000–4050
-   Consumer1: 4100–4150
-   Consumer2: 4200–4250

## Using a MID Server cluster

You can use a MID Server cluster, instead of a single MID Server, for message replication. With a MID Server cluster, if one of the MID Servers in the cluster fails, the other MID Servers can share the load of the failed MID Server.

In a MID Server cluster, the topic partitions are distributed across all the available MID Servers in the cluster. If a MID Server becomes unavailable, the partitions are redistributed on the remaining MID Servers. If an additional MID Server becomes available in the cluster, then the partitions are distributed across the MID Servers again.

For details on setting up a MID Server cluster, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Note:** The MID Server cluster must have the **Load Balance** cluster type. The **Failover** cluster type is not supported.

## Configuring connections and credentials for Kafka

Stream Connect Message Replication uses a Connection &amp; Credential alias to connect to your local Kafka. To configure a Connection &amp; Credential alias:

1.  [Create Kafka credentials](../tasks/create-kafka-ssl-credentials.md) with the authentication data required for the connection.
2.  [Configure a Kafka connection](../tasks/configure-kafka-connection.md) to connect to your Kafka environment.
3.  [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US), to associate the connection information and credential data. The Connection &amp; Credential alias should have a **Connection type** of **Kafka** and must be accessible from the MID Server.

These steps are for configuring a Connection &amp; Credential alias for connecting to Kafka. You don't need to set up connections or credentials for connecting to Hermes, because the MID Server automatically handles the creation of the required keystore, truststore, and certificates.

## Creating message and topic replications

Message replication requires Message Replication records and Kafka Topic Replication records.

A Message Replication record represents a single Kafka cluster. For example, if you have two Kafka clusters, you would create two different Message Replication records, one for each cluster. A Message Replication record is the parent record for all the topics being replicated to or from that cluster. Message Replication records are stored in the Message Replications \[sys\_sc\_message\_replication\] table.

A Kafka Topic Replication record specifies the replication from a single source topic to a single destination topic. You can't replicate a single source topic to multiple destinations. You can only replicate to each destination once. Kafka Topic Replication records are stored in the Kafka Topic Replications \[sys\_kafka\_topic\_replication\] table.

For a step-by-step guide to creating message and topic replication records, see [Create message and Kafka topic replications in Stream Connect](../tasks/configure-message-topic-reps-sc.md).

## Viewing message replication statistics

Once replications are running, the system creates a metrics record for each active topic replication every 60 seconds. Metrics records provide information about topic replications, including the **Message count**, which shows the number of messages replicated in each collection interval.

You can view metrics records on the Message Replication Statistics \[sys\_sc\_channel\_replication\_metric\] table. You can also view metrics records for a particular topic by checking the Message Replication Statistics on its Kafka Topic Replication record.

For a list of message replication metrics and their descriptions, see [Viewing Stream Connect Message Replication statistics](../reference/stream-connect-message-rep-stats.md).

## Required plugin

Stream Connect Message Replication requires the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin.

## Roles

The message\_replication\_admin role can create, modify, and delete records in all the message replication tables, including the connection and credential tables, and the message and topic replication tables.

The message\_replication\_user role can view records in the message replication tables.

## Logging

Most issues are logged in the MID Server log. Additional debug logging can be enabled by setting the **glide.stream\_connect.message\_replication.debug** MID Server property to **true**.

-   **[Create message and Kafka topic replications in Stream Connect](../tasks/configure-message-topic-reps-sc.md)**  
Set up message and topic replications to replicate data between your Apache Kafka environment and ServiceNow.
-   **[Create Kafka credentials](../tasks/create-kafka-ssl-credentials.md)**  
Configure credentials for your Apache Kafka connection.
-   **[Configure a Kafka connection](../tasks/configure-kafka-connection.md)**  
Configure a connection to your Apache Kafka environment.
-   **[Viewing Stream Connect Message Replication statistics](../reference/stream-connect-message-rep-stats.md)**  
When message replications are running, the system creates a metrics record for each active topic replication every 60 seconds. Metrics records provide information about topic replications. You can view metrics records on the Message Replication Statistics \[sys\_sc\_channel\_replication\_metric\] table. You can also view metrics records for a topic by checking the Message Replication Statistics on its Kafka Topic Replication record.

**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

