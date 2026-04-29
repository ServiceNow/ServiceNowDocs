---
title: ServiceNow Kafka Consumer
description: Integrates your ServiceNow instance with Kafka Consumer and stores data in the ServiceNow tables.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# ServiceNow Kafka Consumer

Integrates your ServiceNow instance with Kafka Consumer and stores data in the ServiceNow tables.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Confluent REST Proxy API v2.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Confluent Kafka REST Proxy Spoke](conf-kafka-spoke.md)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - RTE \(com.glide.hub.action\_step.rte\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

ServiceNow Kafka Consumer uses the connection and credential alias of the [Confluent Kafka REST Proxy Spoke](conf-kafka-spoke.md).

-   **[Configure ServiceNow Kafka Consumer](../task/setup-kafka-consumr.md)**  
Retrieve events pertaining to the specified topics and store it in the required ServiceNow tables.

**Parent Topic:**[Building integrations in Integration Hub](../../integrationhub/concept/building-integrations-ih.md)

