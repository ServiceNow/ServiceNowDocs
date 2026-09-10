---
title: Schedule Optimization release notes
description: Version history for the ServiceNow Schedule Optimization application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-schedule-optimization.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Field Service Management version history release notes, ServiceNow Store version history release notes]
---

# Schedule Optimization release notes

Version history for the ServiceNow® Schedule Optimization application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.0.2 - September 2026**
    -   New:
        -   Support for overlapping territories in Prioritized optimization — tasks and agents from overlapping territories are now considered together during optimization runs
        -   Dynamically trigger Prioritized optimization based on configurable max-agent and event-count thresholds
        -   Time-bound availability of demand channels in a territory
        -   Optional skill level support in Schedule Optimization
        -   Schedule Optimization now respects skill validity periods
        -   Shift-level visibility in run results — Run Summary and Run Detail now include optimization horizon, shift, and resource columns; new Run Summary Shift table with related lists for Agent Schedules and Work Order Tasks
    -   Fixed:
        -   Scheduled intraday flow querying events from previous days, with a hard limit of 1000 events
        -   Locked tasks not sent when window end has passed
        -   Tasks with window end beyond the optimization horizon end not considered
        -   Re-using scope from an already active batch incorrectly activating a new batch
-   **Version 29.1.7 - September 2026**
    -   New:
        -   Overlapping territory support for prioritized optimization.
        -   Admin configuration to setup minimum event count for prioritized optimization.
        -   Enhanced Schedule Optimization admin page to manage all system properties.
        -   New Matching rules for Prioritized optimization
            -   retrieve tasks based on skills, retrieve technicians based on skills, retrieve tasks within radius and retrieve technicians within radius
    -   Changed: Prioritized optimization configuration pages are reclassified from MAINT to Admin accessible.
    -   Fixed:
        -   Prioritized intraday jobs getting stuck in queued state
        -   Intraday optimization incorrectly scheduling tasks for the next day
        -   Enhanced location validation to not allow 0,0 or invalid coordinates.
        -   Fixed a race condition in run summary processing where concurrent optimization events could create duplicate run\_summary.jsonattachments on the same run summary record.
-   **Version 29.0.22 - August 2026**
    -   Fixed:
        -   Made Security enhancements on Schedule Optimization store app compatible to Australia release
        -   No Actions needed from customer while upgrading to this version
-   **Version 29.1.6 - July 2026**
    -   Fixed:
        -   Conflict task status overwrite: Unchanged tasks display correct status in Run Detail.
        -   Intraday task optimization: Corrected horizon date consideration for next-day task assignment.
        -   Dynamic Qualifier matching: Resolved cache population, deduplication, and fallback logic.
-   **Version 29.1.4 - June 2026**
    -   New:
        -   Speed up scheduling results by configuring matching rules to define which tasks and technicians are affected when a prioritized event occurs, such as identifying all technicians with matching certifications when someone calls in sick. You can enable matching rules per qualifier, then set criteria such as radius, skills, or time thresholds.
        -   Security Directive Changes to enhance cross scope access implementation
    -   Changed: The Enable assignments only with preferred/secondary agents constraint has been renamed to Enable assignments based on technician assignment preference and updated to restrict task assignment exclusively to technicians marked as required on the work order task. If no required technician is available or eligible, the task is dropped from optimization and is logged in the run summary.
-   **Version 29.0.13 - March 2026**
    -   Schedule Optimization is an advanced scheduling engine that uses Operational Research and Machine Learning models to determine the best assignment for every job — balancing technician availability, travel time, skills, priority, and SLA requirements across your entire workforce simultaneously.
    -   Most scheduling tools optimize locally. Schedule Optimization works across the full picture — fitting more jobs into working hours, routing technicians efficiently, reducing overtime, and giving priority work the placement it needs to meet commit times. When conditions change mid-day, it adapts rather than leaving dispatchers to manually rebuild the schedule.
    -   The result is a schedule that does more with the same workforce: fewer miles driven, higher first-time fix rates, less overtime, and less time dispatchers spend solving problems the system should handle automatically.

**Parent Topic:**[ServiceNow Store - Field Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fsm-highlight.md)

