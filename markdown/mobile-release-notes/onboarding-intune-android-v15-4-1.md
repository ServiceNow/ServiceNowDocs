---
title: ServiceNow Onboarding - Intune for Android v15.4.1
description: The Android v15.4.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v15-4-1.html
release: mobile
topic_type: reference
last_updated: "2023-02-14"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v15.4.1

The Android v15.4.1 release provides fixes for the application.

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

 PRB1637456

</td><td>

App crashes after updating due to SQLCipher error

</td><td>

 

</td><td>

1.  Install 15.3.0 Now App \(Intune v8.3\).
2.  Launch the Now App 15.3.0.
3.  Install the Company Portal.
4.  Launch the Now app again.
5.  Observe the performance instability.
6.  Update to 15.4.0 \(Intune v9.1.0\).
7.  Relaunch.

 Expected behavior: Users are able to upgrade to the 15.4.0 version and log in to the app with no issues.

 Actual behavior: Users observe SQLCipher exceptions when upgrading.

</td></tr><tr><td>

Mobile Android

PRB1634452

[KB1222988](https://hi.service-now.com/kb_view.do?sysparm_article=KB1222988)

</td><td>

Performance degradation when launching app starting in v15.3.0

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

