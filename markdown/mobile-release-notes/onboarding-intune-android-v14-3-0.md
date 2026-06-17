---
title: ServiceNow Onboarding - Intune for Android v14.3.0
description: The Android v14.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v14-3-0.html
release: mobile
topic_type: reference
last_updated: "2022-07-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v14.3.0

The Android v14.3.0 release provides fixes for the application.

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

 PRB1584841

</td><td>

Scanning does not work if a barcode has lot of small lines

</td><td>

Asset scanning does not work if there are many small lines in the bar code.

</td><td>

1.  Navigate to IT Asset Management Mobile in the OOB San Diego instance.
2.  Log in to Agent mobile app and navigate to the Asset tab.
3.  Click Asset lookup and try to scan the attached barcode.

 Observe that the barcode cannot be scanned.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1573251

</td><td>

The NOW Mobile list applet column setup does not work on Android

</td><td>

Items are stretched to the full width of the screen when a list with three columns has fewer than three items.

</td><td>

1.  Log in to a San Diego relee instance on Android.
2.  Create a **Record section** &gt; **List screen segment** &gt; **Item section** &gt; **Data item**.
3.  Add the newly created record section to any applet launcher and open the corresponding Now mobile/agent app.
4.  Under the record section, set 'Column count' and 'Wide column count' to '3'.
5.  Adjust the data item conditions in such a way that only one or two rows of data are sent to the app layer.

 Observe that the one data item spans the whole width of the screen, whereas in iOS, the data item takes up only one space as expected.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1568880

</td><td>

The clipboard is not cleared when the mobile app goes into the background

</td><td>

The clipboard should be cleared if the app is backgrounded when glide.sg.clear\_pasteboard \_when\_background is 'true', but it does not. As a result, text can be copied in certain places \(such as the activity stream\) and text cannot be copied from one place to another within the app.

</td><td>

1.  Log in to any Rome base instance.
2.  Navigate to the system property table and search for the property glide.sg.clear\_pasteboard \_when\_background.
3.  Set the value to 'true'.
4.  Log in to the Agent mobile app on and try to copy any text from the activity stream.

 Expected behavior: The user can't copy text.

 Actual behavior: The user can copy text.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

