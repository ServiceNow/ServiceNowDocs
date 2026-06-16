---
title: Now Mobile - Intune for Android v21.0.0
description: The Android v21.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-android-v21-0-0.html
release: mobile
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 6
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for Android v21.0.0

The Android v21.0.0 release provides fixes for the application.

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

 PRB1966025

</td><td>

The user can't add comments to an incident

</td><td>

The input fields on the page 'Add comments' can't be focused on with the external keyboard \(using Tab or arrow keys\) nor with the screen reader. The screen reader reads out 'In the list, double-tap to activate.'

</td><td>

1.  Navigate to 'My work' and open any incident.
2.  Connect an external keyboard.
3.  Press Tab until the **Add comment** button is reached and press Space bar to land on the Add Comments screen.
4.  Press Tab repeatedly to move through input fields \(**Additional comments**, **Work notes**\).

Observe that focus does not move forward to the input fields.

5.  Press Shift + Tab multiple times.
6.  Focus eventually lands on the **Submit** button with a barely visible indicator.
7.  Continue pressing Shift + Tab to move backward to the **Work notes** input field and **Additional comments** input field.

 Observe the following issues: No visible keyboard focus when the page loads. Forward Tab navigation does not reach the **Additional comments** or **Work notes** fields. Focus becomes visible only after repeatedly pressing Shift + Tab, landing first on the **Submit** button with a barely visible indicator. Input fields are reachable only through reverse tab order, not forward.

</td></tr><tr><td>

Android Mobile

 PRB1957069

</td><td>

Uploading an attachment of any format to the activity stream produces an error

</td><td>

Attachment uploading fails in cases where the maximum file size configured on the instance exceeds a certain value.

</td><td>

1.  On the instance, configure com.glide.attachment.max\_size to 275000.
2.  Open Now Mobile / Agent on Android.
3.  Upload an attachment in any format to the activity stream of any task.

 Observe an error reading, 'Max file exceeded...'.

</td></tr><tr><td>

Android Mobile

 PRB1928040

</td><td>

Ensure offline outbox items include action result context

</td><td>

The temporary incidental remains in the outbox.

</td><td>

1.  Provision an instance with FSM and the Agent app installed and log in.
2.  Download offline cache and go offline.
3.  Navigate **My tasks** &gt; **Work order task** &gt; **Top menu** &gt; **Log incidental**.
4.  Fill out incidental details and submit.
5.  Sync and go online.
6.  Immediately go back offline.
7.  Open my incidentals tab.

 Expected behavior: The temporary incidental created in offline is replaced with the real incidental.

 Actual behavior: The temporary incidental is still in the outbox.

</td></tr><tr><td>

Android Mobile

 PRB1966061

</td><td>

Screen reader does not focus on the Upcoming Shifts list

</td><td>

Screen readers can't focus on the **My Work** &gt; **Upcoming Shifts** list under a calendar.

</td><td>

1.  Select the 'My Work' tab and select **My Schedule**.
2.  Create a schedule event \(for example 'Time Off'\).
3.  Turn TalkBack on.
4.  Attempt to swipe into the schedule list or events.

 Observe that schedule lists and list events can't be accessed unless tapped on.

</td></tr><tr><td>

Android Mobile

 PRB1971396

</td><td>

Out-of-memory crash when a large image is set as a LinearLayoutSGView background

</td><td>

When a large image is used as the background of a linear layout, the instance has an OOM crash.

</td><td>

1.  Open the Now Mobile app.
2.  On the home page, scroll down to the News section.
3.  Swipe right through the news items until the end is reached.

 Observe that when scrolling horizontally \(swiping right\) in the News section of the Now Mobile app, the app crashes and redirects either to the login page or the device home screen.

</td></tr><tr><td>

Android Mobile

 PRB1922792

</td><td>

Now Mobile creates many sessions for a single transaction

</td><td>

There are many sessions for a single login, even though there were only a few transactions.

</td><td>

1.  Log in to the Now Mobile app.
2.  Try to make a few moves in the mobile app.
3.  Navigate to instance and access the transaction logs.
4.  Filter the transaction for the user and group by session.

 Observe that there are many sessions for the single login, even though there were only a few transactions.

