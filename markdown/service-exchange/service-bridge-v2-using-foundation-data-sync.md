---
title: Configuring outbound foundation data sync as providers
description: As a provider, share foundational data with your consumer using foundation data sync \(FDS\).
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Configuring outbound foundation data sync as providers

As a provider, share foundational data with your consumer using foundation data sync \(FDS\).

Before using FDS, you must configure it.

<table id="table_tqf_wwj_5fc"><thead><tr><th>

Step

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1.

</td><td>

[Create an FDS Definition.](../task/service-bridge-v2-create-fds-offering-definition.md)

</td><td>

Define the data that you want to share with your consumer.After you create and publish an FDS definition, wait for your consumers to request FDS offerings based on the published definition.

</td></tr><tr><td>

2.

</td><td>

[Acknowledge FDS requests and send a sample payload.](../task/service-bridge-v2-acknowledge-FDS-request.md)

</td><td>

After receiving an FDS request from your consumer, acknowledge it and send a sample payload for each subscription.After you send the payload, your consumer configures the incoming data for each subscription and accepts it.

</td></tr><tr><td>

3.

</td><td>

[Publish subscriptions.](../task/service-bridge-v2-publish-fds-subscription.md)

</td><td>

After the consumer accepts the subscription, publish it.After the FDS configuration is complete, data starts synchronizing with the consumer based on the defined cadence.

</td></tr></tbody>
</table>**Related topics**  


[Foundation data sync](service-bridge-v2-explore-foundation-data-sync.md)

[Configuring inbound foundation data sync as a consumer](service-bridge-v2-using-foundation-data-sync-for-consumer.md)

