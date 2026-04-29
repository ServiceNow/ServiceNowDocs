---
title: Accept a foundation data sync \(FDS\) subscription as a provider
description: Accept a foundation data sync \(FDS\) subscription to complete the FDS configuration and begin receiving data from the consumer.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [foundation data sync, FDS subscription, accept subscription, provider inbound, activate sync]
breadcrumb: [Configure inbound FDS as providers, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Accept a foundation data sync \(FDS\) subscription as a provider

Accept a foundation data sync \(FDS\) subscription to complete the FDS configuration and begin receiving data from the consumer.

## Before you begin

Role required: admin \(sb\_admin\)

## About this task

After the subscription items are validated, you must accept the subscription to complete the FDS configuration and activate data synchronization.

If the consumer has enabled auto-publish for the subscription, accepting it will automatically publish the subscription and begin data synchronization. Otherwise, your consumer need to manually publish the subscription before data sync begins.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Open Records** &gt; **FDS Requests**.

2.  In the **Type: Inbound**, select the request.

3.  From the Foundation Data Provider Inbound Subscriptions related list, open the provider subscription by selecting the record number in the **Number** column.

4.  Select **Accept**.

    If you reject the subscription by selecting **Reject**, your consumer needs to resend the sample files, and you must reconfigure the subscription items before you can accept the subscription again.


## Result

If the consumer has enabled auto-publish, the subscription automatically moves to Active state and data synchronization begins immediately. Otherwise, the subscription remains in Accepted state until the consumer manually publishes it.

**Related topics**  


[Foundation data sync](../concept/service-bridge-v2-explore-foundation-data-sync.md)

[Configuring inbound foundation data sync as providers](../concept/service-bridge-v2-configure-inboun-fds-providers.md)

[Configuring outbound foundation data sync as consumers](../concept/using-provider-bound-fds-consumer.md)

