---
title: Register associated records in the offline cache
description: Admins can configure offline mode to include associated records in the offline cache when a user performs an action in online mode on their Mobile Agent.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Offline mode, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Register associated records in the offline cache

Admins can configure offline mode to include associated records in the offline cache when a user performs an action in online mode on their Mobile Agent.

## Before you begin

Role required: admin

## About this task

When your ServiceNow instance has offline mode enabled, you can configure their instance to include additional records in the offline cache. Then these additional records are available when the end user is in offline mode.

**Important:** This feature is supported for scripted writeback actions only.

You must configure an action item before you can use the following steps to register associated records in the offline cache. See [Configure action items and action steps in offline mode](configure-action-item-offline.md) for information about configuring an action item.

You must use scripting to configure this task, which requires using an API.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Action item \[sys\_sg\_write\_back\_action\_item\]**, and then select the action item you created.

5.  In the **Type** field, select **Script**.

6.  In the **Execution Script** field, add the synchronization script.

    For example, the following script automatically creates a work order task when a work order is created while the end user is online. Then the work order task is available to the end user when they are in the offline mode:

    ```
    (function WriteBackAction(input) {
        //Register additional record for offline mode
        actionResult.addRecordForSync("work-order-task","ef1a8b34df113100dca6a5f59bf26327")
    })(input);
    ```

    Where `"work-order-task"` is the table to be included in the document data section of the writeback response and `"ef1a8b34df113100dca6a5f59bf26327"` is the sys\_id on the table.

    **Note:**

    -   This API can be called multiple times to register multiple records on different tables or on the same table.
    -   To specify the record that you want to include in the offline database, use the table name \(string\) and the sys\_id \(string\) of the record.
    -   The record specified by sys\_id and its associated fields appear in the document data section of the writeback response.
    -   The record specified by sys\_id is then synced with the offline database.
    -   The data that you add with this API must be encapsulated in the refreshed document or in the destination document of the writeback response. To ensure that at least a refreshed or destination document is present in your writeback response, you can configure a destination screen on the button that invokes this API. When you configure a destination screen on the button that invokes this API, your data is guaranteed to be included in the destination document.
7.  Select **Save**.


**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

