---
title: Mobile Onboarding for Android v14.5.0
description: The Android v14.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v14-5-0.html
release: mobile
topic_type: reference
last_updated: "2022-09-01"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v14.5.0

The Android v14.5.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android \(non-classic\)

 PRB1585986

</td><td>

Text label is not fully visible on Now Mobile App

</td><td>

Users observe that text in a pop-up window is truncated.

</td><td>

1.  Log in to an instance using the Now Mobile app.
2.  Ensure you have created an incident.
3.  Click **My Requests** to be directed to the 'My Request' list view.
4.  Click the record to open it.
5.  Click the 3 dots in the top-right of the screen.
6.  In the footer, click **Escalate a Request**.

 The text in the pop-up window is cut off.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1591393

</td><td>

'Uploading attachments' loading screen does not close

</td><td>

When a user adds an attachment to a record, they get stuck on the 'Uploading attachments' loading screen.

</td><td>

1.  Create an input form screen with inputs.
2.  Create an action item associated with the input form screen.
3.  Create a function using the above action item.
4.  Add the function on the quick action and list top menu.
5.  Create an incident.
6.  Complete the form.
7.  Add an attachment and click **Submit**.

 Observe that the 'Uploading attachments' loading screen never closes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

