---
title: Now Support for Android v20.5.0
description: The Android v20.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-11-06"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v20.5.0

The Android v20.5.0 release provides fixes for the application.

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

 PRB1947988

</td><td>

The initial Agent location entry in the geo\_history table sometimes records a cached location

</td><td>

This occurs when the user enables location tracking.

</td><td>

1.  Log in to the Agent App.
2.  Enable Location tracking \( Manual / Action-based\).

 Observe that the initial Agent location entry in the geo\_history table sometimes records a cached location.

</td></tr><tr><td>

Android Mobile

 PRB1920524

</td><td>

In the Agent Mobile app, the keyboard disappears on a string input field if the user doesn't type for more than one second

</td><td>

If a parameter screen has multiple pages, the keyboard disappears after one second of no typing when filling in some of the string input fields on an input form screen.

</td><td>

1.  Create a function where the action item is has a write-back action of type 'Script' and a parameter screen containing multiple pages.
2.  Create any input form screen with multiple pages and associate it to a function.
3.  Add the function to a record for example 'work order' screen \(for example, open My work tab in the Agent app on an Android device\).
4.  Open a work order task \(for example check under 'My group tasks'\).
5.  Open any WOT and navigate to the work order from there.
6.  Select **Options** &gt; **Sign AIA declaration function.**.
7.  Fill in the fields and select **Next**.
8.  On the second page, start typing in the **String** type field.
9.  Stop typing for a few seconds.

 Notice that the keyboard closes within a couple of seconds.

</td></tr><tr><td>

Android Mobile

 PRB1943594

</td><td>

Mobile app crash when submitting a reservation request.

</td><td>

The screen briefly loads, turns blue, and the application crashes crashes when submitting a reservation request.

</td><td>

1.  On the ServiceNow Mobile App, navigate to **Reservations** &gt; **New Reservation**.
2.  Select Building A, floor 1, unselect "All day" date, and select today's date.
3.  Select **Submit**.

 Observe that the screen briefly loads, turns blue, and the application crashes. Relaunching the app reproduces the issue every time.

</td></tr><tr><td>

Android Mobile

 PRB1947635

</td><td>

Questionnaires occasionally get stuck

</td><td>

The root cause is the out-of-order processing of SetBottomButtons Cabrillo actions.

</td><td>

1.  Navigate to **My work** &gt; **See all**.
2.  Select a WOT ending in 20390.
3.  Select **Take questionnaire**.

The user lands on the 'Get Started' page.

4.  Refresh the 'Get Started' page.

 The user is redirected back to the 'Get Started' page, which erroneously displays the **Previous** / **Next** / **Submit** buttons instead of the **Get Started** button.

</td></tr><tr><td>

Android Mobile

 PRB1939439

</td><td>

The Input Form Screen Submit button is not activated after filling in all mandatory inputs

</td><td>

The user is unable to submit from the Input Form Screen on first try if there are mandatory variables.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../now-support-available-versions.md)

