---
title: Working offline on ServiceNow Agent
description: When you are at a task site that doesn't have an internet connection, you can work on field service tasks, record time, track asset usage, create part requirements, and complete work orders and tasks using the ServiceNow Agent application.Download field service data to the application cache and enable mobile offline mode to execute field service tasks at locations with no internet connection. Synchronize the data when your mobile device is online again.Manage tasks, record time, track inventory, pause tasks, complete tasks, and view knowledge articles using your mobile device when you're offline.Repair an SLA to capture the device timestamp that was recorded when an SLA was closed on the ServiceNow Agent application in offline mode.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Working offline on ServiceNow Agent

When you are at a task site that doesn't have an internet connection, you can work on field service tasks, record time, track asset usage, create part requirements, and complete work orders and tasks using the ServiceNow Agent application.

## Run ServiceNow Agent in offline mode

Download field service data to the application cache and enable mobile offline mode to execute field service tasks at locations with no internet connection. Synchronize the data when your mobile device is online again.

### Before you begin

Role required: wm\_agent or wm\_dispatcher

### About this task

You can view a list of all actions taken when your device was offline and the time stamp for each action in the offline mode outbox. Generates flat data of agent schedules that are used in the mobile application for scheduled downloads of offline payloads. The administrator can also choose to download the cache automatically in the background by setting up the [system properties](../task/configure-field-service-mobile.md). This helps to at least give you one download of data at the beginning of the shift.

### Procedure

1.  Open ServiceNow Agent application.

2.  Log in to your Field Service application instance.

3.  Do the following: Tap the menu icon and select **Offline**.

    -   Tap **More**.
    -   Tap **Settings**.
    -   Tap **Offline**.
4.  To automatically download the scheduled cache in background, tap the **Enable** button.

    For more information, see Scheduled offline caching.

    Scheduled offline caching automatically downloads your cache according to your work schedule. Scheduled caching works in the background, so you can continue to use the application while the download completes. You can also enable **Wi-Fi only** to download cache when you are connected to Wi-Fi. This provides seamless synchronization when the device turns online.

5.  Do one of the following to download data and go offline.

<table id="choicetable_yld_hym_wfb"><thead><tr><th align="left" id="d48668e209">

To

</th><th align="left" id="d48668e212">

Do this

</th></tr></thead><tbody><tr><td id="d48668e218">

**Take the app offline when the data is downloaded.**

</td><td>

1.  Tap the **Offline Mode** button.
2.  Tap **Download cache &amp; go offline**.
 The app takes a few minutes to download the data and then takes the app offline. You can click **cancel** if you do not want to download data and go offline.

</td></tr><tr><td id="d48668e249">

**Manually download the data and then choose to take the app offline.**

</td><td>

1.  Tap **Download data**.
2.  After the data is downloaded:
    -   To take the app offline, tap **Go offline**.
    -   To stay online, tap **OK**.


</td></tr></tbody>
</table>6.  Update or clear cache on the mobile application.

    If you take your app online and then offline again, you can download the updated data to the app cache. You can clear the cache after you take the app online.

    -   To update the app cache, tap **Update cache**. The app reloads the data to the cache. Refer to the previous step to take the app offline.
    -   To clear the cache, tap **Clear cache**.
7.  Synchronize updated records.

<table id="choicetable_ufz_wr3_zfb"><thead><tr><th align="left" id="d48668e319">

To

</th><th align="left" id="d48668e322">

Do this

</th></tr></thead><tbody><tr><td id="d48668e328">

**Synchronize the data when your mobile device is offline**

</td><td>

1.  Tap **Outbox**.
2.  Tap **Sync**.
3.  Tap **Go Online &amp; Sync**.


</td></tr><tr><td id="d48668e359">

**Synchronize the data after your mobile device is connected online**

</td><td>

1.  Tap the **Offline Mode** button.
2.  Tap **Go Online &amp; Sync**


</td></tr></tbody>
</table>    The application synchronizes all of the data that you updated offline.


**Related topics**  


[bundle-mobile.offline-end-user]

## Working with tasks when your mobile device is offline

Manage tasks, record time, track inventory, pause tasks, complete tasks, and view knowledge articles using your mobile device when you're offline.

With your Field Service instance on your mobile device in offline mode, you can:

-   **Execute tasks assigned to you at the task location.**
    -   Start working on tasks by [accepting or rejecting tasks assigned to you.](../task/accept-reject-task-on-mobile.md)
    -   Record the time when you [start to travel to the task site or start the work on a task](../task/work-task-on-mobile.md).
-   **View knowledge articles**
    -   When you want to find information on how a similar work order task has been performed [Access knowledge articles attached to your work order task](access-information-you-need-mobile.md#).
    -   When you want to rate an article [Provide feedback for knowledge articles](access-information-you-need-mobile.md#).
-   **Track asset usage.**
    -   Tap **My Inventory** on your mobile app to view your inventory.
    -   After you work on a task [record assets used for a task](../task/use-create-asset-mobile.md).
-   **Record an incidental expense.**

    Record an incidental expense that occurred when you’re offline: [Record an incidental expense](../../planning-and-policy/task/t_RecordAnIncidentalExpense.md)

-   **Create a work order task.**

    Create, work on, and mark a task as closed complete while offline: [Create a work order task](../../planning-and-policy/task/t_CreateAWorkOrderTask.md)

-   **Pause work order tasks.**

    When you want to take a break from the task activity [pause a work order task](close-wo-wot-mobile.md#).

-   **Create a part requirement.**

    Create a new part requirement when offline: [Request inventory](request-inventory.md#)

-   **Complete work orders and work order tasks.**
    -   After you complete the work on a task [close a work order task](close-wo-wot-mobile.md#).
    -   When you finish all tasks related to a work order [complete the work order](close-wo-wot-mobile.md#).

-   **Log incidentals.**

    Report the expenses such as car rental cost, mileage, car rental cost, and vendor cost to execute the work order tasks by [logging incidentals](close-wo-wot-mobile.md#).

-   **Complete questionnaire**

    Take questionnaires when mobile is offline. For more information, see [Complete questionnaire](../task/complete-questionnaire-mobile-app.md).


You can close work order SLAs in offline mode. The Field Service mobile application records the device timestamp when the SLA was closed. After you connect your device online and synchronize the data, the SLA admin can repair the SLA to display the actual time the SLA was closed.

## Repair an SLA after closing a work order on ServiceNow Agent

Repair an SLA to capture the device timestamp that was recorded when an SLA was closed on the ServiceNow Agent application in offline mode.

### Before you begin

Role required: sla\_admin or admin

### About this task

Agents and dispatchers can close work-order SLAs when their mobile application is offline. The mobile application records the device timestamp when the SLA was closed. When the mobile application is online again and the data is synchronized, you can repair the SLA and capture that device timestamp. That reflects the actual time when the SLA was closed.

### Procedure

1.  In your desktop instance, navigate to **Field Service** &gt; **SLAs Updated Offline**.

2.  Perform one of the following actions:

    -   Select an SLA to repair.
    -   If you have more than one SLA to repair, select those SLAs.
3.  Click **Repair**.


**Related topics**  


[bundle-itsm.c_RepairSLAs]

