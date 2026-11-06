---
title: Mobile Agent for iOS v22.3.0
description: The iOS v22.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-ios-v22-3-0.html
release: mobile
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 9
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v22.3.0

The iOS v22.3.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS

PRB2081491

</td><td>

The **Done** button text on the barcode scan review screen is unreadable on iOS 26

</td><td>

On devices running iOS 26, the **Done** button text on the barcode scan review screen blends into the background, which makes the button difficult to see.

</td><td>

1.  Log in to the ServiceNow Agent app on an iOS 26 device as a Field Service Management \(FSM\) technician.
2.  Navigate to My Work and open a work order task.
3.  Select the Asset Usage tab.
4.  Under Assets Used or Assets Removed, select **See all**.
5.  Select the more options menu on an asset usage entry, for example, Repair in Place.
6.  Scan a barcode.
7.  Select **Review**.

 Expected behavior: The**Done** button text is legible against its background.

 Actual behavior: The**Done** button text blends into the background and is unreadable.

</td></tr><tr><td>

Mobile iOS

PRB2088834

</td><td>

A blank screen appears and two back actions are required when leaving a requested item opened from Virtual Agent

</td><td>

After a user orders an item through Virtual Agent in the mobile app and opens the requested item from the conversation, selecting the **Back** button displays a blank white screen. A second back action is required to return to the previous screen.

</td><td>

1.  Log in to the mobile app on an iOS device.
2.  Open Virtual Agent.
3.  Enter 'I need a new laptop' and follow the prompts to order the item.
4.  When the order is complete, select the request card in the conversation.

The requested item opens.

5.  Select the **Back** button.

 Expected behavior: The user is returned to the previous screen with a single back action and no blank screen appears.

 Actual behavior: A blank white screen appears, and a second back action is required to exit the screen.

</td></tr><tr><td>

Mobile iOS

PRB2089475

</td><td>

Decimal values entered with a comma aren't handled correctly in the FSM mobile app on iOS when the region is set to France

</td><td>

In the Field Service Management \(FSM\) mobile app on iOS, when the device language and region are set to French, a decimal value entered with a comma \(for example, 0,75\) in the **Count** field when logging an issue is accepted instead of rejected. As a result, the value may not be saved correctly.

</td><td>

1.  On an iOS device, open **Settings** &gt; **General** &gt; **Language &amp; Region**, and set both the language and region to French.
2.  Open the ServiceNow Agent app, set the language to French on the login page, and log in.
3.  In the app settings, set the account language to French.
4.  Navigate to **My Work** and open a work order task.
5.  Select the more options menu and select the option to log an issue.
6.  In the **Count** field, enter 0,75 and save.

 Expected behavior: The comma is rejected at input, consistent with the Android app.

 Actual behavior: The value 0,75 is accepted.

</td></tr><tr><td>

Mobile iOS

PRB2086208

</td><td>

Time sheet hours entered with a comma are converted to whole numbers on iOS when the region is set to France

</td><td>

In the mobile app on iOS, when the device region is set to France, hours entered on a time sheet with a comma as the decimal separator \(for example, 2,11\) are converted to a whole number \(211\) after the entry is submitted.

</td><td>

1.  On an iOS device, open Settings, select General, then select Language &amp; Region, and set the region to France.
2.  In the mobile app, navigate to Settings, select Preferences, then select Language, and set both the preferred language and account language to French.
3.  Log in to the instance.
4.  On the Time Sheets tab, open a time sheet.
5.  Enter an hours value with a comma, for example, 2,11.
6.  Submit the entry.

 Expected behavior: The value remains in its original comma format \(2,11 h\) on the time entry and in the day-of-week title.

 Actual behavior: The value is converted to a whole number \(211\).

</td></tr><tr><td>

Mobile iOS

PRB2087440

</td><td>

Now Mobile app crashes when opening an assessment task from a journey on iOS

</td><td>

In the Now Mobile app on iOS, the app crashes when a user opens an assessment task from the 'To do' page of a journey.

</td><td>

1.  Log in to the Now Mobile app on an iOS device as a user who has an assessment task assigned in a journey.
2.  Navigate to Journeys and select the My journeys tab.
3.  Select a journey.
4.  Select the 'Tasks for you' tab.
5.  Select an assessment task, for example, a task to complete a culture and character assessment.
6.  Navigate to the 'To do' page.
7.  Select the same assessment task.

 Expected behavior: The assessment task opens without the app crashing.

 Actual behavior: The app crashes.

</td></tr><tr><td>

Mobile iOS

PRB2095184

</td><td>

Selecting a link after a session becomes invalid opens Safari instead of logging out the user

</td><td>

When a user's session is no longer valid and the user selects a link in the Now Mobile app, a message states that the session is invalid. After the user acknowledges the message, Safari opens to the link destination instead of logging the user out.

</td><td>

1.  Log in to the Now Mobile app on an iOS device.
2.  On the instance, invalidate the user's session token.
3.  In the Now Mobile app, select a link.

A message states that the session is invalid.

4.  Select **OK**.

 Expected behavior: The user is logged out of the app.

 Actual behavior: Safari opens with the link destination.

</td></tr><tr><td>

Mobile iOS

PRB2087062

</td><td>

BlackBerry MAM versions of the Now Mobile and Agent apps display a blank screen on iOS 27

</td><td>

On devices running iOS 27, the BlackBerry Mobile Application Management \(MAM\) versions of the Now Mobile and ServiceNow Agent apps display a blank white or black screen at launch instead of the login or home screen. This is due to a compatibility issue between iOS 27 and the BlackBerry Dynamics software development kit \(SDK\) version included in the apps.

