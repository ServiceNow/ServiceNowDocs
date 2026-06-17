---
title: Mobile Onboarding for iOS v12.1.0
description: The iOS v12.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-05-20"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v12.1.0

The iOS v12.1.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS \(non-classic\)

 PRB1430361

</td><td>

Navigating to a Service Portal page directs to a Service Portal login page

</td><td>

After launching the mobile app and tapping a Service Portal service, the user is intermittently presented with a Service Portal login page.

</td><td>

1.  Place the app in the background.
2.  Ensure that enough time has passed that the access token needs to be refreshed.
3.  Launch the app.
4.  Immediately tap a 'Popular Services' card.

 Notice that a login page is rendered.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1441943

</td><td>

Luminosity contrast ratio for the 'Search' placeholder is less than 4.5:1

</td><td>

The luminosity contrast ratio for the 'Search' and 'Category' placeholders is 1.65:1, which is less than 4.5:1.

</td><td>

1.  Open the Agent mobile app.

The login screen appears.

2.  Navigate to **Service Desk agent** &gt; **Launch Demo**.
3.  Navigate to **My Incidents** &gt; **More** &gt; **New control** using the swipe gesture and activate it.
4.  Search for the caller 'Abel Tuter'.

 Expected behavior: The luminosity contrast ratio for the 'Search' placeholder should be equal to or greater than 4.5:1.

 Actual behavior: The luminosity contrast ratio for the 'Search' placeholder is 1.65:1, which is less than 4.5:1.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1456162

</td><td>

Unable to open the attachment file via Virtual Agent from Now Mobile

</td><td>

The following error appears in the syslog: 'Attempt to load invalid content type for image in table: incident, filename: xxxxxxxxxx.pdf: no thrown error'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1478837

</td><td>

Font sizes are inconsistent in iOS

</td><td>

A new form from a homepage and a new form from a list have different font sizes. For example, when creating an incident from the homepage, if the 'New Incident' function is placed in a homepage and a list applet, the fields from a new incident form have slightly bigger font.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1481132

</td><td>

KB articles show an attachment as unavailable after scrolling up and down several times

</td><td>

 

</td><td>

1.  In the Agent mobile app, log in to the instance.
2.  Click the settings icon in the bottom navigation bar and click **Offline**.
3.  Click **Download cache**.
4.  Once complete, enable offline mode and turn on airplane mode.
5.  Open a KB with attachments.
6.  Scroll to the bottom of the KB.

Notice the list of available attachment files.

7.  Scroll up and down multiple times.

 Notice that some attachment files show as unavailable.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1485101

</td><td>

The mobile app on iOS does not give a proper message if uploading an attachment fails on the activity screen

</td><td>

The iOS mobile app doesn't wrap the exception or error when the attachment upload API call fails.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1488487

</td><td>

The iOS WebView User-Agent string may have an incorrect format

</td><td>

This can cause some web applications to render incorrectly.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

