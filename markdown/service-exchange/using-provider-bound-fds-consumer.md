---
title: Configure outbound foundation data sync as consumers
description: Foundation data sync \(FDS\) consumers share foundational data with a provider by creating FDS definitions, acknowledging requests, and publishing subscriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/using-provider-bound-fds-consumer.html
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Configure outbound foundation data sync as consumers

Foundation data sync \(FDS\) consumers share foundational data with a provider by creating FDS definitions, acknowledging requests, and publishing subscriptions.

<table id="table_msw_fm4_4hc"><thead><tr><th>

Step

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1.

</td><td>

[Create an FDS Definition.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-create-provider-bound-fds-consumer.md)

</td><td>

Define the data that you share with your provider.After you create and publish an FDS definition, wait for your provider to request FDS offerings based on the published definition.

</td></tr><tr><td>

2.

</td><td>

[Acknowledge FDS requests and send a sample payload.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-con-acknowledge-fds-request.md)

</td><td>

After receiving an FDS request from your provider, acknowledge it and send a sample payload for each subscription. After you send the payload, your provider configures the incoming data for each subscription and accepts it.

</td></tr><tr><td>

3.

</td><td>

[Publish subscriptions.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-publish-con-fds-subscription.md)

</td><td>

After the provider accepts the subscription, publish it. After the FDS configuration is complete, data starts synchronizing with the provider based on the defined cadence.

</td></tr></tbody>
</table>**Related topics**  


[Foundation data sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-explore-foundation-data-sync.md)

