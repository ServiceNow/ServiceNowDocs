---
title: Now Mobile - Intune for Android v17.4.0
description: The Android v17.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-04-04"
reading_time_minutes: 2
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for Android v17.4.0

The Android v17.4.0 release provides fixes for the application.

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

 PRB1739688

</td><td>

The user is unable to follow links to third party apps

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1729686

</td><td>

PDFs with pre-filled form data do not render properly

</td><td>

Pre-filled PDFs with fonts that aren't embedded result in a corrupted file.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1735791

</td><td>

The **Back** button sends the user to the main screen instead of the previous screen

</td><td>

 

</td><td>

1.  In the Now Mobile app, navigate to the 'Support' tab in the lower part of the screen.
2.  In 'Browse all topics' click **See all**.
3.  Click IT5.
4.  Click any topics in IT topics.
5.  Choose any topic that is available.
6.  Click an article.
7.  Click the **Back** button of Android mobile.

 Expected behavior: The user is directed to the previous screen.

 Actual behavior: The user is directed back to the **Browse all topics** &gt; **See all** screen.

</td></tr><tr><td>

Mobile Android

 PRB1741217

</td><td>

A blank screen or crash occurs after an action is performed in offline mode

</td><td>

When Android is in offline mode with large documents in memory, an action may result in the Android OS killing the activities in the back stack. If the action is on a form screen and requires user input from a form, the memory pressure increases. The TabsActivity may get killed by the OS, and the form screen view model is then cleared. As a result, the bundle containing the form template is no longer available. This results in a blank screen.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1744555

</td><td>

Unnecessary getGroup requests are sent to mobile scripts when the user reaches the bottom of a legacy list

</td><td>

Swiping up after reaching the end of the list sends additional getGroup requests to mobile scripts, resulting in duplicate list items.

</td><td>

1.  Configure a legacy list \(related list\) in a record screen using a scripted data item or a declarative data item with a parameter.
2.  Mark both the record screen and the legacy list as available offline.
3.  Download offline cache.
4.  Go offline.
5.  Tap the legacy list.
6.  Scroll to the bottom and swipe up again.

 Expected behavior: The client stops sending getGroup requests.

 Actual behavior: Additional getGroup requests are sent to mobile scripts, resulting in duplicate list items.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](../nowmobile-intune-available-versions.md)

