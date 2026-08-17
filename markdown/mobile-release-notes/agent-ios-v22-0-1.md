---
title: Mobile Agent for iOS v22.0.1
description: The iOS v22.0.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-ios-v22-0-1.html
release: mobile
topic_type: reference
last_updated: "2026-08-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v22.0.1

The iOS v22.0.1 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

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

iOS Mobile

 PRB2071235

</td><td>

Camera not visible when scanning Barcode/QR on Legacy SG Form screens on iOS 26

</td><td>

No camera preview appears.

</td><td>

1.  On an iOS 26.0+ device or simulator, open the Now Mobile app \(v22.0.0+\).
2.  Navigate to any Legacy SG Form screen with a Barcode/QR input field \(for example, Asset Lookup\).
3.  Tap the field's **Scan** button to launch the inline camera scanner.
4.  Grant camera permission if prompted.

 Expected behavior: The camera preview slides into view above the form fields, as it does on iOS &lt; 26 and in app version 21.5.2.

 Actual behavior: No camera preview appears. No error, no alert — the screen looks unchanged aside from a brief animation that has no visible effect.

</td></tr><tr><td>

iOS Mobile

 PRB2070099

</td><td>

Add to Calendar .ics file links download as .bin files and fail to open

</td><td>

The file download as a .bin and can't be opened unless renamed.

</td><td>

1.  When in the app, scroll to bottom of homepage.
2.  Locate 'Upcoming events' widget.
3.  Select the **Add to calendar** button on any event.

 Expected behavior: Selecting Add to calendar in the MyHR Portal \(embedded in the Now Mobile App\) should add the event to the device calendar without error, on both iOS and Android.

 Actual behavior: On iOS the file will download as a .bin and thus can't be opened unless renamed.

</td></tr><tr><td>

iOS Mobile

 PRB2070098

</td><td>

The viewFile API for viewAttachment shows 'Error downloading file'

</td><td>

The user observes 'Error downloading file'.

</td><td>

1.  Launch the Now mobile app.
2.  Navigate to **Home page** &gt; **Cabrillo** &gt; **View attachment**.

 Expected behavior: Downloading spinner and file download and should show 'Open with Calendar' or directly open the .ics file with Calendar app.

 Actual behavior: Error message shown - 'Error downloading file'.

</td></tr><tr><td>

iOS Mobile

 PRB2070825

</td><td>

Intune sign-in fails for Azure Government / National Cloud users

</td><td>

Sign-in fails.

</td><td>

1.  On a device whose user is in an Azure Government tenant, install the Intune build.
2.  Launch the app and start sign-in.
3.  Complete the Microsoft Authenticator prompt.

 Expected behavior: MSAL authenticates against the user's National Cloud, enrollment completes, and the user reaches the app.

 Actual behavior: Sign-in fails. Microsoft returns an error indicating the account belongs to a National Cloud.

</td></tr><tr><td>

iOS Mobile

 PRB2069935

</td><td>

Crash on creating a notification banner on cold launch from a push notification tap

</td><td>

The app crashes during launch when the user opens it by tapping a push notification. Users may perceive this as the app closing itself right after launch.

</td><td>

1.  Ensure the app is not running \(force quit or fresh launch\).
2.  Put the device in a state where the read-state update will fail \(for example, airplane mode / no connectivity\).
3.  Tap a push notification for the app.

Notice that the app cold-launches and crashes as the failure banner is constructed.

</td></tr><tr><td>

iOS Mobile

 PRB2070691

</td><td>

Crash on Activity Stream form screen teardown

</td><td>

The app crashes.

</td><td>

1.  Open a record form whose Activity Stream contains an image attachment.
2.  Navigate away while the image is still downloading. Timing-dependent — reproduces most reliably on a slow connection.

 Expected behavior: Controller tears down cleanly.

 Actual behavior: App crashes.

</td></tr><tr><td>

iOS Mobile

 PRB2066528

</td><td>

Silent-push force-logout traps the user in an infinite login/logout loop on the same instance

</td><td>

When a force\_logout silent push is received for an instance, the user is correctly logged out. But if they then log back into that same instance, they are force-logged-out again immediately.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-available-versions.md)

