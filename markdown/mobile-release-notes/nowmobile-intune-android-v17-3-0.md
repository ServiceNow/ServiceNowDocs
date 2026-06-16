---
title: Now Mobile - Intune for Android v17.3.0
description: The Android v17.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-android-v17-3-0.html
release: mobile
topic_type: reference
last_updated: "2024-03-07"
reading_time_minutes: 3
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for Android v17.3.0

The Android v17.3.0 release provides fixes for the application.

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

 PRB1734432

</td><td>

The user is unable to view an attachment

</td><td>

An attachment in Android does not open when clicked and shows the message 'Can't open file. Try saving the file on the device and then opening it.'

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1733542

</td><td>

The user is unable to open a banner push notification

</td><td>

Tapping a banner notification leads to an infinite load screen in the app.

</td><td>

1.  Log in to any base instance on Android as an admin or maint user.
2.  From the platform desktop view, open any RITM record opened by an ITIL user.
3.  Add a comment in the **Additional Comments** field in the record.
4.  Wait for a banner notification to appear and tap to open.

 Expected behavior: The App should open and navigate the user to the Notifications tab.

 Actual behavior: The page gets stuck and displays a spinning circle.

</td></tr><tr><td>

Mobile Android

 PRB1726649

</td><td>

When an agent sends an image file to a mobile chat user, there's a false indication that the agent is typing

</td><td>

When workspace agent sends an image to mobile end user, the UI of the mobile app indicates that the agent is still typing when they are not.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1729792

</td><td>

Inconsistency between Android and iOS in displaying currency fields in List view

</td><td>

For example, A$ 3.40 in Android is $AUD 3.40 in iOS.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1733802

</td><td>

The input form screen mandatory choice submit field rule doesn't work when a choice is deselected

</td><td>

The user can't submit a form when a mandatory field is empty. However, they can get around this by populating then depopulating a field before submitting.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1716477

</td><td>

Barcode scanning with an external zebra scanning device doesn't automatically shift focus to the next field after scanning

</td><td>

The user needs to manually tap the next field in order for the barcode scan to work.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1734336

</td><td>

The client does not honor a disabled universalLink Properties rule.

</td><td>

The client does not honor SystemProperty.universal LinkProperties.enabled = false.

</td><td>

1.  Log in to an instance that has the universalLink Properties disabled.
2.  Navigate to a Service Portal page.

 Expected behavior: The client does not make an API call to Universal Links.

 Actual behavior: The client makes a request to the Universal Links API and displays the "Error loading URL" screen.

</td></tr><tr><td>

Mobile Android

 PRB1735778

</td><td>

Attachments become corrupted and not viewable on Android or Web after being uploaded to the instance

</td><td>

 

</td><td>

1.  Navigate to the 'Work order' tab.
2.  Open the first WOT.
3.  Click the top menu \(3 dots\).
4.  Click **Add attachment** and attach a PDF.

 Expected behavior: The uploaded PDF should be viewable from the Activity Stream.

 Actual behavior: The PDF cannot be viewed/opened.

</td></tr><tr><td>

Mobile Android

 PRB1735806

</td><td>

Paging does not work inside the item section screen

</td><td>

 

</td><td>

Pre-requisites:

 -   FSM OOB configuration. Any necessary offline configuration.
-   The item section screen must be a list that is available offline.

 Steps:

 1.  Log in to an instance with the above pre-requisites with Now Agent.
2.  Navigate to a list of records. Open a record.
3.  Swipe to the list item section on the record.
4.  Open the list in the item section.
5.  Scroll to the very bottom of the list.

 Expected behavior: Scrolling to the bottom of the list pages a new group of items.

 Actual behavior: Paging does not occur. For example, scrolling to the bottom of the list simply shows the bottom of the list.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

