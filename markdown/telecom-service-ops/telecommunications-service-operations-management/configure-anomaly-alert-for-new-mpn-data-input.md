---
title: Configure an anomaly alert for an MPN data input
description: Configure a log anomaly alert for a Mobile Private Network \(MPN\) data input that generated its own source type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-anomaly-alert-for-new-mpn-data-input.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [MPN, anomaly alert, Health Log Analytics, log anomaly alert]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure an anomaly alert for an MPN data input

Configure a log anomaly alert for a Mobile Private Network \(MPN\) data input that generated its own source type.

## Before you begin

You created a data input and, if applicable, a source type, as described in [Configure security log collection for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-security-log-collection-for-mpn.md).

Role required: tsom\_assurance\_admin

## About this task

An anomaly alert is configured for the out-of-box MPN source type and fires on Major-severity `ERROR` events with no aggregation window. If your data input generated its own source type, configure a matching alert for it.

## Procedure

1.  Navigate to **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **Define Alert** and select **Create Alert**.

2.  Select the index corresponding to the data input and source type pairing you configured.

3.  Define the filter or query for the condition to detect.

    For example, specify a severity or field value. Use the **Lexical Keywords**, **Metrics Threshold Raises**, or **Advanced Log Alert Filter** related lists if a simple filter is not sufficient.

4.  Set the trigger thresholds, then set the alert severity, name, and description.

    Trigger thresholds include the number of matches, time period, and consecutive periods.

5.  Activate the alert and validate it with a test event.

    Use **Muted Metrics** to temporarily suppress noisy conditions while you tune the alert.


**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

