---
title: Define the number of displayed records in offline mode
description: Define the number of records to display to users in offline mode. Choose between 0 through 1000 records. This range gives you the flexibility to display different amounts to the user in online and offline modes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/config-offline-record-number.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported screens, Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Define the number of displayed records in offline mode

Define the number of records to display to users in offline mode. Choose between 0 through 1000 records. This range gives you the flexibility to display different amounts to the user in online and offline modes.

## Before you begin

Role required: mobile\_admin, admin

## About this task

Define the number of records to display in offline mode, up to a maximum of 1000 records per segment of a screen. For example, you can display the top 200 most relevant records. Limiting the number of displayed records can help prevent oversized local databases and slow device performance.

This is an example of how the number of records is calculated:

-   One record is equivalent to one row: Each top-level record counts as one row.  For example, a record from the main table used in the list.
-   Child/related records:  
    -   If child records are embedded in the main record through an association, they may contribute to the payload size. However, they don’t count as additional rows toward the 1,000-record limit.  
    -   Child records fetched separately through another data item are displayed independently, for example, as a nested list or detail view, and subject to their own caching logic and limits. They aren't counted as part of the parent screen's 1,000-record limit.

-   **Example**

    A list screen can show 1,000 work orders \(parent\) with five embedded Work Order Tasks \(child\) each within the 1000-record limit. In this scenario, the child tasks don’t count towards the row total. However, if the Work Order Tasks are configured as separate data items, they are subject to their own 1,000-record limit.


## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Screen Segment \[sys\_sg\_item\_stream\_segment\]** and then either select **New** or an existing record.

5.  In the **Max Offline Rows** field, enter a number from 0 through 1000 to be the number of displayed rows displayed in offline mode.

    **Note:** When this field is empty, the default value of 1000 rows is used.

6.  Select **Save**.


**Parent Topic:**[Supported screens for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/screens-offline.md)

