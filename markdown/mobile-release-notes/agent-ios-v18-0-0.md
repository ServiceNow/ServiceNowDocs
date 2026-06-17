---
title: Mobile Agent for iOS v18.0.0
description: The iOS v18.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-07-04"
reading_time_minutes: 9
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v18.0.0

The iOS v18.0.0 release provides fixes for the application.

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

 PRB1751431

 [KB1638841](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638841)

</td><td>

The Agent Mobile App crashes when opening an applet

</td><td>

The Agent Mobile App crashes when opening an applet using a button in a card template referring to Next Experience CSS variables if Next Experience UI is disabled.

</td><td>

1.  Set the system property 'glide.ui.polaris.experience' to false to disable the Next Experience UI.
2.  Log in to the Agent Mobile App.
3.  Navigate to **My work** &gt; **My tasks**.
4.  Open a record.

 Expected behavior: The record should be opened successfully in the Agent Mobile App.

 Actual behavior: The record is opened but the Agent Mobile App crashes.

</td></tr><tr><td>

Mobile iOS

 PRB1730998

</td><td>

The form screen record doesn't display when the user taps a notification

</td><td>

Setting a record state to 'Requested' triggers a push notification. Tapping the notification fails to take the user to a form screen that displays 'Approve Requested Item'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1643367

</td><td>

The Mobile Agent app scanner doesn't work on iPhone 14

</td><td>

The image is blurry when the user tries to scan from a close distance.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1765341

</td><td>

Low successful scanning rate for barcode input in the iOS app

</td><td>

Sometimes the barcode scanner does not respond to the barcode.

</td><td>

1.  Install IT Asset Management Mobile.
2.  Identify the input form screen 'Asset lookup'.
3.  Configure a function to navigate to this input form screen.
4.  On an iOS device, navigate to the input form screen.
5.  Scan a barcode.

 Observe that sometimes it does not respond to the barcode.

</td></tr><tr><td>

Mobile iOS

 PRB1733722

</td><td>

Siri Shortcuts is only displayed in the debug mode build, not the app center build

</td><td>

The Siri shortcut should be displayed in the app center build, but it is only displayed in the debug mode build.

</td><td>

1.  Provision an instance with the latest App Center build downloaded.
2.  Navigate to **Settings** &gt; **Preferences**.

 Expected behavior: The Siri shortcut should be displayed in the app center build.

 Actual behavior: The Siri shortcut is not displayed in the app center build. Instead, it is displayed in the debug mode build.

</td></tr><tr><td>

Mobile iOS

 PRB1765471

</td><td>

A custom app crashes with a PopOver Alert while the user is scrolling on iPad

</td><td>

The app intermittently crashes while scrolling on a form on iPad.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1734936

</td><td>

Inline Predictions breaks Activity Stream entries

</td><td>

When adding a comment or work note to a record via the Activity Stream with iOS Inline Predictive text enabled, predictive text suggestions are automatically added to the typed text, resulting in unwanted/extra characters being added.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1749472

</td><td>

Barcode scanning doesn't focus on the crosshair

</td><td>

Because the scanning area isn't well defined, it's difficult to catch a specific barcode when there are multiple barcodes caught in the frame.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1714977

</td><td>

In Now Mobile, the cursor jumps when the user types in Japanese

</td><td>

The cursor jumps between Japanese characters in the Additional Comments and Worknotes sections.

</td><td>

1.  Create a new incident.
2.  Navigate to My request and click the incident created in step 1.
3.  Select the **Updates** tab.
4.  Select **Add comment**.
5.  Type 'テストです' with the mobile Japanese keyboard and select the sentence from the suggestions.

 Expected behavior: The cursor should stay at the end of the text.

 Actual behavior: The cursor moves to between 'ト' and 'で'.

</td></tr><tr><td>

Mobile iOS

 PRB1743247

</td><td>

The user can't select between paged carousel images with Voice Over in Now Mobile

</td><td>

Swiping on the page doesn't do anything.

</td><td>

1.  Provision an instance with Voice Over enabled.
2.  Navigate to **More** &gt; **Campaigns**.
3.  Using Voice Over, focus on the paging component.

Notice that Voice Over says 'Page 1 of X, adjustable, swipe up or down with one finger to adjust the value'.

4.  While focused on the component, swipe up or down with one finger.

 Expected behavior: Swiping up or down changes to the previous or next image in the carousel.

 Actual behavior: The current image in the carousel is not changed.

</td></tr><tr><td>

Mobile iOS

 PRB1743319

</td><td>

Live Agent chat is stuck on a loading screen when the user closes and reopens the mobile app

</td><td>

When the user closes the mobile app without closing the chat conversation and then reopens it to connect to a live agent, they get stuck on the loading screen.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1742496

</td><td>

Selecting a deeplink URL navigates the user to the screen, but selecting the **Back** button shows a blank page

</td><td>

When the user selects a record, they are navigated to the screen provided in a deeplink. However when they select the **Back** button, a blank screen appears. The user must then select **Back** again to navigate to the home screen.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1738630

</td><td>

Special characters in questionnaire details are not displayed correctly on the Mobile Agent application

</td><td>

 

</td><td>

1.  Open the Agent mobile app in iOS.
2.  Navigate to 'My work'.
3.  Select any task under 'My tasks'.
4.  Select the three dots.
5.  Select **Take questionnaire**.
6.  Open the first questionnaire.
7.  Scroll down to see 'Ã©'.

 Expected behavior: The text should render as 'extérieure'.

 Actual behavior: The text displays unusual characters, which means it is not rendering the special character properly.

</td></tr><tr><td>

Mobile iOS

 PRB1739201

</td><td>

Failure attempting to upload attachments from the parameter screen

</td><td>

