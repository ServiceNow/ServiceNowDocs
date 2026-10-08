---
title: Configure rate limits for metric rules
description: Control alert volume by setting the maximum number of alerts a single metric or event rule can raise in a time window, and the total across all rules. Use rate limits to prevent alert storms and keep processing within your instance capacity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/configure-metric-rule-rate-limits.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [configure metric rule rate limit, set alert rate limit, event rule rate limit, system properties, alert volume, throttle alerts]
breadcrumb: [Metric rule rate limiting, Managing alert rules, Configure, Digital End-User Experience, IT Service Management]
---

# Configure rate limits for metric rules

Control alert volume by setting the maximum number of alerts a single metric or event rule can raise in a time window, and the total across all rules. Use rate limits to prevent alert storms and keep processing within your instance capacity.

## Before you begin

Role required: sn\_dex.admin

## About this task

The per-rule limit and the total limit are enforced independently. Review [Metric rule rate limiting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/metric-rule-rate-limiting.md) before you change either value, so that you understand which limit stops alert processing first.

## Procedure

1.  From your ServiceNow instance, navigate to **All** &gt; **All properties**.

2.  Select the **sn\_dex.per\_alert\_rule\_rate\_limit** property.

    The System Properties form opens.

3.  In the **Value** field, enter the maximum number of alerts a single rule can raise in one window.

    The default limit is 300000 every 5 mins which is the maximum/upper bound for total number of metric rule alerts.

4.  Select **Update**.

    The new value for the property is saved.

5.  Select the **sn\_dex.alert.rate\_limit** property to set the combined limit for all metric rules and event rules.


## Result

The new limits take effect in the current 5 min window.

**Note:** The value of **sn\_dex.per\_alert\_rule\_rate\_limit** for all metric or event rules doesn't exceed total rate limit defined in **sn\_dex.per\_alert\_rule\_rate\_limit**.

