---
title: Mobile Onboarding for Android v15.1.0
description: The Android v15.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-11-03"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v15.1.0

The Android v15.1.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="AllOtherFixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile Android \(non-classic\)

 PRB1609551

</td><td>

On the ServiceNow Mobile Agent app for Android, a user can always delete attachments on a form

</td><td>

In iOS Agent mobile app, when attachments are added on a form screen and delete access is removed, the delete option is still visible for attachments.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1608991

</td><td>

Users are unable to toggle notification preferences on/off

</td><td>

The issue occurs when there is more than one channel with the name 'ServiceNow Mobile Application'.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1604161

</td><td>

Configuration on an icon section causes crashes on Android devices

</td><td>

When creating an icon section with the display type of anything other than 'image', and when the subsequent icon section destination record has a value set for image, background color, and foreground color, it causes the app to crash on Android devices.

</td><td>

1.  Open a San Diego instance.
2.  Open up an existing, or create, an applet launcher tab in the Now Mobile app.
3.  Create a UI section in the body with the type of 'icon section' \(sys\_sg\_navigation\_section record\).
4.  Set the display type to 'Basic'.
5.  Save.
6.  Create an 'Icon section destinations' record in the related list with the class of 'Icon section destination function'.
7.  For the 'Icon section destination function' record, set the icon, foreground, and background color to some value.
8.  Save.
9.  Open the Now Mobile app.
10. Navigate to the launcher tab.
11. Verify if it crashes.

 Expected behavior: App functions.

 Actual behavior: App crashes.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1603008

</td><td>

The **Create Event** and **Edit** functions on the 'My Schedule' screen adds seconds to the times in both Android and iOS mobile after the San Diego upgrade from Quebec

</td><td>

Android and iOS mobile clients, when submitting a write back action with a 'Parameter' screen with an input of type 'Date/Time', sends a value that includes the seconds even though in the UI the user can choose a time with a minutes precision. They shouldn't be sending seconds.

</td><td>

1.  Log in to a San Diego instance in the Agent app version.
2.  Navigate to 'My work'.
3.  Open the 'My Schedule' screen.
4.  Open the top right menu option \(three dots\).
5.  Choose **Create Event**.
6.  Populate the information on the screen.
7.  Select hours and minutes.
8.  Click **Submit**.
9.  Refresh the screen.
10. Open the event just created.

Notice the seconds in the 'Start Date Time' and 'End Date Time'. It is supposed to be 00. Instead, it adds seconds as well \(ex: 2022-09-14 17:55:09\).

11. Open the top right menu.
12. Choose **Edit**.
13. Edit the 'Start' and 'End' times.
14. Refresh.

 Expected behavior: The seconds should be set as 00.

 Actual behavior: The seconds are set to something other than 00.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1595392

</td><td>

The 'choice list' image on the 'Parameter' screen cuts-off for larger device display sizes

</td><td>

 

</td><td>

1.  Configure an instance with a 'Parameter' screen with an input of 'Choice list' that contains images.
2.  Modify the device's display size to be larger than the default.
3.  Navigate back to the choice list parameter screen.

 The image view is cut off.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

