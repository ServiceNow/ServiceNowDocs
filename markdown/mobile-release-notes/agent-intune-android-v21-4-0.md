---
title: Mobile Agent - Intune for Android v21.4.0
description: The Android v21.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-intune-android-v21-4-0.html
release: mobile
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for Android v21.4.0

The Android v21.4.0 release provides fixes for the application.

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

 PRB2017687

</td><td>

Bundled language not applied when user hasn't explicitly selected the app language

</td><td>

UI strings display in English.

</td><td>

1.  Navigate to Meu trabalho \(My Work\) tab.

Observe that the **See all** button next to the 'Minhas tarefas' section header is not translated \(displays **See all** instead of 'Ver tudo'\).

2.  Select **See all** to open the full tasks list.
3.  Select the filter icon.

 Observe that the filter screen displays a mix of languages — filter action strings such as 'Filters', 'Clear', 'Sort by', 'Default', 'Any', and 'Apply' remain in English while field labels \(for example, 'Solicitante', 'Resumo', 'Número'\) are correctly translated in Portuguese.

</td></tr><tr><td>

Android Mobile

 PRB2013599

</td><td>

The app closes and returns to the home screen after approving/rejecting via push notification

</td><td>

The device returns to the home screen.

</td><td>

1.  Impersonate abel.tuter on a base instance.
2.  On an Android 16 device, log in to the Now Mobile app as the admin user, then return to the homepage.
3.  On the desktop platform, navigate to /esc portal.
4.  **Request** &gt; **Hardware** &gt; **Mobiles** &gt; **Apple iPhone 13**, and complete the request.

On the Android device, a push notification appears for the approval request.

5.  Select the notification then **Approve**.

 Expected behavior: The app remains in the Now Mobile app and displays the next screen.

 Actual behavior: The Now Mobile app closes, and the device returns to the home screen \(the approval itself is processed successfully on the server side\).

</td></tr><tr><td>

Android Mobile

 PRB2017507

</td><td>

Voice Agent doesn't work on android devices when using an account nickname

</td><td>

If the nickname is different from the instance name, voice chat does not work.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-intune-available-versions.md)

