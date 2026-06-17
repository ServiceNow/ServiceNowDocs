---
title: Mobile Agent for iOS v20.6.0
description: The iOS v20.6.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v20.6.0

The iOS v20.6.0 release provides fixes for the application.

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

iOS Mobile

 PRB1952341

</td><td>

Attachments uploaded in offline mode are not visible once back online

</td><td>

Attachments uploaded in offline mode are not visible once back online.

</td><td>

1.  Make sure offline functionality is enabled on the instance.
2.  Navigate to **Offline mode**
3.  Open a record with an activity.
4.  Attach an image via the camera.
5.  Set the app to 'Online'.

 Observe that the attached images are not visible.

</td></tr><tr><td>

iOS Mobile

 PRB1955492

</td><td>

Smart Assessment questionnaire responses in a question are not retained when navigated back on iPad

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1946347

</td><td>

A smart button of type 'Email' does not use the default email app to open on iOS devices.

</td><td>

The iCloud email app is opened instead of the user-selected default app.

</td><td>

1.  Create a

sys\_sg\_button

of type 'Email'.

2.  Link it to a button instance.
3.  Set the default email app on the iOS device by navigating to **Settings** &gt; **Default Apps** &gt; **Email** and set to Gmail or Outlook.

 Notice that when used from an iOS device, it uses the iCloud email app rather than the default app.

</td></tr><tr><td>

iOS Mobile

 PRB1956594

</td><td>

Step loader gets displayed after a synthesized response

</td><td>

 

</td><td>

1.  Ask 'I need a new laptop'.
2.  Note the first step loader and synthesized response.

 Expected behavior: A step loader reading 'Generating a response' appears before a synthesized response.

 Actual behavior: Both controls are displayed at about the same time and the step loader comes after the synthesized response.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

