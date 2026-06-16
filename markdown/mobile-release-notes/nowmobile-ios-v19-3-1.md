---
title: Now Mobile for iOS v19.3.1
description: The iOS v19.3.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v19-3-1.html
release: mobile
topic_type: reference
last_updated: "2025-03-11"
reading_time_minutes: 2
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v19.3.1

The iOS v19.3.1 release provides fixes for the application.

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

 PRB1843809

</td><td>

Messages sent by Virtual Agent are not labeled correctly

</td><td>

Admins can configure a name of their choosing for the Virtual Agent. Messages from the Virtual Agent should be sent by the configured name. Instead, they are sent by 'Virtual Agent'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1849703

</td><td>

External URLs can't be opened via push notification

</td><td>

When the user selects a push notification that contains an external URL, they observe an error instead of being navigated to the URL.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1844219

</td><td>

The Now Mobile App screen does not update when navigating multiple web screen segments

</td><td>

The Now Mobile Screen segment does not update to the user's selection when navigating between web browser screens in a record screen.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1854874

</td><td>

ItemView is rendered incorrectly if ViewGroup has a background image with an empty URL

</td><td>

When booking a desk, a selected space tile is grayed out when selected in map view.

</td><td>

1.  Log in to Now Mobile.
2.  Select **Make a reservation** &gt; **Desk booking** &gt; **Browse all**.
3.  Select a building and floor.
4.  Select a space on the map.

 Expected behavior: The tile shows details of the space selected.

 Actual behavior: Notice that the space tile is grayed out when selected.

</td></tr><tr><td>

Mobile iOS

 PRB1855927

</td><td>

Authentication errors appear upon logging in to mobile app

</td><td>

The user observes 'No Data Available' and 'Agent.AuthenticationError Error 3'.

</td><td>

1.  Log in to the app.
2.  Clear the authentication tokens in Settings to force token errors.

 Observe the authentication errors on ALPs.

</td></tr><tr><td>

Mobile iOS

 PRB1847104

</td><td>

An error appears when the user selects an external hyperlink returned by Virtual Agent \(VA\)

</td><td>

The user must navigate back from the error screen to access the chat.

</td><td>

Prerequisite: Virtual Agent is configured for the Now Mobile app and a topic that returns an external hyperlink.

 1.  Log in to the Now Mobile app
2.  Navigate to the launcher tab/screen where the bot is configured.
3.  Start a conversation with the bot.
4.  When prompted, select the option to call the topic returning hyperlink.
5.  Select the hyperlink.
6.  Return to the app.

 Expected behavior: The user lands on the Virtual Agent chat screen.

 Actual behavior: The user observes a screen with the error 'Frame load interrupted'.

</td></tr><tr><td>

Mobile iOS

 PRB1863121

</td><td>

A push notification with universal links doesn't open the destination screen

</td><td>

When a push notification with an internal link is selected, the screen is not opened.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

