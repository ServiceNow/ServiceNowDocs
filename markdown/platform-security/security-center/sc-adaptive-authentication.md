---
title: Adaptive authentication Security Metrics
description: Use authentication policies to evaluate authentication requests and deny or allow access to your instance based on the specified policy conditions.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security metrics, Security monitoring console, Security Center, Platform Security]
---

# Adaptive authentication Security Metrics

Use authentication policies to evaluate authentication requests and deny or allow access to your instance based on the specified policy conditions.

Adaptive authentication metrics enable you to monitor how adaptive authentication is being used on your instance. View a summary of all of your metrics on Adaptive authentication, individual metrics such as policy result rates or denied IP addresses. This page requires the Adaptive Authentication \(**com.snc.adaptive\_authentication**\) plugin for adaptive authentication to be available in your instance. You must enable Authentication Policy to see the metrics. See [Activate adaptive authentication](../../../integrate/authentication/task/adaptive-authentication-plugin.md) and [Configure adaptive authentication properties](../../../integrate/authentication/task/configure-adaptive-auth-properties.md) for more details.

**Note:** This feature was released with version 1.2.

-   Policy result rates: All the successful and failed adaptive authentication events.
-   Event failure distribution: All the failed events for each event type.
-   Event success distribution: The successful events associated with every event type.
-   Denied IP addresses: The number of IP addresses blocked by the instance, along with their associated data.
-   Authenticated user logins: The number of events counted for each event type, excluding the pre-login event.
-   API user logins: The number of events associated with API Authentication policies for each event type.
-   Authentication trend: The total number of events recorded.
-   Authenticated users: The number of users counted for each event type, excluding the pre-login event.

Select the cards to view the individual metrics page with additional details.

Select the **+Create task** button to create a Security Task related to a metric. For details on Security Tasks, see [Security Tasks](security-task-manager.md).

**Parent Topic:**[Security metrics](sc-metrics.md)

