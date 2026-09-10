---
title: Now Support for Android v22.1.0
description: The Android v22.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowsupport-android-v22-1-0.html
release: mobile
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v22.1.0

The Android v22.1.0 release provides fixes for the application.

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

Android Mobile

 PRB2019578

</td><td>

Barcode scanning with Bluetooth scanner is broken

</td><td>

 When using a Bluetooth barcode scanner in external scanner mode, only part of the barcode is captured.

</td><td>

1.  Navigate to the 'My Work' tab.
2.  Quick action function scan asset.
3.  Enable 'Use camera' to scan.
4.  Scan the barcode.

 Notice that barcode scanning doesn't work.

</td></tr><tr><td>

Android Mobile

 PRB2051230

</td><td>

Mobile Client Script notifications placement issue

</td><td>

When an error message is added using m\_form.addErrorMessage API, the Dismiss button on the message is not selectable. It is hidden under the bottom device menu.

</td><td>

1.  Added the error message using m\_form.addErrorMessage API.
2.  When the message is displayed, it is showing in the bottom and covered by the device menu icons. The Dismiss button of the message is not selectable.

 Expected behavior: The **Dismiss** button of the message should be selectable.

 Actual behavior: The **Dismiss** button of the message is covered by the device menu icons and is not selectable.

</td></tr><tr><td>

Android Mobile

 PRB2060857

</td><td>

ImageMaxDimensionPreset is not honored in offline mode in input form screens

</td><td>

The image is full size instead of a reduced size.

</td><td>

Provision any instance with FSM plugins installed. Make sure to set the ImageMaxDimensionPreset to 'low' mobile property on sys\_sg\_properties.LIST.

 1.  Download offline cache and go offline.
2.  In offline mode, **Open any WOT** &gt; **Log Incidental** &gt; **Add details**.
3.  Upload an attachment by taking an image from camera.
4.  Submit.
5.  Go online and sync.
6.  Navigate to the logged incidental on the instance and check the image size.

 Expected behavior: Image size must be significantly reduced \(to about 60KB or similar\). ImageMaxDimensionPreset must be honored in offline mode.

 Actual behavior: Image is full size \(size is in MB\).

</td></tr><tr><td>

Android Mobile

 PRB2051137

</td><td>

Number inputs \(Integers\) incorrectly accept dashes/hyphens between digits

</td><td>

When setting a number input value on an Input Form Screen, the input incorrectly accepts a dash or hyphen between digits.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2010062

</td><td>

An empty **Building** field appears in the parameter screen of a reservation form.

</td><td>

When editing a reservation, the user observes an empty **Building** field.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

