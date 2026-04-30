---
title: Using foundation data sync as a consumer
description: As a consumer, receive the foundation data from your provider using foundation data sync \(FDS\).
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Exchange for Consumers, Service Exchange]
---

# Using foundation data sync as a consumer

As a consumer, receive the foundation data from your provider using foundation data sync \(FDS\).

Before you use FDS, you must request and configure foundation data. After your provider creates and publishes the FDS definitions, request and configure FDS.

<table id="table_tqf_wwj_5fc"><thead><tr><th>

Step

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1.

</td><td>

[Request a foundation data offering.](../task/service-bridge-v2-request-fds-offerings.md)

</td><td>

Requests FDS offerings from your provider based on the published offerings.After you request a foundation data offering, your provider acknowledges your FDS request and sends a sample payload for each subscription.

</td></tr><tr><td>

2.

</td><td>

[Configure the sample data and validate subscription items.](../task/service-bridge-v2-validate-fds-subscription.md)

</td><td>

Configure the incoming data based on the CMDB or non-CMDB table to validate subscription items.After you validate subscription items, you must accept the subscription.

</td></tr><tr><td>

3.

</td><td>

[Accept the subscription](../task/service-bridge-v2-accept-fds-subscription.md)

</td><td>

Accept the subscription.After you accept the subscription, your provider publishes the subscription and data synchronizes according to the defined cadence.

</td></tr></tbody>
</table>**Related topics**  


[Foundation data sync](service-bridge-v2-explore-foundation-data-sync.md)

