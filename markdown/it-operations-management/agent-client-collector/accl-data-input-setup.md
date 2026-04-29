---
title: Set up additional ACC data inputs
description: Data inputs for streaming log messages to your ServiceNow instance using the Agent Client Collector are created automatically as part of the Agent Client Collector setup. Set up additional ACC data inputs manually as needed using the Health Log Analytics data input setup flow.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Set up additional ACC data inputs

Data inputs for streaming log messages to your ServiceNow instance using the Agent Client Collector are created automatically as part of the Agent Client Collector setup. Set up additional ACC data inputs manually as needed using the Health Log Analytics data input setup flow.

## Before you begin

-   The Agent Client Collector Log Analytics application has a dependency on the following ServiceNow applications, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):
    -   Health Log Analytics, Version 22.0.12 - December 2021 and later releases.
    -   Agent Client Collector -Framework, Version 2.7.0 - December 2021 and later releases.
-   Verify that a MID Server is installed and configured. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   The MID Server must be configured to work with the Agent Client Collector. For more information, see [Enable Agent Client Collector monitoring on the MID Server](acc-monitoring-setup.md).

**Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

Role required: evt\_mgmt\_admin

## About this task

It is important to configure an ACC data input for every MID Server to which Agent Client Collectors can connect, even if no agent is currently connected to it. An agent works with one MID Server at a time, but is connected to a different MID Server when necessary to provide failover protection.

**Important:** As part of the standard Health Log Analytics data input setup, you can define JavaScript functions for mapping and preprocessing raw log data. The JavaScript function must be identical for all ACC data inputs, because agents will switch to a different ACC data input when the system connects them to a different MID Server to provide failover protection. The latest published JavaScript function is provided to all existing and future ACC data inputs and replaces the previous one. This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Procedure

1.  Set up additional ACC data inputs manually using the Health Log Analytics data input setup flow.

    For more information, see [Configure ACC data inputs manually](../../health-log-analytics-admin/task/hla-data-input-acc.md).

2.  Identify and address log streaming issues to ensure that your data inputs are streaming data properly.

    For more information, see [Ensure that the data input is streaming data](accl-verify-log-streaming.md).

3.  Determine how Health Log Analytics handles raw log data that is streaming into your instance.

    By default, every incoming log line is auto-mapped to the correct tag. If properties aren't discovered automatically, map the data input sources manually by defining a JavaScript function. For more information, see [Map the raw data](../../health-log-analytics-admin/task/hla-data-input-mapping.md).

4.  Modify raw log data and drop or break up log messages before they are processed.

    Define a JavaScript function that modifies your raw log data before Health Log Analytics maps and structures it. For more information, see [Edit your raw log data before processing](../../health-log-analytics-admin/task/hla-data-input-preprocess.md).

5.  Refine the source type structure to make sure that Health Log Analytics extracts and classifies all properties correctly.

    For more information, see [Refine the source type structure in Health Log Analytics](../../health-log-analytics-admin/task/hla-source-type-structure-refine.md).


