---
title: Mobile Onboarding for Android v10.0.0
description: The Android v10.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v10-0-0.html
release: mobile
topic_type: reference
last_updated: "2020-04-24"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v10.0.0

The Android v10.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

 PRB1385961

</td><td>

Images in Android are zoomed in a lot when compared with iOS in media sections

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1387935

</td><td>

The navigator.geolocation. getCurrentPosition API does not work when used in Android

</td><td>

When the API navigator. geolocation.getCurrentPosition is placed in a widget and the widget is called from an applet, the API does not work in Android. The following error message appears: 'User denied Geolocation'.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1392623

</td><td>

Updating the short description by jumping to the previous screen from the details screen does not update the list

</td><td>

 

</td><td>

1.  Open the mobile app and log in to the instance.
2.  Navigate to **ALP Form** &gt; **Form in List**.
3.  Tap on the item and tap **Update SD and Jump previous**.
4.  Fill in the text and submit.

 Notice that the list screen displays but the short description is not updated. After pulling to refresh the screen, the short description is updated.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

