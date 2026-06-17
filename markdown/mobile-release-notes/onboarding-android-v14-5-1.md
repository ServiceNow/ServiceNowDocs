---
title: Mobile Onboarding for Android v14.5.1
description: The Android v14.5.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v14-5-1.html
release: mobile
topic_type: reference
last_updated: "2022-09-15"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v14.5.1

The Android v14.5.1 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## New feature

Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

PRB1600198

</td><td>

Users are unable to deep link to third-party apps

</td><td>

Users are unable to deep link to a third-party app from ServiceNow Mobile on Android devices.

</td><td>

1.  Configure a button to open a URL: 'rmapp://employee'.
    1.  Create button pointing at rmapp://employee.
    2.  Create a button instance of the button.
    3.  Add the button to the launcher screen to create a quick action.
2.  Allow list rmapp by editing the glide.sg.allowed\_external\_deeplinks system property and setting the value to 'rmapp' \(or adding it, comma-separated, to the existing list\).
3.  Install the 'Routematic' application on the device.
4.  Run the Agent application, log in, and run the button.

 Expected behavior: The Routematic application opens.

 Actual behavior: The user observes a modal pop-up error.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

