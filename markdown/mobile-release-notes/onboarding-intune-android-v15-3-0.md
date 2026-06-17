---
title: ServiceNow Onboarding - Intune for Android v15.3.0
description: The Android v15.3.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2023-01-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v15.3.0

The Android v15.3.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android \(non-classic\)

 PRB1622705

</td><td>

Navigating deep into a tab stack causes performance issues

</td><td>

 

</td><td>

1.  Install FSM on a base instance.
2.  Login as any user with some tasks.
3.  Open any WOT.
4.  Open the Related tab.
5.  Click a work order in Related Work Orders.
6.  Repeat steps 4 and 5 until you are many levels deep.

 Expected behavior: The UI should still behave without an affect on performance.

 Actual behavior: The UI starts to drop frames and the performance degrades.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1621875

</td><td>

The user is unable to enter composite characters on a Korean keyboard when entering text on the input form screen

</td><td>

The user can only observe composite characters by posting a work note or comment in an activity stream.

</td><td>

1.  Enable a Korean keyboard input in the device settings.

\(Note: On Samsung, navigate to **Settings** **&gt; General Management** **&gt; Samsung Keyboard settings** **&gt; Languages and types** and change Querty to Chunjiin\)

2.  Open any input form screen.
3.  Start typing multiple characters.

 Expected behavior: Composite characters are formed.

 Actual behavior: Only a single character is allowed.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1612984

</td><td>

Mobile UI rule does not work as expected in Android

</td><td>

The field does not hide when assignment group changes for the first time but gets hidden if you try to change it a second time.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1612041

 [KB1184889](https://hi.service-now.com/kb_view.do?sysparm_article=KB1184889)

</td><td>

Label for grouped input from bar code scanning is not showing up in Android

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1609815

</td><td>

Font size decreases in the Android NOW mobile app after upgrading to 14.5.0 when the language is traditional Chinese

</td><td>

 

</td><td>

1.  Log in to an instance on Now Mobile with the Chinese language plugin and select the Chinese language while logging in.
2.  Navigate to any applet where the user can see the list of the records \(make sure the record is in Chinese or update the record title and description with Chinese content\).
3.  Open the record and navigate back to the list.

 Observe that the font of the opened record gets smaller.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1609551

</td><td>

On the ServiceNow Mobile Agent app for Android, a user can always delete attachments on a form

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1602165

</td><td>

The Edit Case &gt; Product options shows text in many sizes

</td><td>

 

</td><td>

1.  Log in to the Agent mobile app on an Android device.
2.  Open any case by navigating to **Edit Case** &gt; **Product** to see the list of available products.

 Expected behavior: The list of available products has the same font size.

 Actual behavior: The list of available products has many different font sizes.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1597243

</td><td>

After submitting a reservation request in Now mobile app by Android mobile, the app returns to the same page after editing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1596466

</td><td>

Quantity and Cost are missing in the Agent app when creating incidental expenses in WOT

</td><td>

 

</td><td>

1.  Log in to the Agent mobile app on an Android device.
2.  Navigate to the My Work tab and open any assigned WOT.
3.  Click on the 3 dots in the top-right hand corner of the screen and select the 'Create incidental expense' action.
4.  Fill the field as Type: Non Standard Installation charges, in the second field, select 'Over the ceiling/roof'.

 Expected behavior: The Quantity and Cost fields are visible.

 Actual behavior: The Quantity and Cost fields are NOT visible.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1596400

</td><td>

The filter buttons in 'My Approvals' are described as 'unlabelled '

</td><td>

All filter buttons contain 'unlabelled' as a description.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1572307

</td><td>

Talkback does not have focus on play button

</td><td>

 

</td><td>

1.  Open the Now Mobile app and log in as admin user.
2.  Enable screen reader.
3.  Select Mobile Regression 2.
4.  Read through/interact with the first video.

 Actual behavior: The video play control does not inform a user they can play a video.

 Expected behavior: Non-vision users need to be informed that the control will play a video.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

