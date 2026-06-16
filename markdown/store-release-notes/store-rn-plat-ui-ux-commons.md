---
title: UX Commons release notes
description: Version history for the UX Commons application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-ux-commons.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# UX Commons release notes

Version history for the UX Commons application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.0.1 - June 2026**
    -   New:
        -   AI‑powered enhancement to the Schedule Recurrence component that lets users create complex recurring schedules using natural language. Instead of manually configuring multiple recurrence fields, users can now simply describe their schedule in plain English, and the system automatically fills in the recurrence form for them.
        -   This feature significantly reduces the time and effort required to set up recurring events, especially for complex or non‑standard recurrence patterns.
        -   Creating recurring schedules—especially with complex rules—has traditionally been error‑prone and time‑consuming. This AI enhancement makes recurrence creation:
            -   Faster – No need to understand or manually configure every recurrence rule
            -   More intuitive – Users describe what they want in natural language
            -   Less error‑prone – Structured validation ensures accuracy
            -   More accessible – Ideal for both simple and advanced scheduling scenarios
        -   This capability is a major productivity boost for teams that rely on recurring events such as meetings, shifts, reminders, and operational schedules.
        -   Availability &amp; Scope
            -   Available as part of the Schedule Recurrence component
            -   Integrated via the Recurrence Event generator AI platform skill
-   **Version 27.0.2 - August 2025**
    -   New Feature: Event Recurrence Support This release introduces robust event recurrence features that can be used in calendar and scheduling systems, enabling users to automate and manage repeating events with flexibility and precision.
    -   Key Features
        -   1. Flexible Frequency Options
            -   Daily: Repeat every day or on selected weekdays.
            -   Weekly: Schedule on specific days of the week such as, every Monday and Thursday.
            -   Monthly: Repeat by date, such as 15th of every month, or weekday such as, second Friday.
            -   Yearly: Repeats yearly for a specific month, such as Repeats yearly every January on a specific date.
        -   2. Custom Recurrence Patterns
            -   Interval-based: Recurrence every n days/weeks/months.
            -   Weekday logic: Support for rules like every third Monday or last Friday of the month. Only available in presentational layer.
        -   3. End Conditions
            -   End after N occurrences \(available only in presentational layer\).
            -   End by specific date \(on\).
            -   Never - no end date \(infinite repetition\).
        -   4. Exception Handling and Overrides
            -   Exclude Specific Dates \(e.g., holidays\).
            -   Edit Individual Occurrences without affecting the entire series.
        -   5. Summary The component creates a summary when the event details are configured.
        -   6. End Date Rules and Validations
            -   Validations to Prevent Overlap with Frequency Range:
                -   Daily: To Date must align with daily frequency window.
                -   Weekly: To Date must not exceed the specified weekly span.
                -   Monthly: Ensure To Date stays within intended monthly recurrence.
                -   Yearly: Prevent overlap across multiple years unintentionally.
    -   Accessibility
        -   WCAG 2.1 AA Compliant: Fully accessible for inclusive experiences.
        -   Localization Support: Date and time patterns adapt to regional formats.
        -   Preset and Controller Compatible: Designed to work seamlessly with or without a preset.
    -   Impact This release significantly improves the scheduling component's utility, enabling smarter automation of recurring events and reducing manual overhead for users.
-   **Version 24.6.0 - August 2024**

    Unified controller provides integration between the node map component and the CMDB Unified Map.


