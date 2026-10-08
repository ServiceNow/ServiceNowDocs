---
title: Metric rule rate limiting
description: Rate limiting controls how many alerts metric and event rules can raise within a time window. DEX enforces a per-rule limit and a combined limit across all rules, so a single rule matching more devices or events than expected doesn't overwhelm alert processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/metric-rule-rate-limiting.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [metric rule rate limiting, event rule rate limiting, alert rate limit, per metric rule limit, total rate limit, alert suppression, alert window]
breadcrumb: [Managing alert rules, Configure, Digital End-User Experience, IT Service Management]
---

# Metric rule rate limiting

Rate limiting controls how many alerts metric and event rules can raise within a time window. DEX enforces a per-rule limit and a combined limit across all rules, so a single rule matching more devices or events than expected doesn't overwhelm alert processing.

A metric rule raises an alert every time its criteria are met. When a rule applies to many devices or applications, or when one condition affects many users, the rule might generate more alerts than your team can act on. Rate limiting bounds that volume.

DEX counts the alert requests each rule makes during a window and compares that count against two separate limits. Both limits are enforced independently, and reaching either one stops further alerts until the window closes.

-   **Per-rule rate limit**

    Each metric rule and event rule carries its own limit. DEX tracks the alert count for a rule against the end of the current window. Rate limiting helps prevent one noisy rule from consuming the capacity that the rest of your rules need.

    The per-rule count resets when the window closes.

-   **Total rate limit**

    The total rate limit applies to all metric rules and event rules combined. Even when no individual rule has reached its own limit, alert processing stops for the remainder of the window after the combined count reaches the total limit.


When the limit is reached, the alert rule is dropped and an error is recorded.

To set the limits, see [Configure rate limits for metric rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configure-metric-rule-rate-limits.md).

A separate control caps how many metric rules you can create, rather than how many alerts they raise. For that control, see "Define threshold for handling user metric rules."

For general information about metric rules, see [Using alert rules for Digital End-User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/metric-rules.md).