</td><td>

1.  Install the BlackBerry MAM version of the Now Mobile or ServiceNow Agent app on an iOS 27 device.
2.  Launch the app.

 Expected behavior: The app loads and displays the login or home screen.

 Actual behavior: A blank screen appears, which is white or black depending on the device theme.

</td></tr><tr><td>

Mobile iOS

PRB2088325

</td><td>

Now Mobile app crashes when filtering AI Search results by knowledge base on iOS

</td><td>

In the Now Mobile app on iOS, when the app is used in Japanese, the app crashes when a user filters AI Search results on the Knowledge tab by knowledge base.

</td><td>

1.  Log in to the Now Mobile app on an iOS device with the language set to Japanese.
2.  Open the Knowledge tab.
3.  Select **Search** and enter a search term that returns results.
4.  Select the filter button.
5.  Select Knowledge Base, select a knowledge base, and then apply the filter.

 Expected behavior: The search results are filtered by the selected knowledge base.

 Actual behavior: The app crashes.

</td></tr><tr><td>

Mobile iOS

PRB2098531

</td><td>

Team approval requests intermittently don't appear on the Time Sheets tab until 'See all' is selected

</td><td>

In the Now Mobile app on iOS, the Team Approval Requests section on the Time Sheets tab intermittently appears empty even when requests exist. The requests appear only after the user selects **See all**.

</td><td>

1.  Launch the Now Mobile app on an iOS device and log in as a user with pending team time sheet approvals.
2.  Wait for the app to fully load and open the first tab.
3.  Open the Time Sheets tab.
4.  View the Team Approval Requests section.

 Expected behavior: The section displays the pending requests.

 Actual behavior: The section is empty.

</td></tr><tr><td>

Mobile iOS

PRB2089834

</td><td>

Card layout and field alignment are incorrect in the Now Mobile app on iOS

</td><td>

In the Now Mobile app on iOS, cards in list rows and fields on some record screens are misaligned compared to the same screens on Android.

</td><td>

1.  Log in to the Now Mobile app on an iOS device.
2.  Navigate to a tab that displays records as cards.

Notice the alignment of the card in each row.

3.  Open a record and view its fields and screen segments.
4.  Compare the same screens on an Android device.

 Expected behavior: Cards and fields are aligned consistently with Android.

 Actual behavior: Cards and fields are misaligned on iOS.

</td></tr><tr><td>

Mobile iOS

PRB2091088

</td><td>

The bottom tab bar background color on iOS versions earlier than iOS 26 is inconsistent with Android

</td><td>

In the mobile apps on iOS versions earlier than iOS 26, the bottom tab bar uses a different background color than the same apps on Android.

</td><td>

1.  Open the mobile app on an iOS device running a version earlier than iOS 26.
2.  Open the same app on an Android device connected to the same instance.
3.  Compare the background color of the bottom tab bar on both devices.

 Expected behavior: The bottom tab bar uses the same background color on both platforms.

 Actual behavior: The bottom tab bar on iOS uses a different background color than on Android.

</td></tr><tr><td>

Mobile iOS

PRB2094915

</td><td>

Quick links tiles ignore the configured background color on iOS

</td><td>

On iOS, tiles in a Quick links section that use the Icon display type show the default theme background instead of their configured background color. The configured foreground color is still applied.

</td><td>

1.  On the instance, make sure the mobile home screen contains a navigation section with the display type set to Icon, a vertical orientation, and a column count of two \(for example, the base instance Quick links section\), with a background color configured for each button.
2.  Log in to the Now Mobile app on an iOS device.
3.  On the Home tab, scroll to the Quick links section.

 Expected behavior: Each tile uses its configured background color.

 Actual behavior: All tiles use the default theme background, for example, white in light mode.

</td></tr><tr><td>

Mobile iOS

PRB2087479

</td><td>

Otto onboarding pop-up can reappear after switching instances

</td><td>

In the mobile app on iOS, the Otto onboarding pop-up can appear again after a user switches to another instance and then back, even if the user has already dismissed the pop-up.

</td><td>

1.  Log in to the mobile app on an instance with Otto enabled as a user who has already dismissed the Otto onboarding pop-up.

Notice that the pop-up doesn't appear.

2.  Switch to a different instance that doesn't have Otto enabled and log in.
3.  Switch back to the first instance.

 Expected behavior: The Otto onboarding pop-up doesn't appear.

 Actual behavior: The Otto onboarding pop-up appears.

</td></tr><tr><td>

Mobile iOS

PRB2082214

</td><td>

Removing an instance from the account list doesn't clear the device trust credential on iOS

</td><td>

In the ServiceNow Agent app on iOS, removing an instance from the account list doesn't clear the trusted device credential. When the instance is added again, the user isn't prompted to register the device again, which is inconsistent with the Android app.

</td><td>

1.  On an instance with Adaptive Authentication and device trust configured, register an iOS device as a trusted device with the quick response \(QR\) code flow while on a trusted network.
2.  Log in to the ServiceNow Agent app from outside the trusted network.

Notice that login succeeds because device trust is active.

3.  Open the instance list in the app and remove the instance.
4.  Add the same instance again.
5.  Log in from outside the trusted network.

 Expected behavior: The user is prompted to register the device again.

 Actual behavior: The user isn't prompted to register the device again, and the previous trust credential is still used.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-available-versions.md)

