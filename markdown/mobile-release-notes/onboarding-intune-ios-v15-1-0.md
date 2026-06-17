---
title: ServiceNow Onboarding - Intune for iOS v15.1.0
description: The iOS v15.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v15-1-0.html
release: mobile
topic_type: reference
last_updated: "2022-11-03"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v15.1.0

The iOS v15.1.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="id_tdh_llq_fvb"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1609162

</td><td>

The agent mobile app crashes when using the 'Search' list input type on iOS 16 and above devices

</td><td>

 

</td><td>

1.  Log in to the agent app on any IOS 16 or above version devices.
2.  Choose **My work** from the navigation bar.
3.  Click the **Plus** icon on the header.
4.  Choose **Caller**.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1600723

</td><td>

Focus shifts to hidden content after navigating to the **Search** button and announces it as 'Search'

</td><td>

 

</td><td>

1.  Enable VoiceOver.
2.  Open the application in the latest iOS device.
3.  Log in with valid credentials.

The 'Applications' screen displays.

4.  Navigate to the 'EUSE Mobile' tab by using swipe gestures.
5.  Invoke it.
6.  Using swipe gestures, navigate to 'All RITMs'.
7.  Select any record from the list.
8.  Invoke it.
9.  Navigate to the top right corner's three dots\(...\) using swipe gestures.
10. Select **Edit**.
11. Select **State**.
12. Invoke it.
13. Check if the VoiceOver focus shifts to some hidden 'Search' control after the actual **Search** button visible on screen.

 Expected behavior: Focus should not shift to hidden content.

 Actual behavior: Focus shifts to hidden content after navigating to the **Search** button and announces it as 'Search'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1607261

</td><td>

Issue with document upload attachments in the chat in the Now Mobile app

</td><td>

When using an iPhone, attachments can only be downloaded and not previewed.

</td><td>

1.  Log in to any Tokyo instance in Now Mobile app, using iOS.
2.  Log in to the same instance on the desktop.
3.  Impersonate any agent \(awa\_agent role\) who can receive the live agent chat.
4.  Open Agent Workspace.
5.  Make it available.
6.  Initiate the chat from the mobile app by clicking the **+** quick action.
7.  Select the chat with the virtual agent option.
8.  Click **Show me everything**.
9.  Select **Live agent support**.

The agent should receive a chat in Agent Workspace.

10. Accept the chat.

A message displays: 'Thank you for contacting support. I am looking into your question now'.

11. There is an option to the attachment in Agent Chat in Now Mobile. Add any attachment from mobile.
12. Navigate to Agent Workspace on a desktop.
13. Refresh the page on the right side.

The 'Attachment' screen and the added attachment are reflected.

14. Try to click on the attachment.

 Expected behavior: When clicking on the attachment in the Agent Workspace, it should preview.

 Actual behavior: When clicking on the attachment in the Agent Workspace, it does not preview.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

