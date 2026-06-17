---
title: Now Mobile - Intune for iOS v18.1.0
description: The iOS v18.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-ios-v18-1-0.html
release: mobile
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v18.1.0

The iOS v18.1.0 release provides fixes for the application.

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

 PRB1774000

</td><td>

A space is added to the middle of an auto-corrected word

</td><td>

When adding a comment, misspelled words are auto-corrected with a space in the middle of the word and the cursor moves to the middle of the word.

</td><td>

1.  Ensure ITSM Mobile Agent is installed.
2.  Open the agent app on an iOS device.
3.  Open any record, such as an incident \(assign one to the currently logged in user if required\).
4.  Within the activity section of the incident, select the **Add comment** option to bring up the composer.
5.  Type any word that would be autocorrected \(for example, 'tessting'\).

 Notice that the word is auto corrected. However, a space is added in the middle of the word \(for example, 'tes ting'\). Also notice that the cursor moves to the middle of the word.

</td></tr><tr><td>

Mobile iOS

 PRB1766373

</td><td>

Theme color glitch issue for screens/icons on Mobile Device Management \(MDM\) configured instances

</td><td>

The instance displays a green theme.

</td><td>

1.  Open the Now Mobile App. In the instance name, type 'OMV' and log in to the app.
2.  The theme appears properly without any issues.
3.  Close and re-open the app, using the pre configured instance OMV to log in.

 Observe that the instance displays a green theme. The correct theme loads when the page is refreshed.

</td></tr><tr><td>

Mobile iOS

 PRB1769567

</td><td>

The **Translate** option from the user context menu isn't blocked when the 'Restrict cut, copy, and paste between other apps' protection policy is set

</td><td>

The 'target\(forAction' function overrides Intune's code to block the **Translate** option from being selected.

</td><td>

1.  Log in to an instance.
2.  Select any Incident.
3.  Tap and hold down on any text in any of the fields until the context menu appears.
4.  Select **Translate** from the user context menu.

 Expected behavior: The user observes an alert reading 'Action Not Allowed'.

 Actual behavior: The translation menu appears.

</td></tr><tr><td>

Mobile iOS

 PRB1767995

</td><td>

The user can't open a .WAV file

</td><td>

The user can't open a .WAV file attached in the Activity Stream

</td><td>

1.  Attach a .WAV file to an incident.
2.  Open the incident in the mobile app.
3.  Select the .WAV file in the Activity Stream of the incident.

 Expected behavior: The .WAV file is opened and played \(or at least downloaded to the device\).

 Actual behavior: An 'Unsupported file type' error is shown.

</td></tr><tr><td>

Mobile iOS

 PRB1769722

</td><td>

The 'Favorites' filter is removed when refreshing the list

</td><td>

Only the filtered list is displayed.

</td><td>

1.  Open the Agent app. Navigate to the 'My work' tab.
2.  Open the 'Breached incidents' list. Filter the list by 'Caller'.
3.  Save the filtered list as favorite.
4.  Navigate to the 'More' / 'Saved' tab.
5.  Open the last saved favorite.

Notice that the 'Bookmark' button displays as inactive even though it should be active.

6.  Refresh the list.

 Expected behavior: Only the filtered list is displayed.

 Actual behavior: The entire unfiltered list is displayed and the applied filter is reset.

 Note: The issue reproduces only with a 'reference' filter applied \(for example, Caller, Assigned to, etc.\). If the regular filter is applied the issue will not reproduce.

</td></tr><tr><td>

Mobile iOS

 PRB1780274

</td><td>

The barcode scanner intermittently fails to scan QR codes

</td><td>

 

</td><td>

1.  Log in to the Agent app.
2.  From **More**, select **Asset**.
3.  Select **Asset Lookup**.
4.  Scan a QR code.

 Expected behavior: The code is scanned and the details are shown on the app.

 Actual behavior: Nothing happens as the code doesn't get scanned.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

