---
title: Mobile Agent for Android v17.1.0
description: The Android v17.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-01-04"
reading_time_minutes: 1
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for Android v17.1.0

The Android v17.1.0 release provides fixes for the application.

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

 PRB1713635

</td><td>

A signature field with UI rules does not get disabled

</td><td>

A field that should be disabled is not.

</td><td>

1.  Log in to the Mobile \(requestor\) app.
2.  Scroll down to the Actions section and tap the **ListActions** screen.
3.  Swipe on an item from left to right.
4.  Tap **...** &gt; **SingatureWithUIRules** &gt; **Next** &gt; **Fill the order 5 value** &gt; **Signature3** and draw something.
5.  Tap **Apply** &gt; **Previous**.

 Expected behavior: The **Signature 1** field should be disabled.

 Actual behavior: The **Signature 1** field is enabled.

</td></tr><tr><td>

Mobile Android

 PRB1720676

</td><td>

Uploading multiple attachments from different actions while offline fails

</td><td>

An error message displays saying that the publication has failed.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1712303

</td><td>

Screen reader announces static text sections as buttons

</td><td>

Static text should not be announced as a button.

</td><td>

1.  Log into the Now Mobile app.
2.  On the home page, navigate to **Browse all topics**.

 Note that everything in this screen is selectable but nothing happens.

</td></tr><tr><td>

Mobile iOS

 PRB1711313

</td><td>

The screen reader focuses on the image and announces 'unlabeled, button'

</td><td>

The Talkback application on Android announces the images on the home page of the Onboarding application as unlabeled buttons.

</td><td>

1.  Have the Talkback built-in feature in the Android device enabled.
2.  Log into the Test instance in the Onboarding Mobile application.
3.  On the home screen, click the image to get the login and password

 Expected behavior: Screen readers should ignore images and announce only the text.

 Actual behavior: The talkback application announces the image as an unlabelled button.

</td></tr><tr><td>

Mobile Android

 PRB1710229

</td><td>

Deep links route to SSO login instead of Local Login

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

