---
title: View Hermes Messaging Service log messages
description: Review Hermes event details by viewing log messages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/view-hermes-log-messages.html
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

    1.  Select the filter icon \(\[Omitted image "FilterIcon.png"\] Alt text: Filter icon.\).

    2.  Set a condition with a field, operator, and search string.

        For example, **\[Source\] \[contains\] \[Hermes\]**.

    3.  Select **Run**.


## Result

The Log \[syslog\] table displays only the Hermes Messaging Service log messages.

**Parent Topic:**[Administering Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-administration.md)

**Related topics**  


[Managing Hermes settings]()

[Check the status of and connection to the Hermes Kafka cluster]()

[Monitoring data usage in Hermes]()

[Tracking message usage in Hermes]()

[Cloning with Hermes Messaging Service enabled]()

