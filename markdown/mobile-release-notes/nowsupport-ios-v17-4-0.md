---
title: Now Support for iOS v17.4.0
description: The iOS v17.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowsupport-ios-v17-4-0.html
release: mobile
topic_type: reference
last_updated: "2024-04-04"
reading_time_minutes: 5
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for iOS v17.4.0

The iOS v17.4.0 release provides fixes for the application.

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

 PRB1733722

</td><td>

Siri Shortcuts is only displayed in debug mode build and not in App Center build

</td><td>

 

</td><td>

1.  Provision an instance with the latest App Center build downloaded.
2.  Navigate to **Settings** &gt; **Preferences**.

 Expected behavior: The Siri shortcut should be displayed in the App Center build.

 Actual behavior: The Siri shortcut is not displayed in the App Center build. Instead it is displayed in the debug build.

</td></tr><tr><td>

Mobile iOS

 PRB1738630

</td><td>

Special characters in questionnaire details are not displayed correctly in the Mobile Agent app

</td><td>

 

</td><td>

1.  Open the Agent mobile app in iOS.
2.  Navigate to 'My work'.
3.  Click any task under 'My tasks'.
4.  Click the three dots.
5.  Click Take questionnaire.
6.  Open the first questionnaire.
7.  Scroll down to see Ã© , which does not seem correct.

 Expected behavior: The text should render as 'extérieure'.

 Actual behavior: The text displays as Ã© which means it is not rendering the special character properly.

</td></tr><tr><td>

Mobile iOS

 PRB1697417

</td><td>

'Post' is not translated correctly in a base instance

</td><td>

When using Now Mobile in Canadian French, the word 'Après' should actually be 'Suivant'.

</td><td>

1.  Open the Now Mobile app.
2.  Change the language to French prior to entering credentials.
3.  In the system settings, navigate to the Now Mobile settings and change the preferred language from English to Canadian French.
4.  After logging in, navigate to the house icon or **Accureil**.
5.  Under 'Mes elements' select **Mes demanded**.
6.  Select the first record, then when the record opens, select the **Mises a jour** tab.
7.  Type in the comment box.

 When the composer modal pops up, observe that either 'Post' or 'Après' is untranslated.

</td></tr><tr><td>

Mobile iOS

 PRB1734936

</td><td>

Inline Predictions breaks Activity Stream entries

</td><td>

When adding a comment or work note to a record via the Activity Stream with iOS Inline Predictive text enabled, predictive text suggestions are automatically added to the typed text, resulting in unwanted/extra characters being added.

</td><td>

1.  Open NOW Mobile.
2.  Tap **Home**.
3.  Tap **My requests**.
4.  Tap any of the requests.
5.  Tap the **Updates** pill.
6.  Tap **Add** comment.
7.  Type 'Can I please get an update on this request'.

 Expected behavior: The text being typed by the user is entered.

 Actual behavior: Predictive text auto-completes several words, resulting in garbled text as the user types.

</td></tr><tr><td>

Mobile iOS

 PRB1739201

</td><td>

Now Mobile content publishing campaign banners disappear or do not load

</td><td>

The contents of the content publishing campaign section disappears as the user scrolls through it. This occurs when there is an empty record section above the campaign section that is hidden when empty.

</td><td>

1.  Set up an ALP with a campaign section that has more than one record \(for example, more that one banner image\).
2.  Add a record section above the campaign section that is hidden when empty and ensure that there are no records in this section.

 Expected behavior: The images are loaded properly on the carousel.

 Actual behavior: The images are not loaded or are disappearing when swiping through the carrousel. They only appear when the user starts scrolling down.

</td></tr><tr><td>

Mobile iOS

 PRB1741168

</td><td>

The error message 'UI Rule Error. Unable to submit' is observed when using a UI Rule on a function

</td><td>

Setting any input to 'visible : false' causes the error.

</td><td>

1.  Log in to a Vancouver or Utah Instance.
2.  Activate the ITSM Mobile Agent Plugin.
3.  Disable the **Advanced** Option for the Edit Input Form Screen.
4.  Create a UI rule on the above Input Form Screen to set any input to 'Visible false'.
5.  Open an incident and click **Edit Function**.
6.  Change the value of the short description.

 Expected behavior: There is no UI Rule error. The short description can be changed.

 Actual behaviour. There is a UI Rule Error. The user is unable to submit.

</td></tr><tr><td>

Mobile iOS

 PRB1740206

</td><td>

An .ics file downloaded from the Walkup Visits widget doesn't work as expected

</td><td>

After configuring the out-of-the-box Walkup Visits widget in the Now Mobile app, if a user schedules a visit from it, there is an option for adding the appointment to the calendar. It downloads the .ics file which is opened as plain text in the iOS app while it opens the calendars application from the iOS Safari browser.

</td><td>

1.  Activate the Walk-up Experience plugin \(sn\_walkup\). Configure a Mobile Web Screen to base instance Walkup Visit page \(for example, URL=/mesp?id=walkup\_visit\) in the Now Mobile app.
2.  Log in with the iOS Now Mobile App and navigate to the the Mobile Web Screen configured above.
3.  Select **Plan your visit** and then any location.
4.  Fill in the form to schedule an appointment.
5.  After scheduling the appointment, Select **Add to iCalendar**.

 Observe that the .ics file is opened as plain text.

</td></tr><tr><td>

Mobile iOS

 PRB1741894

</td><td>

The item execution script doesn't work as expected

</td><td>

When an item execution script fails, the error message gets printed in the record screen but not in the input form screen. All of the fields in the input form screen are cleared, requiring the user to fill in the inputs again.

</td><td>

1.  Log in to any instance.
2.  Create an input form screen with a few inputs and make it callable from any task record.
3.  In the action item, make sure to set the type to 'Script' and add a script.
4.  In the associated function, enable **Show confirmation message** and fill in other mandatory fields \(such as Confirmation message, Confirm label, Cancel label, etc.\).
5.  Navigate to the task record where the input form screen is linked, fill out the form, and submit.

 Notice that the user is redirected to the record screen, and the error message gets printed in the record screen but not in the input form screen.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

