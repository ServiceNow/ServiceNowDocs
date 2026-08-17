---
title: Now Mobile - Intune for Android v22.0.0
description: The Android v22.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-android-v22-0-0.html
release: mobile
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 7
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for Android v22.0.0

The Android v22.0.0 release provides fixes for the application.

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

 PRB2017687

</td><td>

Bundled language not applied when user hasn't explicitly selected the app language

</td><td>

UI strings display in English.

</td><td>

1.  Navigate to Meu trabalho \(My Work\) tab.

Observe that the **See all** button next to the 'Minhas tarefas' section header is not translated \(displays **See all** instead of **Ver tudo**\).

2.  Select **See all** to open the full tasks list.
3.  Select the filter icon.

 Observe that the filter screen displays a mix of languages remain in English while field labels are correctly translated in Portuguese.

</td></tr><tr><td>

Android Mobile

 PRB2040002

</td><td>

'You were logged out' dialog translation issue

</td><td>

The translation is not consistent. The title, body and buttons are not all translated.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2026254

</td><td>

Embedded YouTube links throw Error 153

</td><td>

YouTube displays error 153 and the video does not play.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2003220

</td><td>

Quick Action Function instance not visible in Mobile Agent

</td><td>

The default icon should be a plus sign.

</td><td>

Log into a Mobile Agent app that has a quick action function instance on launcher screen.

 Observe that the quick action function instance is no longer visible.

</td></tr><tr><td>

Android Mobile

 PRB2031389

</td><td>

PDF viewer does not support panning/scrolling after zooming in, making zoomed content unreadable

</td><td>

When users open a PDF within the app, they can pinch-to-zoom in on the document. However, once zoomed in, there is no ability to pan or scroll across the zoomed content. The zoom only operates from the center point, leaving content at the edges inaccessible. This makes PDFs effectively unreadable when zoomed.

</td><td>

