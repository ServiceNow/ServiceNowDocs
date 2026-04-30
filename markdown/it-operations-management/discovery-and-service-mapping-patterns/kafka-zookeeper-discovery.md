---
title: Apache Kafka and Apache Zookeeper discovery
description: ServiceNow Discovery uses the Kafka and Zookeeper discovery pattern to find Kafka data built on the Zookeeper synchronization service.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Apache Kafka and Apache Zookeeper discovery

ServiceNow Discovery uses the Kafka and Zookeeper discovery pattern to find Kafka data built on the Zookeeper synchronization service.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **CMDB CI Class Models store app**

    Verify the CMDB CI Class Models store app \(version 1.20.0\) is installed.

-   **Discovery and Service Mapping Patterns store app**

    Verify the Discovery and Service Mapping Patterns store app \(version 1.0.72\) is installed.

-   **Certificate Authority process**

    Ensure that the CA process is up and running on the host machine.

-   **Discovery credentials**

    Ensure you have the credentials for running Discovery on the host machine running the CA process​.


Kafka and Zookeeper process should be running on the host.

**Note:** Kafka Broker Discovery should run first followed by Zookeeper. In the Zookeeper Configuration file, the order of nodes forming the cluster should be consistent across all of the nodes in the cluster.

## Data collected by Discovery during horizontal discovery

|Fields|Description|
|------|-----------|
|name|Name of the CI|
|node|Node where the zookeeper is installed|
|tier|Tier of the zookeeper|
|install\_directory|Path of the install directory|
|config\_file|Path of the config file|
|config\_directory|Path of the config directory|

|Fields|Description|
|------|-----------|
|name|Name of the CI|
|isr|In Sync Replica|
|replicas|Number of replicas of the topic|
|partition\_count|Partition count of the topic|
|replication\_factor|Replication factor of the topic|

|Fields|Description|
|------|-----------|
|name|Name of the CI|
|node|Node where the zookeeper is installed|
|tier|Tier of the zookeeper|
|config\_file|Path of the config file|
|install\_directory|Path of the install|

|Fields|Description|
|------|-----------|
|Cluster\_id|Unique id specific to cluster|

|Fields|Description|
|------|-----------|
|Cluster\_id|Unique id specific to cluster|

|Fields|Description|
|------|-----------|
|Name|Name of the Node|
|Clustername|Name of the cluster the node belongs to|

|Fields|Description|
|------|-----------|
|Name|Name of the Node|
|clustername|Name of the cluster the node belongs to|

## CI Relationships

The Kafka and Zookeeper pattern does not create any CI relationships.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

