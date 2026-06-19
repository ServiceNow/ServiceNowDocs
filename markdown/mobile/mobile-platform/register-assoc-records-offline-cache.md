---
title: Register associated records in the offline cache
description: Configure a write-back action step by adding an execution script that registers newly created instance records for synchronization. Local and server-side records are then reconciled when connectivity is restored, preventing duplicate records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/register-assoc-records-offline-cache.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Offline record reconciliation, Action items/action steps, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Register associated records in the offline cache

Configure a write-back action step by adding an execution script that registers newly created instance records for synchronization. Local and server-side records are then reconciled when connectivity is restored, preventing duplicate records.

## Before you begin

Role required: mobile\_admin, admin

## About this task

When a record is created offline, it is assigned a temporary ID that needs to be matched with the permanent ID created on the server once connectivity is restored. You add the addRecordForSync\(\) method to your write-back action step so that the offline and server records are automatically linked during synchronization, preventing duplicate records.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Action item \[sys\_sg\_write\_back\_action\_item\]**, and then select the action item you created.

5.  In the **Type** field, select **Script**.

6.  In the **Execution Script** field, add the execution script, `actionResult.addRecordForSync([tableName], [sysId]);`

    For example, in the following script the write-back action creates a new time worked entry on the task\_time\_worked table. It retrieves the time worked value from the form input, creates a new record linked to the relevant task using its sys\_id, and inserts it into the instance. The addRecordForSync\(\) method is then called to associate the newly created instance record with the corresponding local record on the device, ensuring they are reconciled during the offline synchronization.

    ```
    (function WriteBackAction(parm_input,parm_variable,actionResult) { 
    
    var timeWorked = parm_input[“time_worked”]; 
    
    var gr = new GlideRecord("task_time_worked"); 
    gr.initialize(); 
    gr.task = parm_variable.task_sys_id; 
    gr.time_worked = timeWorked; 
    var newId = gr.insert(); 
    actionResult.addRecordForSync("task_time_worked", newId); 
    
    })(parm_input,parm_variable,actionResult); 
    ```

    Where:

    -   task\_time\_worked is the `tableName` that contains the record created on the instance.
    -   `newId`is the `sysId`of the record created on the instance.
    -   `actionResult`is the object on which the `addRecordForSync()`method is called.
7.  Select **Save**.


## Result

When the device reconnects and synchronization occurs:

-   The server creates the record during the online step.
-   The addRecordForSync\(\) method registers the server record as part of the action result.
-   The mobile platform reconciles the locally created record with the server-side record. The device and instance remain consistent without creating duplicate records.

**Note:** The addRecordForSync\(\) method can be called multiple times to register multiple records on different tables or on the same table.

**Parent Topic:**[Offline record reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-record-reconciliation.md)

