---
title: ServiceNow Onboarding - Intune for Android v13.3.0
description: The Android v13.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v13-3-0.html
release: mobile
topic_type: reference
last_updated: "2022-01-13"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v13.3.0

The Android v13.3.0 release provides fixes for the application.

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

 PRB1529644

</td><td>

Geolocation tracking service failed to call startForeground\(\)

</td><td>

 

</td><td>

Toggle the background location service setting on and off on an Android device.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1542455

</td><td>

'Mailto' in the Now Mobile app throws an invalid URL error on Android devices

</td><td>

 

</td><td>

1.  Open the instance.
2.  Navigate to 'Services' and search for 'apple'.
3.  Select any Apple catalog item.
4.  Select **mailto:&lt;email address&gt;**.

Notice the 'Invalid URL' error.


 Expected behavior: It should behave similarly to iOS, where it opens an email app.

 Actual behavior: 'Invalid URL' appears.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

