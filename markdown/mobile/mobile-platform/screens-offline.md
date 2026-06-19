---
title: Supported screens for offline mode
description: Consider which screen types to use in offline mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/screens-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-05-31"
reading_time_minutes: 1
breadcrumb: [Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Supported screens for offline mode

Consider which screen types to use in offline mode.

## Consider which screen types to use in offline mode

Screens are the building blocks of your mobile experience. Each screen defines what information is shown, what actions are available, and how users navigate between tasks. Screen types are designed for different kinds of action.

|Screen type|Description|
|-----------|-----------|
|List screen|Browse through a list of records, such as incidents, work orders, or approvals. Tap any record to open its details.|
|Record screen|Shows the details of a single record, like a specific work order or task. Read information, view related tasks, add attachments, or post comments from this screen.|
|Input form screen|Fill in information, answer questions, or submit data through input fields, checkboxes, sliders, and more.|
|Launcher screen|Displays shortcuts, quick actions, or grouped sections of information.|

## How screens relate to mobile apps and offline mode

Each mobile app has its own configuration. Within that configuration, you decide which screens to include in the app.

Offline mode is supported in the following screens. For more information about screen types in mobile, see [Mobile screen types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/sg-mobile-applet.md).

-   Input form screen
-   List screen
-   Map screen
-   Calendar screen
-   Record screen

    The following screen segments are available within the record screen:

    -   Sections screen
    -   Related list screen
    -   Details screen
    -   Activity stream screen

-   **[Setup screens for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/setup-screens-offline.md)**  
Setup ofﬂine mode for your mobile screen so that users can work without an internet connection.
-   **[Configure data items in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/config-offline-data-item.md)**  
Define a separate data item for offline mode, giving you the flexibility to define the amount of data to display when a user is offline.
-   **[Define the number of displayed records in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/config-offline-record-number.md)**  
Define the number of records to display to users in offline mode. Choose between 0 through 1000 records. This range gives you the flexibility to display different amounts to the user in online and offline modes.

**Parent Topic:**[Set up and align the app, screen, and function hierarchy for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/align-app-screen-function.md)

