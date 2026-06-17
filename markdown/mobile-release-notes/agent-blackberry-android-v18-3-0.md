---
title: Mobile Agent - BlackBerry for Android v18.3.0
description: The Android v18.3.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-10-03"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for Android v18.3.0

The Android v18.3.0 release provides fixes for the application.

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

 PRB1801355

</td><td>

The DateTime Input date picker shows an incorrectly formatted error when validating MaxDays and MinDays

</td><td>

Observe the error: 'Please choose a time on or before \[L\]java.lang.String@7063c12.'

</td><td>

1.  Log in to an instance with WSD installed. 
2.  Tap **MyReservations** &gt; **Make reservations** &gt; **Workspace** &gt; **Browse all**.
3.  In the start date and time field, set a date ten days from now.

 Expected behavior: An error is displayed with the max date time added at the end.

 Actual behavior: The following error appears: 'Please choose a time on or before \[L\]java.lang.String@7063c12.'

</td></tr><tr><td>

Mobile Android

 PRB1780908

</td><td>

'You are offline' message and incorrect message order in the agent chat window

</td><td>

When Chat is initiated from Mobile and the user has left the chat for over one minute, the user observes a message reading 'You are offline' and the messages sent by Agent go out of order.

</td><td>

1.  Initiate a chat and make the app run in the background.
2.  Send messages to the user after waiting 30 seconds.
3.  Re-open the app by clicking the notification.

 Notice a message that reads 'You are offline' on top of the chat window. Sometimes the order of messages that was shown after opening up an app through notification is also incorrect.

</td></tr><tr><td>

Mobile Android

 PRB1790033

</td><td>

Pale screen header background makes system icons unreadable in Now Mobile

</td><td>

If a theme uses a pale color for the secondary brand color, it results in the header washing out the system icons \(battery, clock, etc.\) and there is no way to control the background color behind the icons to prevent this.

</td><td>

1.  Hop to an instance with Theme Builder installed.
2.  Open Theme Builder and create a theme.
3.  For the Brand Secondary color pick something very pale/white \(for example, \#FDFDFD\).
4.  Save and apply the theme for both web and mobile.
5.  Confirm that the theme is applied in the browser and then log in via the Now Mobile app.

 Notice in the header that the clock, battery, reception etc. are either almost invisible or hidden entirely.

</td></tr><tr><td>

Mobile Android

 PRB1790203

</td><td>

Text in the 'Media' section does not display in full on Android devices

</td><td>

Text gets cut off with an ellipsis.

</td><td>

1.  Create a sys\_media\_section with the following message in the text field: 'In the app, users can manage approvals, raise an incident, check the status of a request or incident, manage delegation, and view the guest Wi-Fi password. Further functionality will be deployed in the future.'
2.  Add the Media section to the Applet Launcher screen.
3.  Log in to the instance on the NOW mobile app using an Android device.
4.  Navigate to the Applet Launcher screen where the Media section was added.

 Expected behavior: The text message should appear in full.

 Actual behavior: The message gets cut off with an ellipsis.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](../agent-blackberry-available-versions.md)

