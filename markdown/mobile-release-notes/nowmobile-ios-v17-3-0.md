---
title: Now Mobile for iOS v17.3.0
description: The iOS v17.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v17-3-0.html
release: mobile
topic_type: reference
last_updated: "2024-03-07"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v17.3.0

The iOS v17.3.0 release provides fixes for the application.

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

 PRB1732702

</td><td>

Intermittent crashing when the user repeatedly taps an action

</td><td>

When a user approves multiple tasks one at a time using a configured **Approve** footer button, the first approval goes through, but the app crashes on a subsequent approval.

</td><td>

1.  Log in to the Now Mobile app.
2.  In the Home tab, scroll down to 'My tasks'.
3.  Open one of the tasks and tap **Approve**.
4.  Repeat step 3 on four to five tasks.

 Observe that the app crashes.

</td></tr><tr><td>

Mobile iOS

 PRB1726294

</td><td>

The Mobile UI does not apply when refreshing the form screen

</td><td>

 

</td><td>

1.  Log in to Agent Mobile.
2.  Navigate to the 'Outages' launcher.
3.  Open any entry in the list and note the number of fields.
4.  Refresh the screen.

 Observe that more fields appear after refreshing the screen.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

