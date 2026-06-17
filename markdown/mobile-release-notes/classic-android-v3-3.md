---
title: Mobile Classic Android v3.3
description: The Mobile Classic Android v3.3 release provides problem fixes.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic Android v3.3

The Mobile Classic Android v3.3 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.servicenow&hl=en).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem category

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB1151920

</td><td>

Displaying images can lead to memory-related crashes

</td><td>

The Android app uses a lot of memory to try to normalize image rotation, which can lead to out-of-memory app crashes.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB1153065

</td><td>

Text of the 'Logout' and 'Switch Instance' buttons are not visible in light-colored themes

</td><td>

There is not an option to change the text color from the default white. White or light-colored themes make the buttons unreadable.

</td><td>

1.  Create a new mobile UI theme \(sys\_ui\_mobile\_theme record\).
2.  Change the **Navigation bar color** value to **white** \(\#FFFFFF\).
3.  Change the **glide.ui.m.mobile\_theme** property value to the sys\_id of the record created you created in step 1.
4.  Open the instance in the Android app.
5.  Click the user icon in the upper right corner.

 In the 'Session Info' box, the 'Logout' and 'Switch Instance' buttons are no longer readable.

</td></tr><tr><td>

Mobile

 PRB1153066

</td><td>

Android form screen shows "add attachment"

</td><td>

While opening the detailed record view, an intermediate attachment view is popping up before the form loads.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB1161523

</td><td>

App can crash if the webview attempts to download from an internal URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB1166703

</td><td>

Geolocation histories do not get updated

</td><td>

 

</td><td>

1.  Navigate to **Field Services** &gt; **Work Order** &gt; **Create New**.
2.  Create a work order and click **Save**.
3.  To create the work order task, click **Ready for Qualification**.
4.  Open the work order task.
5.  Assign the WOT.
6.  Open the Android mobile app and sign in as the assigned user for the WOT.
7.  Navigate to **WO Tasks Assigned to me**.
8.  Open the WOT.
9.  Click the three dots to display the menu.
10. Accept the WOT.
11. Using the desktop version, go to **Geolocation Histories**.

 Notice there are no new records being generated.

</td></tr><tr><td>

Mobile

 PRB1186524

</td><td>

Crash when showing the navigator search screen

</td><td>

When showing the navigator search, the Android app can crash in rare situations.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB1189164

</td><td>

Change the search bar text color in the navigator

</td><td>

A white navigation bar theme hides the search view text.

</td><td>

1.  Set the mobile theme navigation bar's color to **white** \(\#FFFFFF\).
2.  Open the navigator.
3.  Press the search button.
4.  Start typing.

 The text is not visible.

</td></tr><tr><td>

Mobile

 PRB1192897

</td><td>

Back button behavior in Android native mobile app is inconsistent with iOS behavior

</td><td>

When an Android user navigates from a list to a record to an activity stream, clicking the back button sends the user back to the list instead of the current record.

</td><td>

1.  Navigate to any list \(e.g. incident\).
2.  Open an incident.
3.  Click **Activity stream**.
4.  Click the app's back button.

 The user is redirected to the list instead of the current record.

</td></tr><tr><td>

Mobile

 PRB1193132

</td><td>

For reference search, magnifying glass disappears

</td><td>

Reference search does not work for reference fields. The magnifying glass disappears.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](../classic-available-versions.md)

