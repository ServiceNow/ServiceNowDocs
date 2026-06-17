---
title: Mobile Agent - Intune for Android v20.4.0
description: The Android v20.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-10-02"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for Android v20.4.0

The Android v20.4.0 release provides fixes for the application.

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

 PRB1932109

</td><td>

Added support for 16KB page sizes

</td><td>

Google has a requirement that Android 15+ devices must support 16KB page sizes.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1926309

</td><td>

An offline scheduled download is canceled when an app is in the background

</td><td>

This is an Android issue only.

</td><td>

1.  Log in to the Agent app.
2.  Turn on background downloading from the app settings.
3.  Put the app in the background.
4.  Receive a silent push for an offline scheduled download.

 Expected behavior: The offline download must complete even when app is in the background.

 Actual behavior: The offline download isn't completed. The WorkManager job is started but is cancelled by the OS.

</td></tr><tr><td>

Android Mobile

 PRB1936258

</td><td>

An on-demand work order task \(WOT\) form doesn't refresh after a WB action and the **Close Complete** button remains visible

</td><td>

The Android on-demand form screen doesn't refresh after a successful WB action. The **Close Complete** button is configured with a 'Jump to screen' action targeting the same screen ID. After redirection back to the screen, the original form doesn't refresh, and the **Close Complete** button remains visible. If the button is tapped again, it results in an 'Insufficient Privileges' error.

</td><td>

1.  Impersonate a user.
2.  Navigate to the **My Work tab** &gt; **My Schedule \(Calendar\)**.
3.  Select an accepted WOT from the events.
4.  Tap **Start Work**.
5.  In the pop-up, navigate to the previous task.
6.  Complete the questionnaires.
7.  Select **Close Completed**.
8.  Enter a note and submit.

 Observe that the **Close Completed** button remains visible. When tapped again, entering notes and submitting triggers an 'Insufficient Privileges' error. Repeat 1-20 times if needed, as the issue is intermittent.

</td></tr><tr><td>

Android Mobile

 PRB1931896

</td><td>

Users are unable to open UI parameters for the 'Space Details' screen on Android devices

</td><td>

 

</td><td>

1.  Install Workspace core pluign. Navigate to the sn\_wsd\_core\_space table.
2.  Open a record.
3.  Select **Create a QR code**.
4.  Fill in the required fields.

A QR code attachment is generated.

5.  Log in to the Mobile app on Android.
6.  Open the phone camera.
7.  Scan the QR code.
8.  Select the three dots icon on the top-right of the screen.

 Expected behavior: It should open the pop-up menu, which works on iOS.

 Actual behavior: It either does nothing or goes back to the home page/main navigation.

</td></tr><tr><td>

Android Mobile

 PRB1931874

</td><td>

Offline polling timeout should match the server timeout

</td><td>

 

</td><td>

1.  Open an instance.
2.  Make a large offline cache by adding more documents, so it would take more than five minutes to generate.

 Expected behavior: The client should poll for a default of ten minutes before timing out. If glide.sg.offline.job. maxRuntime is set on the instance, the polling timeout on the clients should match the configuration.

 Actual behavior: The client would stop polling in five minutes and it wouldn't wait for the offline cache. As a result, the offline cache generated isn't retrieved by the client.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](../agent-intune-available-versions.md)

