---
title: Lifecycle Events logging
description: Lifecycle Events supports logging to capture events that occur in a Lifecycle Events case. Organization administrators can use the event logs that are generated to identify errors or to acquire information about the processes that ran in a Lifecycle Events case.
locale: en-US
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Lifecycle Events logging

Lifecycle Events supports logging to capture events that occur in a Lifecycle Events case. Organization administrators can use the event logs that are generated to identify errors or to acquire information about the processes that ran in a Lifecycle Events case.

The Lifecycle Events application is designed for managing HR cases that are long term in nature. These HR cases represent the different types of life cycle events that transpire during the career of a working professional. The Lifecycle Events types for which an HR case is intended are linked to significant phases in an employee's career. These Lifecycle Events types include, but aren’t limited to, onboarding, offboarding, parental leave of absence, and performance improvement plans. Each Lifecycle Events type consists of activities, such as tasks and notifications, which are grouped into activity sets. The activity sets associated with a Lifecycle Events case represent different stages in the life cycle event process and have conditions under which they’re triggered.

The many layers that comprise Lifecycle Events contribute to the application's complexity. The complexity is further compounded by its broad range of components and numerous configurable options, increasing the potential for processing error. To help Lifecycle Events administrators identify and understand the errors that surface in the application, logging can be enabled and used as a tool to diagnose problems.

## Logging components

Lifecycle Events uses the following components to record event logs for the activity associated with a Lifecycle Events case:

-   **Script includes**

    The following script includes are used to support logging:

    -   LifecycleEventLogger
    -   LifecycleEventLoggerSNC
    -   sn\_hr\_LE\_Error
-   **Table**

    Lifecycle Events records each log entry to the HR Lifecycle Events Case Logs \[sn\_hr\_le\_case\_log\] table.

-   **System property**

    The **sn\_hr\_le.log\_level** property lets you specify the types of logs that are written to the HR Lifecycle Events Case Logs table.


-   **[Enable logging for Lifecycle Events](../task/le-enable-logging.md)**  
Use the **sn\_hr\_le.log\_level** system property to enable logging for Lifecycle Events. The log entries that are generated can be used to identify errors or to acquire pertinent data about the processes that ran in a Lifecycle Events case.
-   **[View log entries for a Lifecycle Events case](../task/le-view-logs.md)**  
View the log entries associated with a Lifecycle Events case to acquire pertinent information about the processes that ran and to identify any errors that surface. The error logs can be used as a tool to diagnose problems and effectively troubleshoot the root cause of an issue that is adversely affecting a Lifecycle Events case.

**Parent Topic:**[Using Lifecycle Events](using-lifecycle-events.md)

**Related topics**  


[Lifecycle Events activity set progress optimization](le-stagnant-activity-set.md)

