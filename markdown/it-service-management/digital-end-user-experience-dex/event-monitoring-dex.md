---
title: Event monitoring with DEX
description: DEX collects and analyzes system events from managed devices so that you can detect issues, set alert thresholds, and investigate incidents faster. You can monitor system-level events across endpoints and take action before issues impact employees.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Digital End-User Experience, IT Service Management]
---

# Event monitoring with DEX

DEX collects and analyzes system events from managed devices so that you can detect issues, set alert thresholds, and investigate incidents faster. You can monitor system-level events across endpoints and take action before issues impact employees.

Event monitoring extends Digital End-User Experience \(DEX\) capabilities beyond performance metrics to include system event tracking. This feature enables you to monitor critical system events on managed Windows and macOS devices, providing deeper visibility into device health and enabling faster incident investigation.

System events are discrete, timestamped occurrences that the operating system records when something noteworthy happens on a device—for example, an application crash, a service failure, or a security-related action. Unlike performance metrics, which capture continuous measurements such as CPU utilization, events are point-in-time records that can indicate the root cause of a broader issue.

Event monitoring uses a lightweight agent-based collection process that minimizes impact on device performance while capturing critical system events.

You can configure up to 25 events for each OS type.

## Supported event types

DEX supports event monitoring on both Windows and macOS. On Windows, events are identified by a numeric Event ID from the Windows Event Log. On macOS, you define events using a regular expression that matches the system log entry of interest. For each platform, you specify the event name, Event ID or regular expression, a description, and the target operating system.

You can configure up to 25 events for each operating system type. See [Add an event to monitor](../task/add-event-to-monitor.md) to create a custom event rule.

