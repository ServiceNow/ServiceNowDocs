---
title: Now Support for Android v21.3.0
description: The Android v21.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowsupport-android-v21-3-0.html
release: mobile
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v21.3.0

The Android v21.3.0 release provides fixes for the application.

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

 PRB2004137

</td><td>

OutOfMemoryError during offline to online sync

</td><td>

The app either times out after two minutes or crashes during sync with an OutOfMemoryError.

</td><td>

1.  Install Android Agent 21.1.0.
2.  Enable Offline mode.
3.  Perform actions on a large number of WOTs \(for example, Start Work, Close Complete\) while offline.
4.  Allow actions to queue locally for sync.
5.  Switch back online to trigger /sync.
6.  Observe behavior while processing a large sync response \(tens of MB\).

 Expected behavior: Offline actions should sync successfully without crashing, even with large payloads. The app should not duplicate large response data in memory during sync processing. Users should not be left in an invalid post‑crash state.

 Actual behavior: The app with either time out after two minutes or crash during sync with an OutOfMemoryError. A crash may surface as RxJava UndeliverableException caused by OOM.

</td></tr><tr><td>

Android Mobile

 PRB2009019

</td><td>

A third party deeplink is not functioning in the Now Mobile app

</td><td>

The user is not redirected to the external browser when they select third-party URLs.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2006299

</td><td>

Dialogs do not theme correctly under Microsoft Intune MDM/MAM

</td><td>

The dialog is dark themed and unreadable.

</td><td>

1.  Set up any FSM instance with a work order task that has a Special Handling Note.
2.  Set up Intune to work with Agent Intune app.
3.  Change the device theme to Dark mode \(not in-app theme\).
4.  Log in to Intune and instance on the Agent Intune app.
5.  Ensure that the in-app theme \(**Settings** &gt; **Preferences** &gt; **Theme** &gt; **is Default**\).
6.  Open the work order task in 1.

 Expected behavior: The dialog should be light themed and with the right colors.

 Actual behavior: The dialog is dark themed and unreadable.

</td></tr><tr><td>

Android Mobile

 PRB2003717

</td><td>

Whitelabel app with custom app ID will show 'Error link not supported' with a universal link

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2004277

</td><td>

Now SDK Sample Application crash when device is connected to WiFi without internet due to ServiceNow SDK preload

</td><td>

 

</td><td>

1.  Build and run now SDK sample application.
2.  Log in.
3.  Exit the application by swiping away from task switcher.
4.  Disable internet access while keeping wifi on.
5.  Open the app.

 Observe that the app crashes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

