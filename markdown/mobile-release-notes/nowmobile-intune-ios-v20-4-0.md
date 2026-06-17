---
title: Now Mobile - Intune for iOS v20.4.0
description: The iOS v20.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-ios-v20-4-0.html
release: mobile
topic_type: reference
last_updated: "2024-10-02"
reading_time_minutes: 2
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v20.4.0

The iOS v20.4.0 release provides fixes for the application.

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

 PRB1931580

</td><td>

Intermittently, there's fetch errors when a user submits some records

</td><td>

The user sees an error, either 'For Requestfor.NOWAPIError4 \(Requestfor.NOWAPIError\)' or 'Fetch error, please check fetch status'.

</td><td>

1.  Create a list of work order tasks in the 'Form' screen.
2.  Each task needs to have a link to a 'Cabrillo' page.
3.  The 'Cabrillo' page should contain a button to upload images or files.
4.  After selecting the images, or files through the upload manager, select the 'Back' menu to return to the 'Form' screen.

 Expected behavior: The user sees a list of work order tasks without an error.

 Actual behavior: The user sees a list of work order tasks and with error.

</td></tr><tr><td>

Mobile iOS

 PRB1924641

</td><td>

The chat icon is unresponsive when the user returns to the chat after accessing an incident and deleting an attachment

</td><td>

The user must to log out and log in again to access the chat.

</td><td>

1.  Select the chat icon.
2.  Select the **Check ticket and status** topic.
3.  Once the incident is displayed, select **View record**.

The incident opens.

4.  Add an attachment.
5.  Delete the attachment.

The user is redirected to home screen.

6.  Select the chat icon.

 Expected behavior: The chat should open.

 Actual behavior: The chat icon does not respond, and the user must to log out and log in again to access the chat.

</td></tr><tr><td>

Mobile iOS

 PRB1932213

</td><td>

AppAuth doesn't launch Safari when the default browser is not Safari

</td><td>

On iOS, when the device default browser is set to a non-Safari browser and SNAuthenticationBrowseriOS is set to Safari, authentication launches in the default browser, not Safari.

</td><td>

1.  Set a device's default browser to any non-Safari browser \(Chrome/Edge\).
2.  Log in to an instance.

 Expected behavior: Users are able to launch authentication in a Safari browser.

 Actual behavior: Users are launching authentication in the default non-Safari browser.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

