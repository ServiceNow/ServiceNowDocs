---
title: Publish an outbound FDS subscription as a consumer
description: Publish the foundation data sync \(FDS\) subscription to complete the foundation data sync after the provider configures and accepts the subscription.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring outbound FDS as consumers, Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Publish an outbound FDS subscription as a consumer

Publish the foundation data sync \(FDS\) subscription to complete the foundation data sync after the provider configures and accepts the subscription.

## Before you begin

Role required: admin \(sb\_admin\)

## About this task

If the **Auto publish FDS subscriptions** option is not selected in your offering definition, you must manually publish each subscription after the provider accepts the subscriptions.

Publishing the subscription activates the data synchronization process and begins sending data to the provider according to the defined cadence.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Open Records** &gt; **FDS Request**.

2.  Open the FDS request by selecting the record number in the **Number** column.

3.  In the Foundation Data Consumer Outbound Subscriptions related list, open the foundation data subscription by selecting the record number in the **Number** column.

    Each subscription represents a specific table or data set that the provider has requested.

4.  Select **Publish**.

    You must publish each subscription that is accepted by your provider to activate the subscription and begin data synchronization.

    The subscription state changes to Published.


## Result

The foundation data subscription is now active. Data is synchronized to the provider instance based on the defined cadence and filter criteria.

**Related topics**  


[Foundation data sync](../concept/service-bridge-v2-explore-foundation-data-sync.md)

[Configuring outbound foundation data sync as consumers](../concept/using-provider-bound-fds-consumer.md)

[Configuring inbound foundation data sync as providers](../concept/service-bridge-v2-configure-inboun-fds-providers.md)

