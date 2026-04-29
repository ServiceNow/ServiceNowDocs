---
title: Acknowledge foundation data sync offering request from your provider
description: Acknowledge a foundation data sync \(FDS\) offering request and send a sample payload to help your provider understand the type of data they will receive.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring outbound FDS as consumers, Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Acknowledge foundation data sync offering request from your provider

Acknowledge a foundation data sync \(FDS\) offering request and send a sample payload to help your provider understand the type of data they will receive.

## Before you begin

Role required: admin \(sb\_admin\)

## About this task

After a provider requests an FDS offering, the system generates an FDS request and corresponding FDS subscriptions in your Service Exchange instance.

If the **Auto acknowledge FDS Requests** option is not selected, you must manually acknowledge the provider's FDS request to inform them that you're working on the request. Then, send a sample payload to help them understand the type of data they will receive.

When a provider requests an FDS offering, you receive an email notification about the new request, including any required actions.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Open Records** &gt; **FDS Request**.

2.  Under **Type: Outbound**, open the FDS request by selecting the record number in the Number column.

    The FDS Request form displays details about the provider's data request.

3.  Select the **Acknowledge** button.

    The request state changes from Received to Work In Progress, and the provider is notified that you're processing their request.

4.  Send a sample payload for each subscription.

    Each sample payload contains up to five records of sample data to give providers visibility into the data structure and content they will receive.

    1.  In the Foundation Data Consumer Outbound Subscription related list, open the subscription by selecting the record number in the Number column.

    2.  Select the **Send Sample** button.

        The sample payload sent to the provider is listed in the **Sample Payload** column in the Subscription Items related list.


## Result

A sample payload for each subscription is sent to the provider as sample data. The provider can review the sample to verify the data structure and content before accepting the full data synchronization.

## What to do next

[Publish the foundation data subscription.](service-bridge-v2-publish-con-fds-subscription.md)

**Related topics**  


[Foundation data sync](../concept/service-bridge-v2-explore-foundation-data-sync.md)

[Configuring outbound foundation data sync as consumers](../concept/using-provider-bound-fds-consumer.md)

[Configuring inbound foundation data sync as providers](../concept/service-bridge-v2-configure-inboun-fds-providers.md)

