---
title: Now Support for Android v21.5.0
description: The Android v21.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowsupport-android-v21-5-0.html
release: mobile
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v21.5.0

The Android v21.5.0 release provides fixes for the application.

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

 PRB2023379

</td><td>

The arrow icon appears in the settings next to the instance name when logged in with the pre-login instance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2023969

</td><td>

Second user PIN is not recognized In Non Shared mode

</td><td>

Incorrect PIN error is shown

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2031389

</td><td>

PDF viewer does not support panning/scrolling after zooming in, making zoomed content unreadable

</td><td>

When users open a PDF within the app, they can pinch-to-zoom in on the document. However, once zoomed in, there is no ability to pan or scroll across the zoomed content. The zoom only operates from the center point, leaving content at the edges inaccessible. This makes PDFs effectively unreadable when zoomed.

</td><td>

1.  Open any PDF attachment within the app \(for example, from a record's attachment list\).
2.  Pinch to zoom in on the PDF document.
3.  Attempt to drag/swipe with one finger to pan across the zoomed content.

 Expected behavior: User can pan/scroll the document in all directions to view zoomed content.

 Actual behavior: Document remains locked at center. No panning occurs. Content beyond the visible area is inaccessible.

</td></tr><tr><td>

Android Mobile

 PRB2013102

</td><td>

Currency code is not displayed in a doughnut chart on Android while it appears on iOS

</td><td>

In Mobile Agent application, the currency code \(RM\) configured in the data visualization is displayed correctly inside the doughnut chart on iOS but is missing on Android.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2026492

</td><td>

Universal linking opens the URL in a browser rather than inside the Agent app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2032631

</td><td>

A Slack deep link opens inside the Agent app's task instead of launching Slack as separate task \(missing FLAG\_ACTIVITY\_NEW\_TASK\)

</td><td>

Tapping a MyHub function-link button with the Slack deep-link URL \(slack://open\) launches Slack's deep-link Activity inside the Agent app's task. Android Recent Apps shows the task labeled 'Agent' with Slack's UI on top, instead of Slack appearing as its own separate task.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2008004

</td><td>

unreadConversation API on Now Mobile returns an inflated badge count and empty chat history when mobileChannelType and mobileChannelId are not passed

</td><td>

The /unreadConversation API on Now Mobile returns an incorrect \(inflated\) unread notification badge count on the Now Assist stars icon. When the user taps the clock icon to view chat history, the same inflated count is shown but no conversations are listed \('No chat found'\).

</td><td>

1.  Log in to Now Mobile \(iOS or Android\) on the affected instance.
2.  Navigate to Now Assist \(stars icon\).

Observe the notification badge on the stars icon showing a non-zero count.

3.  Open Now Assist.
4.  Tap the clock icon to open chat history.
5.  Observe the chat history view.

 Expected behavior: The notification badge should show 0 \(or no badge\) when there are no active unread conversations. The chat history view should accurately reflect the user's conversation history.

 Actual behavior: The notification badge displays a non-zero count \(matching stale records in \[sys\_cs\_message\_last\_read\]\). The chat history view shows the same inflated count but displays "No chat found" with no conversations listed.

</td></tr><tr><td>

Android Mobile

 PRB2034164

</td><td>

The app crashes when a screen rotates with the signature input bottom sheet open

</td><td>

 

</td><td>

1.  From the 'More' tab, access My work.
2.  Open any WOT and from 'Details' open the parent 'Work order'.
3.  Select the **Sign and Confirm footer** button.

Observe that the signature input screen shows up.

4.  Rotate the screen.

 Observed that the app crashes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

