---
title: Creating entitlements in Service Exchange for Providers
description: Using consumer criteria associated with record producers and other configurations, Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create remote catalogs, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Creating entitlements in Service Exchange for Providers

Using consumer criteria associated with record producers and other configurations, Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.

Consumer Criteria records are used to entitle Service Exchange content, such as Remote Record Producers and Remote Task Definitions, to Service Exchange consumers. Consumer criteria enables you to ensure that a consumer has access only to the appropriate Service Exchange content. Using consumer criteria, you can entitle content explicitly to a single customer or to multiple customers.

A few examples of how you configure the consumer criteria are given below. For example, you can entitle content:

-   To a specific consumer.
-   To all consumers that have an active sold product of a specific model.
-   To all consumers that have an active service contract.

The Service Exchange entitlement process runs as a scheduled job each night. During the entitlement process, filters defined in the condition builder of the consumer criteria record are applied to the selected table to find records that match the condition. If a matching record is found, the associated Service Exchange content is entitled to the consumer. For example, when a consumer with an active sold product creates an order, the appropriate Service Exchange content is automatically entitled to the consumer. Entitlements are updated daily, reflecting changes if the data in the tables being queried has changed.

## Benefits

Your consumers can see and request the content entitled to them. A scheduled job runs nightly and updates the entitlements, based on any changes made to the tables or records that are queried by the consumer criteria. Additionally, entitlements are checked immediately when updates are made.

You can update Service Exchange entitlements in the following ways:

-   Define the consumer criteria in the Remote Record Producer.
-   Register a new consumer in Service Exchange.
-   Click the **Refresh Entitlements** related link in the Consumer Connections record or the Provider record.

## Define a consumer criteria

To define a consumer criteria, see [Create a consumer criteria](service-bridge-v2-create-consumer-criteria.md).

