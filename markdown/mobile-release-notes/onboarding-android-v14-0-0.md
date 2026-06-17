---
title: Mobile Onboarding for Android v14.0.0
description: The Android v14.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-04-07"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v14.0.0

The Android v14.0.0 release provides fixes for the application.

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

 PRB1543317

</td><td>

The ServiceNow Now Mobile app prevents camera usage from internal apps

</td><td>

Users are never prompted for camera permissions, nor is the permission forwarded to the web view, which allows the camera to be opened.

</td><td>

1.  Log in to the instance.
2.  Select the 'Services' applet.
3.  Select the 'Reservations' application.
4.  Click the QR code scanner icon.

 The QR code scanner cannot access the camera.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1560448

</td><td>

Images for categories and catalog items no longer display in the launcher screen or list screens after upgrading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1555645

</td><td>

Mobile web screen behaving incorrectly

</td><td>

Users observe that on the Now Mobile app for Android, the mobile web screen disappears when the app returns from the background.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

