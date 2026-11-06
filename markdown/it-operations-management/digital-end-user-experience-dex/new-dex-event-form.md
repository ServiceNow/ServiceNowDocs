---
title: New DEX event form
description: The New record form for DEX event monitoring enables you to add events to monitor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/new-dex-event-form.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Operations Management]
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

Name of the event, for example, "Application crash."

</td></tr><tr><td>

OS Type

</td><td>

Operating system for which the event is configured:-   Windows
-   macOS

</td></tr><tr><td>

Query Type

</td><td>

Message pattern used to identify the event in the log: -   Contains \(Substring\) is used for plain-text matching.
-   Regex \(Pattern Matching\) is used for regular expression matching.

</td></tr><tr><td>

Active

</td><td>

Option that activates the event when selected. When the check box is cleared, the event is inactive.

</td></tr><tr><td>

Application

</td><td>

Application that owns the record. The default is Application and Device Health.

</td></tr><tr><td>

Event message

</td><td>

Message for which the event rule searches to trigger an alert.This field is optional on Windows devices, and required on macOS devices.

</td></tr><tr><td>

Domain

</td><td>

Domain of the record. The default is global.The record is visible across all domains.

</td></tr><tr><td>

Log level

</td><td>

Severity level of the log event being monitored, such as Debug, Error, Fault, Info, or Warning.

</td></tr><tr><td>

macOS Category

</td><td>

Logging category associated with the event, used to narrow down log sources.This field only appears for the events on macOS devices.

Adding a category can improve performance and accuracy.

</td></tr><tr><td>

macOS Process

</td><td>

Specific process that generates the event \(for example, kernel or loginwindow\).This field only appears for the events on macOS devices.

Adding a process can improve performance and accuracy.

</td></tr><tr><td>

macOS Subsystem

</td><td>

Subsystem identifier \(typically in reverse-domain notation, such as com.apple.Authorization\) used to filter logs.This field only appears for the events on macOS devices.

</td></tr><tr><td>

Windows Event ID\(s\)

</td><td>

Numeric ID used to identify the event in the Windows Event Log.This field only appears for the events on Windows devices.

</td></tr><tr><td>

Windows Log Source

</td><td>

Source where the event is recorded, such as Application, System, or Security.This field only appears for the events on Windows devices.

</td></tr></tbody>
</table>**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-console-reference.md)

