---
title: Offline mode setup options
description: Review the setup options to determine which configurations apply to your offline mode requirements. Each option explains what to configure and why, helping you make informed decisions. Before configuring, identify your target users, the screens they need, expected data size, and connectivity patterns such as field versus office use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/offline-setup-options.html
release: australia
topic_type: reference
last_updated: "2026-06-09"
reading_time_minutes: 4
breadcrumb: [Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Offline mode setup options

Review the setup options to determine which configurations apply to your offline mode requirements. Each option explains what to configure and why, helping you make informed decisions. Before configuring, identify your target users, the screens they need, expected data size, and connectivity patterns such as field versus office use.

## Performance and download time

A large offline setup increases download time and bandwidth consumption, which can slow cache load for users. Keeping the offline setup minimal allows for quicker setup and faster access to data. When configuring cache refresh timing, consider the following parameters.

-   Payload generation time limit: Define the time limit between 0 to 20 minutes using the parameter `glide.sg.offline.job.maxRuntime`. The default is 10 minutes.
-   Payload size limit: Payload size is unlimited, except for a maximum total size limit on attachments. For more information, see [Attachment behavior in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-attachment-behavior.md).
-   Download time limit: Download time is not controlled by the application but is governed by standard OS and network HTTP timeouts at the device, browser, or infrastructure level.

-   **Device efficiency**

    Smaller caches use less storage, memory, and battery, helping the app remain stable and responsive. Overloading the cache can slow performance and background syncs.

-   **Data freshness**

    Limiting offline content helps maintain data accuracy and relevance, helping users work with up-to-date information.

-   **User-focused experience**

    A focused offline configuration delivers only the data users need to stay productive without connectivity. A streamlined configuration improves usability and sync speed while reducing maintenance.


## Offline mode and strategy

When planning your offline mode strategy, review these setup options to learn about the various flows available for structuring your offline configuration for ServiceNow mobile apps. The setup options cover a range of considerations, from which screens and functions to display, to how the cache and data are managed while offline.

-   **1. Install and enable offline capabilities**

    For more information, see [Install and enable offline capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/enable-offline.md).

-   **2. Set up and align the app, screen, and function hierarchy**

    For more information, see [Set up and align the app, screen, and function hierarchy for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/align-app-screen-function.md).

-   **3. Configure action items and action item steps, to create, edit, and delete records while working offline**

    For more information, see [Using action items and action item steps in ofﬂine mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-action-item-steps.md).

-   **4. Configure the offline cache refresh timing on user’s device**

    For more information, see [Configure offline cache downloads to user devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-cache.md).

-   **5. Understand and configure mobile input forms for offline use**

    For more information, see [Input forms in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-input-form.md).

-   **6. Manage attachment storage to optimize offline device space**

    For more information, see [Attachment behavior in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-attachment-behavior.md).

-   **7. Configure offline security rules to match your organization's data policies**

    For more information, see [Security and compliance in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/security-offline.md).


-   **[Install and enable offline capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/enable-offline.md)**  
Configure the offline mode for your mobile app to control how and when users access data without connectivity. Users can download the cache manually, or receive it automatically based on schedules you configure.
-   **[Set up and align the app, screen, and function hierarchy for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/align-app-screen-function.md)**  
ServiceNow mobile apps are organized into three hierarchical levels, apps, screens, and functions that work together to define the mobile experience for each user role. You can configure offline mode at each level, controlling what users can access and work on without network connectivity.
-   **[Using action items and action item steps in ofﬂine mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-action-item-steps.md)**  
Action items or writeback actions are user-initiated actions that send data changes to the ServiceNow instance. While offline, writeback actions are queued and automatically synced back, once connectivity is restored.
-   **[Configure offline cache downloads to user devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-cache.md)**  
Control when and how the offline cache is refreshed on user devices to maintain relevance, performance, and bandwidth efficiency.
-   **[Input forms in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-input-form.md)**  
Input form screens in offline mode support viewing, editing, and creating records without network connectivity. The ServiceNow apps use locally cached data to display forms, populate fields, and apply form logic, so users can continue working without interruption. Well-designed offline input forms, reduce rework and minimize sync conflicts.
-   **[Attachment behavior in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-attachment-behavior.md)**  
Learn about the size and type limits applied to attachments in the offline cache.
-   **[Security and compliance in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/security-offline.md)**  
Learn how to manage offline mode access and determine which users can use it, helping to secure sensitive data.

**Parent Topic:**[Offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-offline-mode.md)

