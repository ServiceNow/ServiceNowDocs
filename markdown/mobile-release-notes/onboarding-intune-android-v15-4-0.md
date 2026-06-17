---
title: ServiceNow Onboarding - Intune for Android v15.4.0
description: The Android v15.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v15-4-0.html
release: mobile
topic_type: reference
last_updated: "2023-02-02"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v15.4.0

The Android v15.4.0 release provides fixes for the application.

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

 PRB1597243

</td><td>

After submitting a reservation request in Now mobile app by Android mobile, the app returns to the same page after editing

</td><td>

 

</td><td>

1.  Log in to an instance in Now Mobile from Android.
2.  **Home tab** &gt; **Helpful quick actions section** &gt; **Return to Workplace**.
3.  **Preparing to Return** &gt; **Reserve a Workspace**.
4.  **See what's available** &gt; **Search All**.
5.  Provide required details, like building, floor, and dates.
6.  Click **Next**.
7.  Select a location.
8.  Click **Submit**.
9.  After submission, from the bottom buttons, click **Edit reservation**.
10. Click **Next**.
11. Click **Next**.
12. From this page, change 'Reservation Visibility' to another option.
13. Click **Submit**.
14. Repeat the steps 9 to 13.

 After changing 2 or 3 times, the 'Reservation details' page becomes empty when logged-in from an Android phone. In iOS, it displays details as expected.

</td></tr><tr><td>

Mobile Android

 PRB1609741

</td><td>

Push notifications display incorrectly when fields start and end with braces

</td><td>

For example, '\[blah\]' or '\{bloop\}'.

</td><td>

1.  Open the Now mobile app.
2.  Navigate to the platform.
3.  Open an incident.
4.  Click **sendiSMS** from related links.

 Expected behavior: The notification contains a field that starts and ends with braces.

 Actual behavior: The notification is missing fields that start and end with braces.

</td></tr><tr><td>

Mobile Android

 PRB1616771

</td><td>

Fields aren't changing to read-only in Android's Mobile app

</td><td>

The field isn't greyed out even though it's non-editable.

</td><td>

1.  Create an input form screen.
2.  Create an action item.
3.  Create a mobile function \(sys\_sg\_button\).
4.  Associate it with the action item created earlier.
5.  Add the mobile function to any of the Applets.
6.  Create a UI rule to make the field read-only on the input form screen.

 Expected behavior: The read-only field should be greyed out in the input form screen.

 Actual behavior: The read-only field isn't greyed out, though it's not editable.

</td></tr><tr><td>

Mobile Android

 PRB1621875

</td><td>

The user is unable to enter composite characters on a Korean keyboard when entering text on the input form screen

</td><td>

The user can only observe composite characters by posting a work note or comment in an activity stream.

</td><td>

1.  Enable a Korean keyboard input in the device settings.
2.  On Samsung, navigate to **Settings** &gt; **General Management** &gt; **Samsung Keyboard settings** &gt; **Languages and types**.
3.  Change 'Querty' to 'Chunjiin'.
4.  Open any input form screen.
5.  Start typing multiple characters.

 Expected behavior: Composite characters are formed.

 Actual behavior: Only a single character is allowed.

</td></tr><tr><td>

Mobile Android

 PRB1622705

</td><td>

Navigating deep into a tab stack causes performance issues

</td><td>

 

</td><td>

1.  Install FSM.
2.  Log in as any user with some tasks.
3.  Open any work order task.
4.  Open the 'Related' tab.
5.  Tap 'Work order' in related work orders.
6.  Repeat steps 4 and 5 until you are many levels deep \(6+\).

 Expected behavior: The UI should behave in a performant manner.

 Actual behavior: The UI starts to drop frames and performance is noticeably impacted.

</td></tr><tr><td>

Mobile Android

 PRB1628319

</td><td>

When modifying non-string inputs on input form screens, there's a delay before the UI updates

</td><td>

The delay should be limited to text input. Other inputs should have UI rules run immediately, which should complete before the UI updates.

</td><td>

1.  Open Agent app.
2.  Use any instance later than Rome.
3.  Install FSM with demo data.
4.  Log in as an agent.
5.  Open a work order task.
6.  Tap the top menu.
7.  Edit the task.
8.  Change the start or end date.

 Expected behavior: The UI should reflect the updated date immediately.

 Actual behavior: There's a 1.5 second delay before the UI updates.

</td></tr><tr><td>

Mobile Platform

 PRB1600854

 [KB1169099](https://hi.service-now.com/kb_view.do?sysparm_article=KB1169099)

</td><td>

Carried parameters aren't set in an embedded screen in San Diego

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

