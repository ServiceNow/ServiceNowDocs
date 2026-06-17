---
title: Now Mobile for BlackBerry for iOS v20.5.0
description: The iOS v20.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-blackberry-ios-v20-5-0.html
release: mobile
topic_type: reference
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for iOS v20.5.0

The iOS v20.5.0 release provides fixes for the application.

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

 PRB1938771

</td><td>

The Data Visualization Single score on the Mobile app shows 'Content couldn't be displayed' after iOS 26 upgrade

</td><td>

The user observes this error on a Now Mobile app base instance after upgrading to iOS 26.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1936392

</td><td>

The user is unable to use push actions due to an APIError \(NowAPIError - 6\).

</td><td>

The user observes a 'Agent.NowAPIError Error 6' message when accepting WOT on the Field Service Management \(FSM\) Mobile app from a push action notification.

</td><td>

1.  Impersonate an FSM Agent on the iOS Agent Mobile App.
2.  On desktop, assign a Pending Dispatch Work Order Task to an agent.
3.  When the assignment push notification arrives on mobile, long-select the Push notification and select **Accept**.

 Notice that an error is displayed: 'Agent.NowAPIError error 6'.

</td></tr><tr><td>

Mobile iOS

 PRB1943946

</td><td>

The ServerCallBridge execute function causers a crash when non-JSON serializable values are present in the payload

</td><td>

The Now Mobile App crashes when enabling the Mobile UI Rule script that calls the script include.

</td><td>

Navigate to **Reserve a Workspace \(on quick links\)** &gt; **HQ Workstation** &gt; **Browse all** &gt; **Select a Date**.

 Observe that the app crashes as soon as the user selects a date.

</td></tr><tr><td>

Mobile iOS

 PRB1938562

</td><td>

Opening an external link via an actionable push notification doesn't work

</td><td>

When the user selects the notification, the app opens but no redirect occurs.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-blackberry-available-versions.md)

