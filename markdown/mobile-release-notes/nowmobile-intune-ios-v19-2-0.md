---
title: Now Mobile - Intune for iOS v19.2.0
description: The iOS v19.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-ios-v19-2-0.html
release: mobile
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v19.2.0

The iOS v19.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_uw1_y14_31c" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS

 PRB1833380

</td><td>

Public distribution Mobile Publishing apps with Intune throw a MSALErrorDomain -50000 error

</td><td>

The user observes a -50000 error upon logging in to a branded Intune app.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1830718

</td><td>

The wrong error message displays when the app can't open a URL in an external browser

</td><td>

 

</td><td>

1.  Open a webview.
2.  Select a button that tries to open a URL while the app is in the background.

 Expected behavior: The 'Missing app' error shouldn't display.

 Actual behavior: The 'Missing app' error displays.

</td></tr><tr><td>

Mobile iOS

 PRB1816651

</td><td>

Signatures are too large on PDF's generated from Agent Mobile

</td><td>

PDF's generated in Agent Mobile contain signatures that are too large.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1840851

</td><td>

Virtual Agent JSON cards display a button with an empty LinkLabel

</td><td>

Mobile displays a button for a link without text. Selecting the button doesn't do anything because the link is invalid.

</td><td>

1.  Log in to Surf on the My ServiceNow Mobile app.
2.  Type in the query: 'my servicenow app'.

 Notice a large button that doesn't have a label and takes the user to an incorrect URL when selected.

</td></tr><tr><td>

Mobile iOS

 PRB1842355

</td><td>

The background color of ImageChoiceList is incorrect

</td><td>

The background is white.

</td><td>

1.  On the Home page, select **My tasks**.
2.  Open any task.
3.  In the 'To-Do' section, select **Complete new hire pulse check**.

 Notice a white background on the screen.

</td></tr><tr><td>

Mobile iOS

 PRB1740552

</td><td>

A UI Rule is not applied consistently on the Details screen after updating from an input form

</td><td>

When the user edits a record by adding a note, the red background of the note text disappears. This only occurs the second time the user edits a record and navigates back to the home screen.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1847008

</td><td>

Analytics data is not captured for instances on Xanadu and prior release versions

</td><td>

Analytics data about the user's performed events and screen details should be displayed.

</td><td>

Pre-requisites:

 1.  Instance on Xanadu or previous family release version.
2.  Now Mobile application version 19.0.0 or above.
3.  The user logging into the Now mobile application is a user without elevated privileges.

 Steps:

 1.  Log in to the Now mobile application on an iOS device.
2.  Navigate to different screens and tap on some buttons to generate data for Analytics.
3.  Background the application for some time.
4.  Log in to the instance and navigate to the User Experience Analytics dashboard.
5.  Select the Now Mobile application to view analytics data.

 Expected behavior: Analytics data about the user's performed events and screen details should be displayed.

 Actual behavior: No analytics data is captured.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