</td></tr><tr><td>

Android Mobile

 PRB1925481

</td><td>

Promoted topics do not display on Android

</td><td>

 

</td><td>

1.  Promote a topic in virtual agent designer.
2.  Check NASS.

 Notice that the promoted topic does not display.

</td></tr><tr><td>

Android Mobile

 PRB1966590

</td><td>

Some interactive elements are read out without a role by screen readers

</td><td>

Interactive elements must have a role assigned so that non-sighted users will know how to interact with the element.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1936666

</td><td>

When using UseDeviceSettingsForDateTimeFormats property, the activity stream shows an incorrect timestamp

</td><td>

When using UseDeviceSettingsForDateTimeFormats property with a 24 hour mobile time format, the activity stream shows incorrect timestamp with double 'AM' and 'PM' as 'AM AM' or 'PM PM'.

</td><td>

1.  Set the useDeviceSettingsForDateTimeFormats property to true in sys\_sg\_properties.list table.
2.  Set the phone time to 12 hour format.
3.  Open any accepted Work Order Task.
4.  Check the activity stream.

Notice that the time is correct.

5.  Change the Time format to 24 hour.
6.  Refresh the Activity stream and check timestamps.

 Notice that the time stamps show AM or PM twice.

</td></tr><tr><td>

Android Mobile

 PRB1936659

</td><td>

Using the UseDeviceSettingsForDateTimeFormats property sets an incorrect Scheduled Start date for Work Order Tasks when using the 24hour time format in Android

</td><td>

Using UseDeviceSettingsForDateTimeFormats property sets incorrect Scheduled Start date for Workorder tasks. It omits the 'a' in the 'at' word from the Scheduled Start Date.

</td><td>

1.  Set the useDeviceSettingsForDateTimeFormats property to true in sys\_sg\_properties.list table.
2.  Set phone time to 12 hour format.
3.  Open any accepted Work Order Task.
4.  Select **Edit Task**.
5.  Check the Scheduled Start Date.

Notice that it displays correctly.

6.  Change the Time format to 24 hour.

 Notice that in the Scheduled Start Date, the 'a' from 'at' has been omitted.

</td></tr><tr><td>

Android Mobile

 PRB1923465

</td><td>

Mobile UI rule doesn't working on Android devices for the boolean parameter

</td><td>

Mobile UI rule for a simple arithmetic action doesn't work for a boolean input.

</td><td>

1.  Create the 'Create new work' input form screen.
2.  Create a new boolean input.
3.  Add a UI rule for the boolean type input where on-load sets the value to 1 with operation simple arithmetic.
4.  Log in to the ServiceNow Agent app.
5.  Navigate to the 'My work' tab and select the **+** icon for the **Create new work** quick action.

 Expected behavior: The boolean type field is set to true in both iOS and Android.

 Actual behavior: The boolean type field is set to true and the mobile UI rule works only on iOS and not on Android.

</td></tr><tr><td>

Android Mobile

 PRB1924976

</td><td>

Discrepancies in Native Mobile UI during Post-chat surveys

</td><td>

This issue seems to happen with the Numeric Scale data type.

</td><td>

1.  Log into an instance and impersonate an Agent \(for example, Abel Tuter\).
2.  Navigate to 'Inbox' from Service Operations Workspace.
3.  Make the user available.
4.  Find a Device / Emulator running Samsung Galaxy S23 - Android 15 or use a Pixel 6 running Android 14.
5.  On the mobile device, log in to Now Mobile as the end user.
6.  Select the **Chat** button and use '+' to initiate a new chat.
7.  Select the **Contact Live Agent** button to engage a live agent.
8.  Accept the chat from the PC browser opened on Step 1.
9.  End the chat from the PC Browser.

Notice that a survey question appears along with the issue.

10. Try to drag the pop-up window upwards.

 Expected Behavior: The user should be able to select one of the choices and use the **Submit** button to submit. There shouldn't be a box to enter text / attach images. Also, dragging the window should not reveal the messages underneath.

 Actual behavior: The user sees a text box with the ability to attach files, and when trying to drag the window up, they can see the messages underneath.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

