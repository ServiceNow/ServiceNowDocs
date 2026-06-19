---
title: General guidelines for action items synchronization behavior
description: When working with action items keep these general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/action-item-general-guideline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Action items/action steps, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for action items synchronization behavior

When working with action items keep these general guidelines in mind for usability and a good user experience.

-   **Turning off offline mode and syncing the outbox**

    To turn off offline mode and sync pending actions, use one of the following options:

    -   Navigate to **Settings** &gt; **Offline** in the mobile app and toggle **Offline Mode** to off. Alternatively, tap **Sync all** from the outbox items list.
    -   When prompted in a pop-up, select **Go Online and Sync** to upload any pending changes from the outbox.
-   **Action sequencing in the outbox**

    Write-back actions performed while offline are queued in the outbox in the order they were triggered. Once connectivity is restored, actions sync to the instance in the same sequence, ensuring consistency with the order in which they were performed.

-   **Failed sync actions**

    If a specific action fails during sync, it is marked with an error and is not retried automatically. Other queued actions continue to sync in the order they were performed.

-   **Conflict resolution for offline updates**

    Conflict handling is not managed automatically by the mobile app. The administrator is responsible for detecting and resolving conflicts on the server side. When a user performs actions offline, the mobile client sends both the changes and the timestamp of the action to the instance.

    For actions such as input forms, if server validation fails or additional input is required, the business rule error message is surfaced in the **Outbox**, allowing users to review and correct the issue directly on their device.

-   **Simultaneous offline and desktop use**

    Records aren't locked out when using offline mode. The mobile app follows the same business rules as the desktop experience and does not introduce any additional restrictions. For example, users can still add comments or work notes to an incident that has been resolved, unless a business rule explicitly prevents it. In such cases, offline mode respects those rules, ensuring consistent behavior across platforms.

-   **Timestamp handling for offline updates**

    When a user performs updates offline, each action is queued in the **Outbox** and synced to the instance in the original order once connectivity is restored, preserving the sequence and uniqueness of each status update. The timestamp of each offline action is captured and stored as a parameter of the action. During writeback action processing, this timestamp can be written into any desired field, allowing the system to reflect the actual time the action occurred offline.

    Take account of the following behavior for system fields:

    -   Custom fields can be configured to store the original offline action timestamp.
    -   Out-of-box system fields, such as `sys_created_on` and `sys_updated_on`, always reflect the integration timestamp, which is the moment the record was synced to the instance, not the original offline action time.

**Parent Topic:**[Using action items and action item steps in ofﬂine mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-action-item-steps.md)

