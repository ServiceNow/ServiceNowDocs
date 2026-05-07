---
title: Request foundation data sync offerings from a consumer
description: Request a foundation data sync \(FDS\) offering from your consumer to receive foundational data.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [foundation data sync, FDS offerings, request offering, provider inbound, receive data]
breadcrumb: [Configure inbound FDS as providers, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Request foundation data sync offerings from a consumer

Request a foundation data sync \(FDS\) offering from your consumer to receive foundational data.

## Before you begin

Role required: admin \(sb\_admin\)

## About this task

Browse and request FDS offerings that consumers have published. After you submit a request, the consumer is notified and can acknowledge your request.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Request FDS Offerings**.

2.  From the **Offerings** drop-down menu, select your consumer.

3.  From the list of offerings, select an offering.

    You can select more than one offering to request multiple datasets from the same consumer.

4.  In the Additional details section, specify the sync interval and UTC time to define the data sync schedule.

    The sync interval determines how frequently data is synchronized from the consumer instance to your provider instance.

5.  In the **Share any additional changes to the offering** field, add information about any changes you want.

    Use this field to communicate specific requirements or customizations to the consumer, such as additional field mappings or filter conditions.

6.  Select **Submit**.


## Result

A provider offering request is created. After the provider offering is created, a corresponding record is generated in your consumer's instance.

The request state displays as Received until the consumer acknowledges it. If the consumer has enabled auto-acknowledge, and you’ll receive a sample payload automatically and the state changes to Work In Progress. Otherwise, you must wait for the consumer to acknowledge your request.

## What to do next

[Validate FDS subscriptions items as a provider](service-bridge-v2-fds-validate-subs-items-provider.md)

**Related topics**  


[Foundation data sync](../concept/service-bridge-v2-explore-foundation-data-sync.md)

[Configuring inbound foundation data sync as providers](../concept/service-bridge-v2-configure-inboun-fds-providers.md)

[Configuring outbound foundation data sync as consumers](../concept/using-provider-bound-fds-consumer.md)

