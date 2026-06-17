---
title: Mobile Onboarding for Android v15.2.0
description: The Android v15.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-12-01"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v15.2.0

The Android v15.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## New feature

Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile Android \(non-classic\)

 PRB1609815

</td><td>

Font size decreases in the Android NOW mobile app after upgrading to 14.5.0 when the language is traditional Chinese

</td><td>

 

</td><td>

1.  Log in to an instance on Now Mobile with the Chinese language plugin and select the Chinese language while logging in.
2.  Navigate to any applet where the user can see the list of the records \(make sure the record is in Chinese or update the record title and description with Chinese content\).
3.  Open the record and navigate back to the list.

 Observe that the font of the opened record gets smaller.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1617100

</td><td>

Android's location tracking sessions are terminated and reset on logout \(miss-alignment with iOS\)

</td><td>

The user is required to configure a mobile property in the relevant instances. The mobile property's possible values are 'True' or 'False', with 'False' being the default value. To enable location tracking restart behavior, the mobile property should be turned on.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1596400

</td><td>

The filter buttons in 'My Approvals' are described as 'unlabelled '

</td><td>

All filter buttons contain 'unlabelled' as a description.

</td><td>

1.  Open the app and login in.
2.  Enable Talkback
3.  Select **More** &gt; **My Work** &gt; **Approvals**.
4.  Open the filter.
5.  Shift focus through filter and note issue.

 Expected behavior: Buttons are not described as unlabelled.

 Actual behavior: Buttons are described as unlabelled, e.g. 'Service Any Unlabelled'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1621875

</td><td>

The user is unable to enter composite characters on a Korean keyboard when entering text on the input form screen

</td><td>

The user can only observe composite characters by posting a work note or comment in an activity stream.

</td><td>

1.  Enable a Korean keyboard input in the device settings.

\(Note: On Samsung, navigate to **Settings** &gt; **General Management** &gt; **Samsung Keyboard settings** &gt; **Languages and types** and Change Querty to Chunjiin\)

2.  Open any input form screen.
3.  Start typing multiple characters.

 Expected behavior: Composite characters are formed.

 Actual behavior: Only a single character is allowed.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

