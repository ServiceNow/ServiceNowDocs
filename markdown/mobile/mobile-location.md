---
title: Using location tracking for mobile
description: Use location tracking so that you can keep a record of your location, either for a defined period of time or while you perform tasks .
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile app settings, Using the mobile apps, Mobile Platform]
---

# Using location tracking for mobile

Use location tracking so that you can keep a record of your location, either for a defined period of time or while you perform tasks.

There are two location tracking options available, action-based and manual.

-   Action-based tracking - Starts and stops location tracking based on actions you perform.
-   Manual tracking - Starts location tracking for a defined period of time or tracks your location all the time.

Your administrator selects which tracking options are available to you. Either action-based, manual, or both. If both options are made available to you, you can select which tracking option you want to work with.

To monitor your activity, turn on location tracking from your mobile device. Location tracking continues even when there's no internet connection.

**Note:** The location setting on your mobile device takes precedence over the location setting in the mobile app. Grant permission on your mobile device to enable the app to track your location.

<table id="table_k1f_tsr_2wb"><tbody><tr><td>

-   **Enable location tracking**

Access Location tracking by tapping the  **Settings**  tab in the navigation bar, and selecting  **Location Tracking**.

On the next screen, enable the **Location tracking** option.

**Note:** You may see a prompt from your mobile device to grant location tracking permission to the mobile app. Select  **OK ** to enable geolocation tracking.

Depending on the administrator's configuration, one of the following location tracking options are available:

    -   Manual tracking option
    -   Action-based tracking option
    -   A screen enabling you to choose between manual and action-based tracking.

</td><td>

![Settings page to enable location tracking on your app.](../image/location-tracking-enable.png "Enable location tracking on your app")

</td></tr><tr><td>

-   **Set manual tracking**

Tap the **Manual tracking** option in the Location tracking screen. You have the option to either select a period of time in hours to record location tracking, or to record location tracking all the time.


</td><td>

![Location tracking manual configuration option.](../image/location-tracking-manual.png "Location tracking manual configuration")

</td></tr><tr><td>

-   **Set action-based tracking**

Tap **Action-based** to enable the action-based location tracking option.

**Note:** A message stating Tracking or Not tracking displays. This text indicates whether your mobile device is tracking at this current moment.

Action-based location tracking starts and stops when you tap on the corresponding button within a record, as defined by your administrator.


</td><td>

![Location tracking action-based tracking option.](../image/location-tracking-action.png "Location tracking action-based option")

 ![Start and Stop buttons used in action-based location tracking.](../image/location-tracking-start-stop.png "Start and Stop buttons used in action-based location tracking")

</td></tr><tr><td>

-   **Select from either tracking option**

If your administrator has enabled both options, you can select the tracking option you want to work with.


</td><td>

![Location tracking screen with both options available.](../image/location-tracking-both.png "Location tracking screen with both options available")

</td></tr></tbody>
</table>## Location tracking behavior in defined situations

-   **Location tracking behavior when logging out and in**

    When you initiate location tracking, the app saves the tracking start and end time. When the end time passes, the tracking session expires, and location tracking is turned off.

    By default, if you log out during an active location tracking session, when you log back into the same instance, the app checks if the location tracking session has expired. If the session has not expired, the location tracking session automatically resumes, until the defined end time.

-   **Location tracking behavior when overriding an active tracking session**

    If during an active location tracking session you tap another action that starts location tracking, the last tapped action overrides the existing tracking session.


