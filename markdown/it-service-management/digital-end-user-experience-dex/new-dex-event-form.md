---
title: New DEX event form
description: The New record form for DEX event monitoring enables you to add events to monitor.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# New DEX event form

The New record form for DEX event monitoring enables you to add events to monitor.

<table id="table_lhm_x42_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Assigns the event a name, for example "Application crash."

</td></tr><tr><td>

OS Type

</td><td>

Selects the operating system for which the event is configured:-   Windows
-   macOS

</td></tr><tr><td>

Query Type

</td><td>

Selects a message pattern used to identify the event in the log: -   Contains \(Substring\) is used for plain-text matching.
-   Regex \(Pattern Matching\) is used for regular expression matching.

</td></tr><tr><td>

Active

</td><td>

Selects to activate or deselects to make the event inactive.

</td></tr><tr><td>

Application

</td><td>

Defaults to Application and Device Health, which owns the record.

</td></tr><tr><td>

Event message

</td><td>

Identifies the message for which the event rule searches to trigger an alert.This field is optional on Windows devices, and required on macOS devices.

</td></tr><tr><td>

Domain

</td><td>

Defaults to global.The record is visible across all domains.

</td></tr><tr><td>

Log level

</td><td>

Selects the severity level of the log event being monitored, such as Debug, Error, Fault, Info, or Warning.

</td></tr><tr><td>

macOS Category

</td><td>

Selects the logging category associated with the event, used to narrow down log sources.This field only appears for the events on macOS devices.

This filed is optional. Adding a category could improve the performance and accuracy.

</td></tr><tr><td>

macOS Process

</td><td>

Selects a specific process that generates the event \(for example, kernel or loginwindow\).This field only appears for the events on macOS devices.

This field is optional. Adding a category could improve the performance and accuracy.

</td></tr><tr><td>

macOS Subsystem

</td><td>

Selects a subsystem identifier \(typically in reverse-domain notation, such as com.apple.Authorization\) used to filter logs.This field only appears for the events on macOS devices.

This filed is optional.

</td></tr><tr><td>

Windows Event ID\(s\)

</td><td>

Assigns a numeric ID used to identify the event in the Windows Event Log.This field only appears for the events on Windows devices.

This filed is required.

</td></tr><tr><td>

Windows Log Source

</td><td>

Identifies the source where the event is recorded, such as Application, System, or Security.This field only appears for the events on Windows devices.

This filed is required.

</td></tr></tbody>
</table>**Parent Topic:**[DEX Application and Device Health reference](dex-console-reference.md)

