---
title: Field Service Contractor for mobile release notes
description: Version history for the CSM Field Service Contractor for mobile application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-field-service-contractor-mobile.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Field Service Contractor for mobile release notes

Version history for the CSM Field Service Contractor for mobile application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.8.5 - March 2026**
    -   Fixed:
        -   Corrected task assignment notifications to ensure external agents receive a single notification.
        -   This addresses an issue where duplicate notifications were sent during task assignment.
-   **Version 4.8.3 - March 2026**
    -   New:
        -   Retake previously submitted Smart Assessment questionnaires for Work order tasks in Needs Information state.
        -   Preview and sign Work Summary PDF at wok order task level.
        -   Use and Remove Part action to use asset actions APIs from Asset Management.
        -   Capability to swap parts to replace a part with new part using the Asset Actions API.
-   **Version 4.6.1 - September 2025**
    -   Use and remove part action to use asset actions APIs from Asset Management.
    -   Added swap parts action to replace a part with new part. This would also use the asset actions API
-   **Version 4.6.0 - August 2025**
    -   New:
        -   Contractor Mobile: task dependency workflow improvements
        -   We have introduced task dependency validations in the Contractor Mobile application when an agent performs the "Start Work" action.
    -   Validation behavior:
        -   Finish to Start: Agents can start work only if the predecessor task is completed. If not, an error message will be displayed and the start action will be blocked.
        -   Start Together and Start to Start: Agents cannot start work if the predecessor has not started or if there are conflicts with minimum or maximum lag times. An error message will be shown.
        -   If the maximum lag time has elapsed, the Agent can start work, and a work note will automatically be added to the successor task.
    -   The behavior depends on whether the Advanced Task Dependency plugin is installed:
        -   If the Advanced Task Dependency plugin is not installed, validations will be based on basic "Finish to Start" dependencies without considering lag times.
        -   If the Advanced Task Dependency plugin is installed, validations will cover all advanced dependency types and lag time rules.
    -   Note: This workflow is specific to Contractor Mobile and differs from the internal agent mobile experience. This is inline with contractor portal behavior.
-   **Version 4.4.0 - February 2025**

    New: Enable or Disable questionnaire based on Field Service Configuration.

-   **Version 4.1.1 - August 2024**
    -   New:
        -   Changes to support work configuration feature
        -   Notifications to contractor manager related to marketplace requests
        -   Push task to pending review sub-state when contractor closes their assigned task
            -   This is part of the quality management process
-   **Version 4.0.0 - February 2024**
    -   New:
        -   View list of requests pushed to marketplace where the contractors can participate
        -   Respond to marketplace requests
            -   Accept / Reject
            -   Respond with estimate work time, duration, cost
            -   Attach documents relevant to marketplace requests
        -   Withdraw participation from marketplace
-   **Version 3.0.0 - August 2023**
    -   New
        -   Search for work order and work order tasks
        -   Inventory workflows
            -   Pickup and drop off parts
            -   Create and source parts
        -   Native questionnaires
-   **Version 2.0.0 - February 2023**
    -   New
        -   Signature capture after task closure
        -   Preview work summary and capture signature
        -   View recently closed tasks
        -   Create work order for an asset
-   **Version 1.0.1 - November 2022**

    This mobile application allows contractor agents to manage their work assignments and debrief tasks. Contractor managers can also use this application to view all open tasks and re-assign them to contractor agents.


