---
title: General guidelines for working with data items in offline mode
description: When working with data items keep these general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-data-items-general-guidelines.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Configure data items, Supported screens, Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for working with data items in offline mode

When working with data items keep these general guidelines in mind for usability and a good user experience.

-   **Understand how data usage differs between online and offline modes**

    Consider the following differences when configuring data items.

    -   Online mode: Queries run against the entire instance, allowing users to search and access larger datasets.
    -   Offline mode: The app relies only on what was cached through data items. This is a more condense, filtered subset that you configure to verify performance, storage efficiency, and relevance.
    When configuring data items, you have control to broaden queries for online use but can restrict and fine-tune queries for offline use.

-   **Recognize cached data storage locations**

    When configuring offline mode, be aware that offline record data, user preferences \(such as favorites\), and related attachments are stored on the device's filesystem.

-   **Understand how offline data supports the application**

    Offline data keeps the app operational when the instance is unreachable. Configure offline data to support the following functionality.

    -   Display lists and record details.
    -   Enable form completion or task updates.
    -   Run business rules \(such as validations\) using cached values.
    -   Confirm the user's workflow continues seamlessly until sync resumes.
-   **Account for offline record limits in screen segments**

    Each screen segment is backed by a data item. Data items in offline mode can store up to 1,000 records. Any segment that relies on a data item only has access to the first 1,000 records that match its filter when the device is offline.

-   **Limit offline data to optimize performance and security**

    Limit the data downloaded to devices to achieve faster sync performance, reduce device storage consumption, and prevent exposure of irrelevant or sensitive records.

-   **Control downloaded data using conditions**

    Control what data is downloaded to the device by configuring data items with either declarative or scripted conditions.

    -   Declarative conditions: Configure simple field-based filters, such as restricting downloads to active records or records of a certain type. For example, open incidents assigned to me.
    -   Scripted conditions: Write logic for advanced rules that provide more flexibility, including querying multiple tables and plugins. For example, urgent work orders updated in the last 48 hours within my region.

**Parent Topic:**[Configure data items in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/config-offline-data-item.md)

