---
title: Mobile Onboarding for Android v12.5.0
description: The Android v12.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v12-5-0.html
release: mobile
topic_type: reference
last_updated: "2021-09-16"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v12.5.0

The Android v12.5.0 release provides fixes for the application.

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

 PRB1517109

</td><td>

Multi-scan fields do not work as expected for Android Agent and Now Mobile apps

</td><td>

Agents who have upgraded on an Android observe issues with scan fields. Scan fields do not pick up the scan result number.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1509940

</td><td>

Not able to hide or remove the 'Contact Live Agent' option in the mobile app

</td><td>

Users do not see 'Call Support' or 'Send Email to Customer Support'. However, they still see the 'No Chat Agents Currently Available' option in iOS. On Android devices, they still see all these three options. In a browser, users do not see any options.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1511720

</td><td>

The 'Client' theme does not apply for the chat or Virtual Agent in the Android mobile app

</td><td>

Users observe that the unmodified default color is applied to the header of the chat screen.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1507016

</td><td>

Talkback does not announce the role and disabled state for the **Clear filter** control

</td><td>

 

</td><td>

1.  Enable Talkbalk and open the app.

The login screen appears.

2.  Navigate to the 'My incident' control and activate it.

The 'My incident' screen appears.

3.  Navigate to the **Filter** button.

The 'Filter' screen appears.

4.  Complete the fields and navigate to the **Clear filter** button with a swipe gesture.

 Observe whether Talkback announces the role and disabled state for the **Clear filter** control.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1512092

</td><td>

The PIN screen switches back and forth between the original external app and the PIN screen when using a deep link

</td><td>

After clicking the deep link from an external application, it opens the PIN screen. However, sometimes it automatically closes before users can enter the PIN. On some occasions, when users enter the PIN successfully, it closes the app, and the previous external app where the link was clicked is reopened instead of the ServiceNow application.

</td><td>

1.  Open an instance and generate a deep link for mobile.
2.  Set up the Now Mobile or Agent apps with a security PIN required.
3.  Close the app on a mobile device.
4.  Click the link generated in step 1.

 Expected behavior: The PIN screen opens, and you can enter the PIN and navigate to the applet.

 Actual behavior: The PIN screen appears, but closes quickly and the ServiceNow app does not load.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1514049

</td><td>

Notification categories sometimes fail to load due to too many concurrent API requests

</td><td>

 

</td><td>

1.  Navigate to settings.
2.  Open the 'Notifications' setting.

 Observe that sometimes the categories fail to load and display.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1516586

</td><td>

An empty screen is displayed when only invisible parameters exist

</td><td>

 

</td><td>

1.  Log in to the Agent Mobile app.
2.  Click **Asset Lookup**.
3.  Complete 'ddtest' as an asset tag.
4.  Select an asset from the list.
5.  Click the three dots to open 'Assign to user'.

 Expected behavior: It should display the list.

 Actual behavior: A blank screen is visible in Android.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1517957

</td><td>

The icon text color should be a hard-coded hex value

</td><td>

In the 'Icon' section, the icon text color is based on the brand color, which causes a difference between iOS and Android apps.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

