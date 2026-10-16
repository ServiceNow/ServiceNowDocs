---
title: Now Mobile - Intune for Android v22.2.0
description: The Android v22.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-android-v22-2-0.html
release: mobile
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 3
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for Android v22.2.0

The Android v22.2.0 release provides fixes for the application.

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

 PRB2082840

</td><td>

On cold-launch, the user is logged out of an adaptive auth-enabled instance and device registration is lost

</td><td>

When tapping an instance, the user is prompted to register the device again.

</td><td>

1.  On the Android app, register the device as trusted \(for example, generate a QR code on the instance and scan the QR code\).
2.  Log in to instance.
3.  Background the app.
4.  Swipe-quit the app.
5.  Relaunch the app.

 Expected behavior: The app relaunches and the user is still logged in.

 Actual behavior: The user is logged out, and when tapping the instance they are prompted to register the device again.

</td></tr><tr><td>

Mobile Android

 PRB2077545

</td><td>

Material footer button text can be truncated on a single line rather than arranging text on two lines for full visibility

</td><td>

The **Closed complete** button is not fully visible.

</td><td>

1.  Navigate to the 'My work' screen.
2.  Open the active work order task.
3.  Navigate to the details screen.

 Observe that the **Closed complete** button is not fully visible \(depending on the device's display size and text size settings\).

</td></tr><tr><td>

Mobile Android

 PRB2070608

</td><td>

Questionnaire of type Boolean text is not fully displayed in the Agent mobile app on Android, but is visible on iOS

</td><td>

The Questionnaire variable of type Boolean text is not fully displayed.

</td><td>

1.  Log in to Agent mobile app as a user that has a work order task and with a Questionnaire of type 'Boolean'.
2.  From the My Work screen launcher, open any work order task
3.  Select the **More** option and select **Take Questionnaire**.
4.  Open the Questionnaire.

 Notice that in the questionnaire variable of type 'Boolean', full text is not fully displayed.

</td></tr><tr><td>

Mobile Android

 PRB2086849

</td><td>

Write-back action hangs on a non-dismissable spinner when /pre\_fetch returns no document for a prefetched parameter screen

</td><td>

tapping a UI action whose parameter screen was advertised in the form document's PrefetchDocumentRedirections shows a non-dismissable loading spinner forever and issues no network request.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB2076760

</td><td>

The user is unable to scroll down the list of items in the 'Review' tab in Shipment Registry

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB2080917

</td><td>

Android Pixel 10 **Back** button unresponsive from KB Article to Virtual Agent \(VA\)

</td><td>

When the user views a KB Article provided as a source from a VA conversation, the **Back** button is unresponsive and the user can't return to the VA conversation.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB2081200

</td><td>

In the Now Mobile Android app \(Intune\), external links selected from within the app result in a 'Page blocked' message in the Work profile environment

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB2082685

</td><td>

The **Add Time Card** button doesn't work when opened from Search Results

</td><td>

The **Add Time Card** button on an RFST search-result card does not open the Add Time Card input form on the Now Agent mobile app for Android. The same button/action works correctly when the card is opened from the Dashboard launcher screen \(ALP\). Therefore, the write-back action itself is configured correctly — the bug is specific to the Global Search results screen.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB2074491

</td><td>

Video thumbnails aren't displayed for Video Type Media

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB2073045

</td><td>

The Input Form Screen 'Choice' type input does not accept the input when selected on the radio buttons in FSM mobile

</td><td>

When the user selects any of the choices on an input by selecting the **Radio** buttons themselves, the screen does not change and multiple selections will be allowed.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

