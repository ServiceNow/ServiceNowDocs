---
title: Now Mobile for iOS v18.3.0
description: The iOS v18.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v18-3-0.html
release: mobile
topic_type: reference
last_updated: "2024-10-03"
reading_time_minutes: 3
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v18.3.0

The iOS v18.3.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_uw1_y14_31c" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS

 PRB1796531

</td><td>

The read-only Date/Time field is editable

</td><td>

The Date/Time field is editable on iOS app 18.0.0 or above, but it should be read-only.

</td><td>

1.  Create a Date/Time field in an input form screen in Mobile App Builder.
2.  Set it as 'Read-only' in Mobile App Builder.
3.  Open the input form screen on iOS App 18.0.0 or above.
4.  Tab the field.

 Observe that the field is editable.

</td></tr><tr><td>

Mobile iOS

 PRB1789000

</td><td>

Favorites do not get saved after switching instances

</td><td>

Favorites are not saved when logging into one instance after logging out of another.

</td><td>

1.  Open mobile \(requestor\) app.
2.  Log in to the instance 'appw'.
3.  Log out of the instance.
4.  Log in to the instance 'appv'.
5.  In the AppletList section tap **ListEmptyState** &gt; **Favorites**.

 Expected behavior: The favorites get saved.

 Actual behavior: The bookmark icon does not get filled and favorites do not get saved in the favorites screen.

</td></tr><tr><td>

Mobile iOS

 PRB1794170

</td><td>

The user is unable to remove favorited items from Now Mobile

</td><td>

The **Favorite** tile can't be removed.

</td><td>

1.  Log in to Now Mobile.
2.  Select **Request IT assistance**.
3.  Select **Favorite**.
4.  Navigate to the home page and refresh.
5.  Tap the **Favorite** tile, remove it, and refresh.

 Notice that the Favorite tile doesn't go away.

</td></tr><tr><td>

Mobile iOS

 PRB1756073

</td><td>

The user is not redirected to the barcode scanner screen

</td><td>

Jump-to-screen functionality after a successful action completion doesn't work as expected.

</td><td>

1.  Log in to the Mobile Agent app.
2.  Navigate to **Barcode scanner screen** &gt; **Scan Barcode** &gt; **Record screen**.
3.  Select the 'Foot' function configured to update one of the fields.
4.  Submit.

 Expected behavior: The user is redirected to the barcode scanner screen.

 Actual behavior: The user stays on the record screen.

</td></tr><tr><td>

Mobile iOS

 PRB1794694

</td><td>

Fulfillment instruction text is truncated in Now Agent

</td><td>

The agent is unable to view text for fulfillment instruction under the 'Fulfillment Instruction' section in a case on Now Agent.

</td><td>

1.  Log in to the instance with the 'Workplace or Agent Mobile' plugin installed.
2.  Create records and assigned them to the agent: sn\_wsd\_case\_workplace\_case.
3.  Log in to the Mobile app as the assigned agent.
4.  Check the records and 'Fulfillment Instruction' screen.

Notice that fulfillment instruction text is visible.

5.  Refresh the screen by swiping down.

 Expected behavior: The text for fulfillment instruction should remain same.

 Actual behavior: The text is small and not readable.

</td></tr><tr><td>

Mobile iOS

 PRB1797932

</td><td>

The Mobile UI rule to make the date field read-only doesn't work on iOS devices

</td><td>

 

</td><td>

1.  Log in to an Agent Mobile instance.
2.  Navigate to **My work** &gt; **My Incidents.**
3.  Open any Incident record.
4.  Select the top menu functions and select **Test UI Rule**.
5.  Set the Category to 'Yes'.
6.  Set the Sub Category to 'Yes'.

 Expected behavior: The 'UI Date 1' field should be read-only.

 Actual behavior: The 'UI Date1' field is editable.

</td></tr><tr><td>

Mobile iOS

 PRB1719075

</td><td>

A payload sent by Virtual Agent from the mobile app is different from one sent from the desktop

</td><td>

A payload sent by Virtual Agent from the mobile app and desktop are different

</td><td>

1.  Log in to any base Vancouver instance from two separate sessions, one via the NOW mobile app as an end user, and other via desktop as an agent.
2.  Initiate a chat from the mobile app and accept the chat from desktop view.
3.  Select the attachment icon and select **Open camera** or **Open library**.
4.  Once the image is attached, open the sys\_cs\_conversation record from the back-end and check for the payload of the message.
5.  Select the attachment icon again and select Attach a file.
6.  Repeat Step 4.

 Expected behavior: The payload from the image uploaded via camera/library and 'Attach a file' are the same.

 Actual behavior: The payload from the image uploaded via camera/library and 'Attach a file' are different.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

