---
title: Header properties detection in Health Log Analytics
description: In Health Log Analytics, automatic header properties detection separates the transport header from the inner log message and forwards only the inner log message to the source type structure. The inner message contains the actual log data without including shipping information.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, transport header, inner log message, disable header properties detection]
breadcrumb: [Log data auto-mapping and mapping, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Header properties detection in Health Log Analytics

In Health Log Analytics, automatic header properties detection separates the transport header from the inner log message and forwards only the inner log message to the source type structure. The inner message contains the actual log data without including shipping information.

The Health Log Analytics application supports header properties detection for Fluentd, Beats, and Syslog \(RFC 3164, RFC 5424\).

Starting with Version 33.0.27 - August 2024, the system also supports header properties detection for logs that follow the OpenTelemetry logs data model and semantic conventions. For more information, see the [OpenTelemetry Logs Data Model documentation](https://opentelemetry.io/docs/specs/otel/logs/data-model/).

## Disabling header properties detection

When you disable header properties detection for a data input, the Health Log Analytics AI Engine stops extracting properties from the header. Forwarding the complete raw message can be useful in the following situations:

-   The inner log message lacks information for parsing, such as timestamp and severity.
-   The data input contains information that can be used for structuring.
-   The data input forwards the logs fully parsed.

For the procedure to disable header properties detection, see [Map raw log data in Health Log Analytics](../task/hla-data-input-mapping.md).

**Parent Topic:**[Log data auto-mapping and mapping in Health Log Analytics](hla-data-input-automapping.md)

