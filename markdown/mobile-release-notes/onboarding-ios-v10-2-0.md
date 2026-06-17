---
title: Mobile Onboarding for iOS v10.2.0
description: The iOS v10.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-ios-v10-2-0.html
release: mobile
topic_type: reference
last_updated: "2020-08-12"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v10.2.0

The iOS v10.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS \(non-classic\)

 PRB1390462

</td><td>

The click rank is not updated in the sys\_search\_event table for mobile searches

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1413429

</td><td>

Additional list items appearing in the list screen while querying remote table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1416763

</td><td>

Mobile Analytics cannot be enabled/disabled by users who have their phones set to languages other than English

</td><td>

When users have their device language set to something other than English, they are unable to enable/disable Mobile Analytics in the app in the Settings view.

</td><td>

1.  Navigate to the Settings menu, then to **General** &gt; **Language &amp; Region**.
2.  Set the iPhone language to something other than English \(for example, Spanish\).
3.  Launch the app and log in to an instance that supports Mobile Analytics.
4.  Navigate to **Settings** &gt; **Analytics**.
5.  Toggle the switch \(for example, from on to off\), then navigate back to the Settings view.
6.  Navigate back to the Analytics view and check the switch.

 Expected behavior: The switch should be in the state that is set in Step 5. In this case, it should be in the off state.

 Actual behavior: The switch reverts back to the original state. It is still on.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1418264

</td><td>

The mobile app call is not working as expected

</td><td>

The mobile app call is not working as expected. Sometimes users receive the error message 'Carrier is unavailable'. This issue is reproducible intermittently.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1418140

</td><td>

The chat does not show the text input field when users return to the on-going conversation

</td><td>

When a user initiates a chat from the mobile app and moves out of the window by clicking **Done**, the text input box does not display upon returning.

</td><td>

1.  In the instance, make sure the Agent chat plugin is active.
2.  Navigate to Applet Launchers and open the Homepage record.
3.  Activate the Chat quick action.
4.  Pick any user and log in to the mobile app to initiate a chat.
5.  Impersonate on desktop as Beth Anglin \(the VA agent\).
6.  Accept the chat as the agent.
7.  As the user, click **Done**, which takes you back to the homepage.
8.  Return to the chat.

 Notice that there is no text input field to continue the conversation.

 **Note:** This issue is also reproducible if the user backgrounds the app or locks the device and then navigates back to the app.

</td></tr></tbody>
</table>This version also contains the following updates:

-   Enabled image zoom on Activity Stream
-   Other performance improvements and minor bug fixes

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

