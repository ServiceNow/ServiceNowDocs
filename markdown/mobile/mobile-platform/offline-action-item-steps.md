---
title: Using action items and action item steps in ofﬂine mode
description: Action items or writeback actions are user-initiated actions that send data changes to the ServiceNow instance. While offline, writeback actions are queued and automatically synced back, once connectivity is restored.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-action-item-steps.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Using action items and action item steps in ofﬂine mode

Action items or writeback actions are user-initiated actions that send data changes to the ServiceNow instance. While offline, writeback actions are queued and automatically synced back, once connectivity is restored.

## What are writeback actions

Writeback actions can appear across various screens, including input forms, record views, and lists, and perform create, update, or delete operations on records in the database.

Examples of writeback actions:

-   **From an input form**

    Save or submit the form by creating or updating a record, add a work note or comment, or attach a photo or file.

-   **From a recprd screen**

    Accept a work order task, assign or reassign a record, or record the start or end of a shift.


## Online and offline behavior

-   **Online**

    Writeback actions execute immediately and update the instance in real time.

-   **Offline**

    Writeback actions are queued in the Outbox in the order that they were triggered. Once connectivity is restored, the Outbox syncs them back to the instance. Failed actions remain in the Outbox for review and retry.


## Multistep writeback actions

A multistep writeback action is configured once but can include steps that run in different modes, such as online, offline, or both.

The writeback action serves as the parent, containing one or more steps that can run offline, online, or both. Offline steps only affect the local database on the user's device, so any offline step that modifies local data must have a corresponding online step to update the instance database.

-   **Multistep writeback actions in online and offline**
    -   Online behavior:
        -   Executed against the live instance.
        -   Supports both declarative configurations and scripted logic.
        -   Examples: Validate a form, update a record, check related tables, and trigger a workflow.
    -   Offline behavior:
        -   Executed locally on the device against cached data.
        -   Supports only declarative configurations.
        -   Example: Update the cached version of a record and mark it for synchronization.
-   **What does the multistep action affect?**
    -   Online step affects:
        -   Updates instance data immediately.
        -   Triggers server-side logic, business rules, and workflows.
        -   Ability to run complex scripted rules across multiple tables and plugins.
    -   Offline step affects:
        -   Updates cached data only.
        -   Marks changes for later sync to the instance but reflects the changes for the user within the app and affecting workflows where this data is used while offline. For example, for filtering data in lists which show/hide buttons according to conditions.
        -   Limited to simple, rule-based validations \(no advanced scripting\).
        -   Final updates and server logic occur only after the device reconnects.
-   **When to use an offline multistep**

    You should consider using offline multistep when users need to continue working without connectivity and immediate feedback of their actions that affect workflows within the app is important also in offline. Offline steps are used for:

    -   Showing users the look and feel of their changes while offline.
    -   Applying basic record updates that don’t require complex scripting.
    -   Selecting the Save progress button in input forms stores the data locally on the user’s device.
    -   Ensuring business-critical actions remain available even in areas with poor or no network coverage.

-   **[General guidelines for action items synchronization behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/action-item-general-guideline.md)**  
When working with action items keep these general guidelines in mind for usability and a good user experience.
-   **[Configure action items and action steps in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-action-item-offline.md)**  
Configure action items to execute actions like create, edit and delete records while in offline mode. For an action item to perform multiple processes you must define separate action steps.
-   **[Offline record reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-record-reconciliation.md)**  
Configure offline mode to include associated records in the offline cache when users perform an action in online mode.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md)

