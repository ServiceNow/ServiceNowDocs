---
title: Configure data items in offline mode
description: Define a separate data item for offline mode, giving you the flexibility to define the amount of data to display when a user is offline.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/config-offline-data-item.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Supported screens, Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure data items in offline mode

Define a separate data item for offline mode, giving you the flexibility to define the amount of data to display when a user is offline.

## Before you begin

Role required: mobile\_admin, admin

## About this task

Configure a dedicated offline data item for every screen you want to be available offline. Each offline data item defines which tables, fields, and filters are stored on the user’s device. Data Items for offline define which records are downloaded and stored on the device for offline use.

Use data items to confirm the offline cache reflects only what users need, such as their open tasks, assigned incidents, or work orders. Every data item replaces the online data item when building the cache, defining which specific data criteria is stored on the device. Data Items control which records are downloaded, refreshed, and displayed offline. Well-defined filters result in faster sync times and a smaller cache.

**Note:** Offline mode for data configuration is intended to support brief periods without connectivity; the cache isn’t designed for long-term data retention.

Use the Mobile Ofﬂine properties area to specify the type and amount of information to display to a user when they are in ofﬂine mode. For example, you can display a month’s worth of tasks in online mode and only three days’ worth in ofﬂine mode. In both online and ofﬂine modes, the data item type is always the same, and the information is extracted from the same table. For more information, see [Data items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/sg-data-item.md).

**Note:** If a data item is not created for offline mode, then the standard data item is used for both offline and online modes.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Data Item \[sys\_sg\_data\_item\]** and then either select **New** or an existing record.

5.  In the Offline Properties area, define offline mode query conditions for the data item to conform to.

    Create conditions using the Condition builder.

    **Note:** **Declarative** and **Scripts** are supported conditional types.

    Scripted data item conditions are evaluated only when the offline cache is generated. Once the data is downloaded and the user is offline, the script no longer runs. Instead, the app uses the pre-generated query string to filter the data as it was prepared at download time. For more information, see [Mobile experience capabilities available in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-capabilities.md).

6.  Select **Save**.


-   **[General guidelines for working with data items in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-data-items-general-guidelines.md)**  
When working with data items keep these general guidelines in mind for usability and a good user experience.

**Parent Topic:**[Supported screens for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/screens-offline.md)

