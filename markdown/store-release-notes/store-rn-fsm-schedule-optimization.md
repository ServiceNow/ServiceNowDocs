---
title: Schedule Optimization release notes
description: Version history for the ServiceNow Schedule Optimization application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-schedule-optimization.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Schedule Optimization release notes

Version history for the ServiceNow® Schedule Optimization application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 29.1.4 - June 2026**
    -   New:
        -   Speed up scheduling results by configuring matching rules to define which tasks and technicians are affected when a prioritized event occurs, such as identifying all technicians with matching certifications when someone calls in sick. You can enable matching rules per qualifier, then set criteria such as radius, skills, or time thresholds.
        -   Security Directive Changes to enhance cross scope access implementation
    -   Changed: The Enable assignments only with preferred/secondary agents constraint has been renamed to Enable assignments based on technician assignment preference and updated to restrict task assignment exclusively to technicians marked as required on the work order task. If no required technician is available or eligible, the task is dropped from optimization and is logged in the run summary.
-   **Version 29.0.13 - March 2026**
    -   Schedule Optimization is an advanced scheduling engine that uses Operational Research and Machine Learning models to determine the best assignment for every job — balancing technician availability, travel time, skills, priority, and SLA requirements across your entire workforce simultaneously.
    -   Most scheduling tools optimize locally. Schedule Optimization works across the full picture — fitting more jobs into working hours, routing technicians efficiently, reducing overtime, and giving priority work the placement it needs to meet commit times. When conditions change mid-day, it adapts rather than leaving dispatchers to manually rebuild the schedule.
    -   The result is a schedule that does more with the same workforce: fewer miles driven, higher first-time fix rates, less overtime, and less time dispatchers spend solving problems the system should handle automatically.

**Parent Topic:**[ServiceNow Store - Field Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fsm-highlight.md)

