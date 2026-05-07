---
title: Configuring outbound foundation data sync as consumers
description: As a consumer, share foundational data with your provider using foundation data sync \(FDS\).
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Configuring outbound foundation data sync as consumers

As a consumer, share foundational data with your provider using foundation data sync \(FDS\).

<table id="table_msw_fm4_4hc"><thead><tr><th>

Step

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1.

</td><td>

[Create an FDS Definition.](../task/service-bridge-v2-create-provider-bound-fds-consumer.md)

</td><td>

Define the data that you want to share with your provider.After you create and publish an FDS definition, wait for your provider to request FDS offerings based on the published definition.

</td></tr><tr><td>

2.

</td><td>

[Acknowledge FDS requests and send a sample payload.](../task/service-bridge-v2-con-acknowledge-fds-request.md)

</td><td>

After receiving an FDS request from your provider, acknowledge it and send a sample payload for each subscription.After you send the payload, your provider configures the incoming data for each subscription and accepts it.

</td></tr><tr><td>

3.

</td><td>

[Publish subscriptions.](../task/service-bridge-v2-publish-con-fds-subscription.md)

</td><td>

After the provider accepts the subscription, publish it.After the FDS configuration is complete, data starts synchronizing with the provider based on the defined cadence.

</td></tr></tbody>
</table>**Related topics**  


[Foundation data sync](service-bridge-v2-explore-foundation-data-sync.md)