When attachments are added and the app is backgrounded then foregrounded, the files fail to upload.

</td><td>

1.  Open a parameter screen that has an attachment field.
2.  Select a few files and select **Add** in the attachment selection screen.
3.  Background the app and foreground it again.
4.  Select **Submit**.

 Expected behavior: All files get uploaded.

 Actual behavior: All files fail to upload.

</td></tr><tr><td>

Mobile iOS

 PRB1741168

</td><td>

The error message 'UI Rule Error. Unable to submit' is seen when using a UI Rule on a function

</td><td>

Setting any input to 'visible : false' causes the error.

</td><td>

1.  Log in to a Vancouver or Utah Instance.
2.  Activate the ITSM Mobile Agent Plugin.
3.  Disable the 'Advanced' Option for 'Edit Input Form Screen.
4.  Create a UI rule on the input form screen to set any input to 'Visible false'.
5.  Open a incident and click **Edit Function**.
6.  Change the value of the short description.

 Expected behavior: There is no UI Rule error. The short description can be changed.

 Actual behavior. There is a UI Rule Error. The user is unable to submit.

</td></tr><tr><td>

Mobile iOS

 PRB1734959

</td><td>

Content in a text field is cut off when text size is increased

</td><td>

 

</td><td>

1.  Log in to the Now Mobile app.
2.  Select **Welcome tab** &gt; **HR Onboarding Timeline section** &gt; **See all**.
3.  Navigate to iPhone settings and increase the text size.
4.  Navigate back to the app.

 Notice that the text is cut off.

</td></tr><tr><td>

Mobile iOS

 PRB1743865

</td><td>

Extra sessions are created for unreadMessage transactions

</td><td>

After enabling the 'Chat' quick action in the Now Mobile app, there are requests to /api/now/v1/cs/ consumerAccount/unreadMessage. These occur when the user is navigating around the app \(for example, refreshing the screen, switching tabs etc.\). The transactions create new sessions.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1740552

</td><td>

A UI Rule is not applied consistently on the Details screen after updating from an input form

</td><td>

When the user edits a record by adding a note, the red background of the note text disappears. This only occurs the second time the user edits a record and navigates back to the home screen.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1744191

</td><td>

A success message is displayed twice when adding a 'Log Incidental' to a work order task record

</td><td>

The first message appears for one second and disappears before the second message appears.

</td><td>

1.  Log in to any Vancouver instance in Agent Mobile.
2.  Select 'My tasks' on the home page and notice some wm\_task records.
3.  Open any record \(if any records are not visible for admin, impersonate a user with records\).
4.  Open the record and click on three dots on top right corner.
5.  Select the **Log Incidental** function.
6.  Fill in the fields required and click **Submit**.

 Notice that a success message is shown twice.

</td></tr><tr><td>

Mobile iOS

 PRB1733952

</td><td>

Content publishing mobile banners are not loading / disappearing in Now Mobile

</td><td>

The contents of the content publishing campaign section disappear as the user scrolls through them. This occurs when there is an empty record section above the campaign section that is hidden when empty.

</td><td>

1.  Set up an ALP with a campaign section that has more than one record \(for example, more that one banner image\).
2.  Add a record section above the campaign section that is hidden when empty and ensure that there are no records in this section.

 Expected Behavior: The images load properly on the carousel.

 Actual behavior: The images don't load or disappear when swiping through the carrousel. They only appear when the user starts scrolling down.

</td></tr><tr><td>

Mobile iOS

 PRB1741894

</td><td>

Item execution script doesn't work as expected

</td><td>

When an item execution script fails, the user is directed to the record screen and the error message gets printed in the record screen but not in the input form screen. This is an issue as all of the filled input fields in the input form screen are cleared off and the user needs to fill in all the inputs again.

</td><td>

1.  Log in to any instance.
2.  Create an input form screen with a few inputs and make it callable from any task record.
3.  In the action item, set the type to 'Script' and add a script.
4.  In the associated function, enable 'Show confirmation message' and fill in other mandatory fields \(such as Confirmation message, Confirm label, Cancel label, etc.\).
5.  Navigate to the task record where the input form screen is linked, fill out the form, and submit.

 Notice that the user is redirected to the record screen, and the error message gets printed in the record screen but not in the input form screen.

</td></tr><tr><td>

Mobile iOS

 PRB1756605

</td><td>

'My Task Map' crashes the Mobile Agent app on iPad

</td><td>

Crashing only occurs on certain map locations, yet when the location is updated it does not fix the issue in all instances.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1740206

</td><td>

An .ics file downloaded from the Walkup Visits widget doesn't work as expected

</td><td>

After configuring the out-of-the-box Walkup Visits widget in the Now Mobile app, if a user schedules a visit from it, there is an option for adding the appointment to the calendar. It downloads the .ics file which is opened as plain text in the iOS app while it opens the calendars application from the iOS Safari browser.

</td><td>

1.  Activate the Walk-up Experience plugin \(sn\_walkup\).
2.  Configure a Mobile Web Screen to a base instance Walkup Visit page \(for example, URL=/mesp?id=walkup\_visit\) in the Now Mobile app.
3.  Log in with iOS Now Mobile App and navigate to the Mobile Web Screen configured above.
4.  Select **Plan your visit** and then any location.
5.  Fill in the form to schedule an appointment.
6.  After scheduling the appointment, Select **Add to iCalendar**.

 Observe that the .ics file is opened as plain text.

</td></tr><tr><td>

Mobile iOS

 PRB1762684

</td><td>

An 'Action is blocked by policy' error appears when attempting to upload images

</td><td>

The error occurs when preventDataLeakageIn is false. This is because the IntuneMAMOpen LocationPhotos case is missing from the condition.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

