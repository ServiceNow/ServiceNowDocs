---
title: Now Mobile for BlackBerry for Android v18.2.0
description: The Android v18.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-blackberry-android-v18-2-0.html
release: mobile
topic_type: reference
last_updated: "2024-09-10"
reading_time_minutes: 1
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for Android v18.2.0

The Android v18.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.fulfiller). Users can launch a demo to try the ServiceNow Agent app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android

 PRB1783078

</td><td>

There is a null pointer exception in the logs

</td><td>

The error in the logs reads, 'Fatal Exception: java.lang.NullPointerException: destination.itemId must not be null'.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1784293

</td><td>

The Now Agent app shows a decimal for an 'Integer' type field

</td><td>

An 'Integer' type field shows a non-decimal value in iOS, but a shows decimal value in Android.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1784823

</td><td>

The cost per unit field rounds up the values in the Android Agent app

</td><td>

When an input is mapped to a database field that contains decimals, the decimals are rounded up in Android.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-blackberry-available-versions.md)

