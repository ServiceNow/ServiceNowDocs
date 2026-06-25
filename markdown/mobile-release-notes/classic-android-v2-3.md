---
title: Mobile Classic Android v2.3
description: The Mobile Classic Android v2.3 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-android-v2-3.html
release: mobile
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic Android v2.3

The Mobile Classic Android v2.3 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.servicenow&hl=en).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB802370

</td><td>

HTML in journal fields displays tags on native apps

</td><td>

When HTML code blocks are used in activity stream journal fields, the native applications do not render the HTML. Instead, the HTML tags are displayed as inline text.

</td><td>

1.  Create an HTML code block within an activity stream.
2.  View that activity stream from the native mobile applications.

 Expected result: The HTML tags are stripped from the text block, leaving only "human readable" text.

 Actual result: The HTML tags are displayed inline.

</td></tr><tr><td>

Mobile

 PRB819268

</td><td>

Android app does not update Location Timestamp when the Check In feature is used

</td><td>

When the Check In feature is used, the Android app does not send the Location Timestamp when location is updated on the sys\_mobile\_devices table.

</td><td>

Using the Android app:

 1.  Share your location with the "Check In" feature.
2.  Navigate to the sys\_mobile\_devices record for the Android device.

 Expected result: Location Timestamp is updated.

 Actual result: Location Timestamp is not updated.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

