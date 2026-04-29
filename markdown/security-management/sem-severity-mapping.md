---
title: Monitor background job health in Unified Security Exposure Management
description: The Watchdog feature monitors specified tables based on conditions that you define, helping you proactively track and respond to integration issues in Unified Security Exposure Management. When a condition is met such as an integration failure, Watchdog can notify you so you can plan remediation accordingly.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Monitor background job health in Unified Security Exposure Management

The Watchdog feature monitors specified tables based on conditions that you define, helping you proactively track and respond to integration issues in Unified Security Exposure Management. When a condition is met such as an integration failure, Watchdog can notify you so you can plan remediation accordingly.

## Default watchdogs

Three watchdogs are available out of the box:

-   **Integration run failed** Notifies users and user groups when an integration run completes with a Failed substate, indicating the run didn’t succeed.
-   **Long-running integrations**: Alerts you when an integration run exceeds its expected completion time, so you can investigate delays proactively.
-   **Overlapping periodic runs**: Detects recurring integration runs that are still in progress when their next scheduled occurrence begins, and generates a list of the affected runs.

## Watch log

The watch log tracks how many times each condition has been triggered, giving you a historical record of issues over time.

## Overview dashboard

Use the Overview dashboard to monitor Watchdog activity over the past 30 days. You can add widgets to track additional Watchdog conditions you’re monitoring. The Overview dashboard is available in the New Experience UI starting with Vulnerability Response version 19.0.

**Note:** If you are on Tokyo, you can view dashboards in the Next Experience UI with some functional limitations.

<table id="id_fm5_qkw_5sb"><tbody><tr><td>

Name

</td><td>

Description

</td></tr><tr><td>

Last 30 days WatchDog failure

</td><td>

All the conditions met in the past 30 days.

</td></tr></tbody>
</table>**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configure watchdog](../task/sem-watchdog-configure.md)

