---
title: Now Mobile - Intune for Android v18.1.0
description: The Android v18.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-android-v18-1-0.html
release: mobile
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for Android v18.1.0

The Android v18.1.0 release provides fixes for the application.

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

 PRB1750359

</td><td>

Approving / Rejecting RITM with a comment does not work with reauthentication preconditions

</td><td>

The RITM should be rejected or approved but it stays in the reason input screen.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1772263

</td><td>

Prompted topics in Virtual Agent are not shown as buttons

</td><td>

Prompted topics in the default chat experience are not shown as buttons in Virtual Agent.

</td><td>

1.  Log in to an instance in Android mobile.
2.  Select the chat icon the bottom right.

 Notice that a prompted topic appears above 'Show me everything' as a normal text/link rather than a button. In iOS it appears as a button with a border and filling color.

</td></tr><tr><td>

Mobile Android

 PRB1768949

</td><td>

The WebRTC API doesn't work on Android

</td><td>

A banner reads 'Please allow your browser to access your microphone and camera'.

</td><td>

1.  Log into a Now Mobile instance.
2.  On Home, select **My Call**.

This brings up the AWS calling feature.


 Observe a red banner that reads, 'Please allow your browser to access your microphone and camera'.

</td></tr><tr><td>

Mobile Android

 PRB1747963

</td><td>

Old chats in Virtual Agent \(VA\) in Now Mobile don't display the correct VA icon in iOS

</td><td>

The same chats for the same user on Now Mobile for Android show the correct icon.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1763421

</td><td>

Closing a case page redirects to the case form page and not a list of RPs

</td><td>

Upon closing the case page, the user is redirected to the case form page rather than being redirected to a case creation page that shows a list of RPs.

</td><td>

1.  Log in to the Mobile Agent app as a user with elevated privileges.
2.  Navigate to the work view screen of Agent Workplace.
3.  Select the 'Create a task' icon.
4.  On the 'Create a case' screen, select any of the RP's \(for example, 'Submit a general request'\), fill in the mandatory fields, and submit.

On submit, observe the request status screen.

5.  Select the **Close** button.

 Expected behavior: The user is redirected to a case creation page that shows a list of RPs.

 Actual behavior: The user is redirected back to the case form page.

</td></tr><tr><td>

Mobile Android

 PRB1768279

</td><td>

A reference field value is not parsed as a text string

</td><td>

An 'Assignment Group Field' value under the activities tab of 'Incidents' is displayed as a link instead of simple text in Now Agent.

</td><td>

1.  Log in to an instance.
2.  Open any incident and assign it to 'A' user.
3.  Create an assignment group ending with '.app'.
4.  Change the assignment group on this INC to the newly created assignment group.
5.  Log in to the Now Agent app.
6.  Open 'My Incidents' or 'Tickets created by me'.
7.  Open the affected INC.
8.  Navigate to the 'Activity' tab.

 Observe a link in the Assignment Group Field value.

</td></tr><tr><td>

Mobile Android

 PRB1771016

</td><td>

Deep links cannot be opened

</td><td>

Mobile Publishing apps use the requesting instance to set up Android asset links.

</td><td>

1.  Submit an Android private mobile publishing app.
2.  Install it on the device.
3.  Long press the app icon and navigate to **App info** &gt; **Open by default**.

 Expected behavior: In the 'Open by default' list, observe one supported link with the name of the instance on which the mobile publishing app was requested.

 Actual behavior: The 'Open by default' list is empty.

</td></tr><tr><td>

Mobile Android

 PRB1771016

</td><td>

There is a null pointer exception in the logs

</td><td>

The error in the logs reads, 'Fatal Exception: java.lang.NullPointerException: destination.itemId must not be null'.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

