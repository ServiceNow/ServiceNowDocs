---
title: Mobile Classic iOS v4.2
description: The Mobile Classic iOS v4.2 release provides problem fixes.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v4.2

The Mobile Classic iOS v4.2 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Apple App Store](https://itunes.apple.com/us/app/servicenow/id1044428492?mt=8).

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

 PRB749763

</td><td>

In Geneva on iOS, the Knowledge homepage does not fully load

</td><td>

On iPhones, navigating to Knowledge home appears to start loading the Knowledge page, but it switches back to the Mobile home page.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB751837

</td><td>

Native apps should correctly scale up custom navigation bar image from custom theme

</td><td>

 

</td><td>

Upload a nav bar image that is 30x200 pixels for the mobile theme.

 Expected result: The image is scaled up to 30x200 points on retina devices.

 Actual result: The image is rendered as 30x200 pixels \(15x100 points\). This is inconsistent with the mobile web and the Android app.

</td></tr><tr><td>

Mobile

 PRB756336

</td><td>

Mobile app's user agent should include 'ServiceNow'

</td><td>

For example:

-   Android: "User-Agent: ServiceNow/2.1.0-0 \(Android 23; Samsung SM-G920V\)"
-   iOS: "User-Agent: ServiceNow/4.2.0 \(iPad; iOS 9.3.2; Scale/2.00\)"

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB759430

</td><td>

Application crashes when user tries to navigate to modules

</td><td>

This issue is specific to iOS 9.0.1 and iOS 9.0.2 devices.

 The mobile interface and tiles of favorites appear on the homescreen. However, if the user tries to select the navigation at the bottom or select one of the tiles, the application crashes.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](../classic-available-versions.md)

