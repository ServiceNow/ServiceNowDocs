---
title: View Hermes Messaging Service log messages
description: Review Hermes event details by viewing log messages.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View Hermes Messaging Service log messages

Review Hermes event details by viewing log messages.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Log** &gt; **All**.

    The Log \[syslog\] table displays all system log messages.

2.  View logs only related to Hermes by adding a filter.

    1.  Select the filter icon \(![Filter icon.](../../../product/configuration-management/image/FilterIcon.png)\).

    2.  Set a condition with a field, operator, and search string.

        For example, **\[Source\] \[contains\] \[Hermes\]**.

    3.  Select **Run**.


## Result

The Log \[syslog\] table displays only the Hermes Messaging Service log messages.

**Parent Topic:**[Administering Hermes Messaging Service](../concept/hermes-messaging-service-administration.md)

**Related topics**  


[Check the status of and connection to the Hermes Kafka cluster](run-hermes-messaging-service-diagnostics.md)

[Monitoring data usage in Hermes](../concept/monitoring-data-usage-hermes.md)

[Tracking message usage in Hermes](../concept/tracking-hermes-messaging-service-usage.md)

[Cloning with Hermes Messaging Service enabled](../concept/cloning-with-hermes-messaging-service.md)

