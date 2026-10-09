---
title: Dynamic Scheduling Host release notes
description: Version history for the ServiceNow Dynamic Scheduling Host application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-dynamic-scheduling-host.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Field Service Management version history release notes, ServiceNow Store version history release notes]
---

# Dynamic Scheduling Host release notes

Version history for the ServiceNow® Dynamic Scheduling Host application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.1.1 - October 2026**
    -   Migrating this plugin com.snc.dynamic\_scheduling from Glide Family to Store
    -   This version modernizes the application's underlying technical framework of fluent SDK and dependency versions to keep the app aligned with current platform standards.
    -   Improved how territory-specific agent demand channels are factored into scheduling decisions, for both single-task and multi-task assignment scenarios.
    -   Extended demand-channel and territory association data to appointment booking capacity checks.
    -   Improved the resilience of the auto-assignment scheduling window so that temporary failures from third-party mapping and distance-calculation providers no longer disrupt the assignment process.
    -   Modernized the application's underlying technical framework and dependencies to keep the app aligned with current platform standards, with no impact in functional behavior.
    -   Fixed an issue where the Auto Assign button did not work when creating a dynamic crew.
    -   Fixed an issue where Assignment Assistance filtered out agents by territory even when the "Ignore Territory membership" setting was enabled.
    -   Fixed an issue where scheduling did not correctly account for recurrence when multiple demand records existed for the same resource within a territory.
    -   Fixed an issue where the Capacity Console failed to load after the default date format was changed.
    -   Fixed an issue that could cause nodes to restart due to an out-of-memory condition triggered by the Ready for Dispatch work order flow.
    -   Fixed intermittent scheduling errors caused by null-reference conditions in the scheduling engine.
    -   Fixed an issue where scheduled events could overlap under certain conditions.
-   **Version 30.0.9 - September 2026**
    -   Field service schedules break down constantly — a technician calls in sick, a high-priority job comes in mid-day, a route runs long. Dynamic Scheduling keeps assignments current by automatically reassigning and re-optimizing work order tasks as conditions shift, instead of leaving dispatchers to manually rework the schedule every time something changes.
    -   Administrators define the rules dynamic scheduling runs on — prioritization criteria for which tasks get scheduled first, constraints on when a task can be unassigned from a technician, and the conditions that trigger rescheduling. Dynamic Scheduling can run interactively, letting dispatchers review and approve changes, or continuously in the background as a scheduling engine that keeps assignments optimized without manual intervention.

**Parent Topic:**[ServiceNow Store - Field Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fsm-highlight.md)

