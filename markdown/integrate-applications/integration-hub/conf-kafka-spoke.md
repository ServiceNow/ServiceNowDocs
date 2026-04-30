---
title: Confluent Kafka REST Proxy Spoke
description: Integrates your ServiceNow instances with the Kafka cluster through Confluent Kafka REST Proxy API.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Confluent Kafka REST Proxy Spoke

Integrates your ServiceNow instances with the Kafka cluster through Confluent Kafka REST Proxy API.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Confluent REST Proxy API v2.

## Spoke dependencies

If you’re having trouble installing the app, ensure that the dependent plugin, ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\) is installed.

**Note:** The plugin is a licensable feature and requires appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Confluent Kafka REST Proxy spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Action|Description|
|------|-----------|
|Assign Consumer Instance to Topic Partition|Assigns a list of partitions to this consumer manually.|
|Commit Consumer Offsets|Commits a list of offsets for the consumer. When the post body is empty, all the records that have been fetched by the consumer instance are committed.|
|Create a Consumer Instance within a Consumer Group|Creates a consumer instance within Kafka consumer group.|
|Delete Consumer Instance|Destroys the consumer instance.|
|Get Kafka Partition Details For A Topic|Retrieves partition details for a Kafka topic.|
|Get Messages|Retrieves messages from a Kafka topic.|
|Publish Message|Produces messages to a Kafka topic.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Confluent Kafka REST Proxy spoke](../task/setup-kafka-spoke.md).

