---
title: Now Support for Android v17.2.0
description: The Android v17.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v17.2.0

The Android v17.2.0 release provides fixes for the application.

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

 PRB1718094

</td><td>

The user is unable to type anything in response to an Agent

</td><td>

A 'typing' indication is shown indefinitely and the message box is hidden.

</td><td>

1.  Open VA chat.
2.  Click **Show me everything**.
3.  Click **Connect to Agent** and allow the agent to send a message.

 Observe that there is a 'typing' indication and the message box is hidden.

</td></tr><tr><td>

Mobile Android

 PRB1716231

</td><td>

Deep link error in the Google Play console

</td><td>

The web link '/deeplink' for Domain '.service-now.com' is flagged as 'Failed domain checks'.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1724090

</td><td>

Android splash screen icons are warped when no splash screen background color is passed in the manifest

</td><td>

 

</td><td>

1.  Submit a private Android Mobile Publishing app with app icons and splash logos, but do not add a splash screen background color.
2.  Load the Android app onto a device.

 Expected behavior: The splash screen icon should not be warped and the Android build should fall back to the ServiceNow splash background color.

 Actual behavior: The splash screen icon is warped.

</td></tr><tr><td>

Mobile Android

 PRB1728684

</td><td>

The Mobile UI rule 'On change' doesn't work

</td><td>

 

</td><td>

1.  Create a mobile Mobile UI Rule and trigger it on change.
2.  Make a couple of fields mandatory based on the condition and make 'Reverse if False' true.
3.  Log in to the Agent App.
4.  Navigate to the input form screen where the Mobile UI Rule was added.
5.  Make changes to trigger the mobile UI rule.

 Notice that the 'on change' mobile UI rule is not triggered.

</td></tr><tr><td>

Mobile Android

 PRB1722445

</td><td>

Internal links are opened in an external browser instead of in-app

</td><td>

 

</td><td>

1.  Tap the chat icon on the bottom right.
2.  Start a conversation.
3.  Tap **Show me everything**.
4.  Select **Test emoji output topic**.
5.  Click the link.

 Expected behavior: The link should open in a web view in the app because the URL is internal \(same as the instance the user logged in to\).

 Actual behavior: The link opens in an external browser.

</td></tr><tr><td>

Mobile Android

 PRB1727934

</td><td>

Attached KB article links in the Activity Stream do not open in Android Agent/NowMobile apps

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1720676

</td><td>

Uploading multiple attachments from different actions while offline fails

</td><td>

An error message displays saying that the publication has failed.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../now-support-available-versions.md)

