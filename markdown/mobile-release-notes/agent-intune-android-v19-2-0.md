---
title: Mobile Agent - Intune for Android v19.2.0
description: The Android v19.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-intune-android-v19-2-0.html
release: mobile
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for Android v19.2.0

The Android v19.2.0 release provides fixes for the application.

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

 PRB1833425

</td><td>

Relative URL hyperlinks on the Activity Screen are not selectable on the Android Mobile Agent Application

</td><td>

This issue only affects Android devices. Relative URLs are selectable on iOS.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1836078

</td><td>

The app crashes while closing a Work Order Task \(WOT\)

</td><td>

The input form screen throws a null pointer exception when closing a task.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1838146

</td><td>

Client script logs are visible to all users

</td><td>

The 'Client script logs' option in the settings menu is available to all users when it should be hidden.

</td><td>

1.  Log in to an instance with Android app 19.0.0.
2.  Open Settings.

 Expected behavior: The client script logs option should be hidden.

 Actual behavior: The client script logs option is available to all users.

</td></tr><tr><td>

Mobile Android

 PRB1843310

</td><td>

Legacy parameter screen barcode scanning doesn't work

</td><td>

Attempting to scan a legacy parameter barcode doesn't work properly.

</td><td>

1.  Select the **ALP List** tab.
2.  Under the ParamListFieldType section, select **ListParamDateTime**.
3.  Select one of the scan parameters.
4.  Try to scan a barcode

 Notice that the scan doesn't work.

</td></tr><tr><td>

Mobile Android

 PRB1842617

</td><td>

The **See All** button doesn't work on large tables In Virtual Agent

</td><td>

The **See All** button doesn't work on large tables.

</td><td>

1.  Open Virtual Agent.
2.  Select a large table test topic.
3.  Tap the **See All** button after the response is generated.

 Notice that the button doesn't work.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-intune-available-versions.md)

