---
title: Event monitoring with DEX
description: DEX collects and analyzes system events from managed devices so that you can detect issues, set alert thresholds, and investigate incidents faster. You can monitor system-level events across endpoints and take action before issues affect employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/event-monitoring-dex.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 1
breadcrumb: [Managing alert rules, Configure, Digital End-User Experience, IT Operations Management]
---

# Event monitoring with DEX

DEX collects and analyzes system events from managed devices so that you can detect issues, set alert thresholds, and investigate incidents faster. You can monitor system-level events across endpoints and take action before issues affect employees.

Event monitoring extends Digital End-User Experience \(DEX\) capabilities beyond performance metrics to include system event tracking. With this feature, you can monitor critical system events on managed Windows and macOS devices, providing deeper visibility into device health and enabling faster incident investigation.

System events are discrete, timestamped occurrences that the operating system \(OS\) records when something happens on a device. Examples include an application crash, a service failure, or a security-related action. Unlike performance metrics, which capture continuous measurements such as CPU utilization, events are point-in-time records that can indicate the root cause of a broader issue.

Event monitoring uses a lightweight agent-based collection process that minimizes impact on device performance while capturing critical system events.

You can configure up to 25 events for each OS type.

## Supported event types

DEX supports event monitoring on both Windows and macOS. On Windows, events are identified by a numeric Event ID from the Windows Event Log. On macOS, you define events using a regular expression that matches the system log entry of interest. For each platform, you specify the event name, Event ID or regular expression, a description, and the target operating system.

You can configure up to 25 events for each operating system type. To add a custom event to monitor, see [Add an event to monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/add-event-to-monitor.md).

DEX also installs a set of base system event log monitoring configurations that are active by default and count toward this limit. For the full list, see [Event log monitoring configurations installed with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/event-log-monitoring-configs-installed-with-dex.md).