1.  Open any PDF attachment within the app \(for example, from a record's attachment list\).
2.  Pinch to zoom in on the PDF document.
3.  Attempt to drag/swipe with one finger to pan across the zoomed content.

 Expected behavior: User can pan/scroll the document in all directions to view zoomed content.

 Actual behavior: Document remains locked at center. No panning occurs. Content beyond the visible area is inaccessible.

</td></tr><tr><td>

Android Mobile

 PRB2005699

</td><td>

The **Close** button doesn't work after submitting an incident from the record producer

</td><td>

After submitting an incident from a record producer, a confirmation message is displayed; however, the **Close** button does not respond when clicked.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2023969

</td><td>

A second user PIN is not recognized in non-shared mode

</td><td>

 

</td><td>

Pre-requisites:

 1.  Set sys\_property glide.sg.require\_mobile\_application\_pin to true on the instance.
2.  Have two valid user accounts \(User1 and User2\) on the same instance.
3.  Fresh install or cleared app data.

 1.  Launch the ServiceNow mobile app
2.  Add the instance and log in as User1
3.  When prompted, create a PIN \(for example, 123456\) for User1
4.  Verify the app loads successfully with the PIN
5.  Navigate to **Settings** &gt; **Log out**.
6.  Log in as User2 on the same instance
7.  Close and relaunch the app so that it will be prompted with PIN
8.  When prompted, enter the earlier PIN \(123456\)

 Expected behavior: App should land on Home page

 Actual behavior: Incorrect PIN error is shown

</td></tr><tr><td>

Android Mobile

 PRB2033284

</td><td>

Opening the order guide genius results in mobile search takes the user to the catalog item page instead of the order guide page

</td><td>

The catalog item page has no visible Next option. Since there is no Next option, it is not possible to complete the order guide.

</td><td>

1.  Log in to any Zurich instance in the Now Mobile app.
2.  Search for a order guide in the search bar.
3.  Select the **Genius Results** card. Do not select **Request**, instead select the card.

 Notice that the user is taken to the catalog item page where there is no visible **Next** option.

</td></tr><tr><td>

Android Mobile

 PRB2038234

</td><td>

The Reference List in a parameter input form should not send DependentValue

</td><td>

The classification reference list call that occurs when the user taps on the field fails with 500 error.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1965520

</td><td>

The **Submit** button is still enabled when input changes

</td><td>

The **Submit** button on an input form screen must be disabled when input changes until all UI rule conditions have been evaluated.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2008004

</td><td>

unreadConversation API on Now Mobile returns an inflated badge count and empty chat history when mobileChannelType and mobileChannelId are not passed

</td><td>

The /unreadConversation API on Now Mobile returns an incorrect \(inflated\) unread notification badge count on the Now Assist stars icon. When the user taps the clock icon to view chat history, the same inflated count is shown but no conversations are listed \('No chat found'\).

</td><td>

1.  Log in to Now Mobile \(iOS or Android\) on the affected instance.
2.  Navigate to Now Assist \(stars icon\).

Observe the notification badge on the stars icon showing a non-zero count.

3.  Open Now Assist.
4.  Tap the clock icon to open chat history.
5.  Observe the chat history view.

 Expected behavior: The notification badge should show 0 \(or no badge\) when there are no active unread conversations. The chat history view should accurately reflect the user's conversation history.

 Actual behavior: The notification badge displays a non-zero count \(matching stale records in \[sys\_cs\_message\_last\_read\]\). The chat history view shows the same inflated count but displays 'No chat found' with no conversations listed.

</td></tr><tr><td>

Android Mobile

 PRB2026492

</td><td>

Universal linking opens the URL in a browser rather than inside the Agent app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2013102

</td><td>

Currency code is not displayed in a doughnut chart on Android while it appears on iOS

</td><td>

In Mobile Agent application, the currency code \(RM\) configured in the data visualization is displayed correctly inside the doughnut chart on iOS but is missing on Android.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2034164

</td><td>

The app crashes when a screen rotates with the signature input bottom sheet open

</td><td>

This occurs when a screen rotates with the signature input bottom sheet open.

</td><td>

1.  From the 'More' tab, access My work.
2.  Open any WOT and from Details open the parent Work order.
3.  Select the **Sign and Confirm** footer button.

Observe that the signature input screen shows up.

4.  Rotate the screen.

 Observed that the app crashes.

</td></tr><tr><td>

Android Mobile

 PRB2032631

</td><td>

A Slack deep link opens inside the Agent app's task instead of launching Slack as separate task \(missing FLAG\_ACTIVITY\_NEW\_TASK\)

</td><td>

In Mobile Agent v21.3.0 on Android, tapping a MyHub function-link button with the Slack deep-link URL \(slack://open\) launches Slack's deep-link Activity inside the Agent app's task. Android Recent Apps shows the task labeled 'Agent' with Slack's UI on top, instead of Slack appearing as its own separate task.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2017507

</td><td>

Voice Agent doesn't work on Android devices when using an account nickname

</td><td>

If the nickname is different from the instance name, voice chat does not work.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2053357

</td><td>

Hidden-by-script inputs are being populated during multi scanning

</td><td>

The counter on the Review tab counts up by one on every third scan. Two of three scan values are not displayed in the input.

</td><td>

1.  Create an input form screen \(Parameter screen\).
2.  Create a Barcode section of type 'Barcode'.
3.  Create three inputs of type 'Barcode' and add them to the Barcode section.
4.  In the barcode section, navigate to Variable tab and add a variable that uses a script to hide two of the three inputs.
5.  On the mobile device, open the Agent \(or Now Mobile\) app.
6.  Navigate to the barcode section.
7.  Start scanning different barcodes.

 Expected behavior: The counter on the Review tab should count up by on on each scan, because one multi-scan consists of only one scan, since the other inputs are hidden.

 Actual behavior: The counter on the Review tab counts up by one on every third scan. Two of three scan values are not displayed in the input.

</td></tr><tr><td>

Android Mobile

 PRB2052695

</td><td>

Location Tracking background location copy needs update and translation

</td><td>

Google Play rejected a fulfiller/whitelabel app submission under the Prominent Disclosure and Consent Requirement of the User Data policy.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2030003

</td><td>

Incorrect device trust handling during multi-instance switching causes unintended logout and forced re-registration

</td><td>

Background API calls use incorrect or mismatched instance tokens resulting in forced logout.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB2040346

</td><td>

Filter panel reopens after returning to a list following a form submission

</td><td>

After returning to an offline list following a form submission, the filter panel \(DrawerLayout\) re-opens even though the user had closed it.

</td><td>

1.  Go offline.
2.  Open a list \(for example, the equipment list\).
3.  Tap the Filter menu to open the filter panel \(drawer\).
4.  Apply filters and close the panel.

Notice that the panel closes correctly.

5.  Open an item / input form from the list and submit it \(offline\).
6.  Return to the list.

 Expected behavior: The filter panel stays closed.

 Actual behavior: The filter panel is open again.

</td></tr><tr><td>

Android Mobile

 PRB2040091

</td><td>

AsyncAttachmentsUploadEnabled ignores ImageMaxDimensionPreset causing images to upload at full resolution

</td><td>

When AsyncAttachmentsUploadEnabled = true and ImageMaxDimensionPreset = Low/Medium/High, images upload at full resolution — the preset is ignored on the async upload path. The synchronous path \(AsyncAttachmentsUploadEnabled = false\) is unaffected and correctly downscales.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

