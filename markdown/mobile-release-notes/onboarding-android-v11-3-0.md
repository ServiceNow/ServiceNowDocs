---
title: Mobile Onboarding for Android v11.3.0
description: The Android v11.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v11-3-0.html
release: mobile
topic_type: reference
last_updated: "2021-01-20"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v11.3.0

The Android v11.3.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile Android \(non-classic\)

 PRB1424697

</td><td>

The back button is incorrectly announced on all screens in the app

</td><td>

 

</td><td>

1.  Log in to the instance in an Android device and have 'Talk back' on.
2.  Navigate to the work order task or any form and activate the back button.

 Notice that the screen reader announces it as 'navigator button'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1449157

</td><td>

The primary color of the client theme is not applied to the buttons on the Activity Form screen correctly

</td><td>

 

</td><td>

1.  Log in as admin on the Platform UI.
2.  Navigate to **System Mobile** &gt; **Mobile Branding** &gt; **Client Themes**.
3.  Click to open the client theme 'Default'.
4.  Set the primary to '\#000000', which is black.
5.  Navigate to **System Mobile** &gt; **Mobile Branding** &gt; **Native Clients**.
6.  Set the client theme of the app to 'Default'.
7.  Request a 'Developer Laptop \(Mac\)' on the portal.
8.  Log in as admin via the app.
9.  Navigate to **For Me** &gt; **My Requests**.
10. Click to open the requested item created in Step 7.
11. Navigate to the 'Update' form screen.

 Expected behavior: The color of the buttons \(**Add additional comment**, **Add work note** and **Add attachment**\) on the Activity Form screen should be '\#000000'.

 Actual behavior: The color of the buttons on the Activity Form screen is not changed.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1451235

</td><td>

The app crashes on click of the action which has a special character '&gt;'

</td><td>

 

</td><td>

1.  Log in to a Paris instance.
2.  Open a record that contains a field with the special character '&gt;'.
3.  Click the action which contains the field in it.

 Notice that the mobile app crashes.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1451678

</td><td>

The cart icon doesn't show the number of items on the main page

</td><td>

The cart icon in the mobile header does not show the number of items in the cart when the open cart function is added to a custom applet launcher. Note that the cart functionality must be enabled through the system property glide.sc.cart.enabled.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1452003

</td><td>

The luminosity contrast ratio of the **Edit** button text is 3.7:1, which is less than 4.5:1

</td><td>

 

</td><td>

1.  In the mobile app, log in to the instance.
2.  Navigate to 'Service Desk agent', and then launch demo.
3.  Navigate to 'My Incidents'.
4.  Navigate to the created incident and activate it.

'My incident' screen will appear.

5.  Activate any ticket that appears on the screen.
6.  Navigate to the **Menu** button and activate it.

The **Edit** button and other UI action buttons will appear.

7.  Open the CCA tool.
8.  Check the foreground and background ratio for the **Edit** button text and observe whether it is less than 4.5:1 or not.

 Expected behavior: The luminosity contrast ratio of the **Edit** button text should be greater than or equal to 4.5:1.

 Actual behavior: The luminosity contrast ratio of the **Edit** button text is 3.7:1, which is less than 4.5:1.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1454660

</td><td>

Cannot attach files from OneDrive

</td><td>

 

</td><td>

1.  Configure an instance so that you can add an attachment \(for example, through the activity stream\).
2.  Make sure you have a license to use OneDrive.
3.  Install the OneDrive app on your device and log in, and make sure you have a file available.
4.  Log in to the ServiceNow app.
5.  Attempt to add an attachment.

 Notice that the error message 'The selected content is not a file' appears.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1456634

</td><td>

The success message doesn't display for footer functions

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also contains fixes for several accessibility-related issues and a pagination issue on the list, as well as other performance improvements and minor bug fixes.

**Note:** This version is compatible with Quebec Early Availability instances.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

