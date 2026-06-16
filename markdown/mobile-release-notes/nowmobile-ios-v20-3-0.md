---
title: Now Mobile for iOS v20.3.0
description: The iOS v20.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v20-3-0.html
release: mobile
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v20.3.0

The iOS v20.3.0 release provides fixes for the application.

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

 PRB1925234

</td><td>

Push notifications are received after logout

</td><td>

Push notifications are received from the Agent app on an inactive/logged out session.

</td><td>

1.  Log in to an instance.
2.  Trigger a push notification.

Observe that a notification is received.

3.  Log out of the instance.
4.  Re-trigger the notification.

 Observe that the notification is still received from the iOS device.

</td></tr><tr><td>

Mobile iOS

 PRB1924641

</td><td>

The chat icon is unresponsive when the user returns to the chat after accessing an incident record and deleting an attachment

</td><td>

The user must to log out and log back in to access the chat.

</td><td>

1.  Select the chat icon.
2.  Select the 'Check ticket and status' topic.
3.  Once the incident is displayed, select **View record**.

The incident opens.

4.  Add an attachment.
5.  Delete the attachment.

The user is redirected to home screen.

6.  Select the chat icon.

 Expected behavior: The chat should open.

 Actual behavior: The chat icon does not work, and the user must to log out and log back in to access the chat.

</td></tr><tr><td>

Mobile iOS

 PRB1929399

</td><td>

Web session timeout causes an infinite loop

</td><td>

When the user is logged out, they are redirected to the portal login page which refreshes in an infinite loop.

</td><td>

1.  Select the **Menu** button on the top right.
2.  Select **Log out**.

 Expected behavior: The system maintains the current session.

 Actual behavior: The user is redirected to a portal login page that is refreshing indefinitely. The application is unusable until it is ended and relaunched.

</td></tr><tr><td>

Mobile iOS

 PRB1917575

</td><td>

Overlapping cards in the record section of ALP

</td><td>

When a record section is configured on a launcher page, cards appear to be overlapping.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

