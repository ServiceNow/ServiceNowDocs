---
title: Supported functions for offline mode
description: Functions define the actions users can perform from a screen, such as tapping a button, icon, or menu option. In offline mode, only functions configured as available on offline are accessible to users without network connectivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/functions-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Supported functions for offline mode

Functions define the actions users can perform from a screen, such as tapping a button, icon, or menu option. In offline mode, only functions configured as available on offline are accessible to users without network connectivity.

Functions are the action layer of your mobile experience. Each function type performs a different kind of task, such as:

-   Create or update records. For example, submit a form, add a new incident, or update a work order.
-   Navigate to a list of records or a specific record. For example, navigate to another area of the app, or open a related record, list, or a specific form.
-   Add attachments to records. For example, to add, or view attachments related to a record.

Functions appear as buttons, icons, or quick actions within screens or mobile cards. Each function is configured to define what it does, when it’s visible, and which users can use it.

## How functions relate to mobile apps and offline mode

For each screen configured as available offline, enable only the functions that are relevant to offline workflows, such as creating a task, scanning a barcode, or navigating a record. This prevents users from tapping actions that require network connectivity or not required for the offline flow. Each mobile app configuration, whether for Now Mobile, Mobile Agent, or a custom app, can include its own set of screens and functions, allowing you to tailor the available actions for each app type. When defining functions, you control whether each function is available offline or restricted to online use only.

Here are some examples:

-   An Add Comment or Update Record function can be available offline; storing changes locally until the device reconnects.
-   A navigation function that opens a list screen for tasks assigned to the current user can be designated as offline, since those records are relevant and typically included in the offline payload. However, a navigation function that opens all tasks assigned to an entire group may not be suitable for offline use. Loading group-wide data would significantly increase the cache size and download data that is not relevant to the individual user.
-   Similarly, a function that navigates to a website, for example, opening a company portal or knowledge article in a browser, should not be available offline, as the website itself requires internet connectivity to load.

**Note:** For function instances, a function is available offline only when both the button instance and the button itself are configured to be available offline.

-   **[Display and hide functions in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/buttons-offline.md)**  
Define whether to show or hide buttons while users are in offline mode on their Mobile Agent app.
-   **[Configure offline mode properties for action functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/config-offline-properties-action-funct.md)**  
Determine which fields and functions are available to users when working in offline mode.
-   **[Configure offline mode properties for function instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/config-offline-property-function-instance.md)**  
Determine if the function instance available to users in online mode is also available in offline mode. This option gives you more control over how users manage their offline tasks.

**Parent Topic:**[Set up and align the app, screen, and function hierarchy for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/align-app-screen-function.md)

