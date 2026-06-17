---
title: Now Mobile for iOS v18.2.0
description: The iOS v18.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-09-10"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v18.2.0

The iOS v18.2.0 release provides fixes for the application.

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

 PRB1780274

</td><td>

The barcode scanner intermittently fails to scan QR codes

</td><td>

Barcode scanner is not working intermittently on iOS.

</td><td>

1.  Log in to the Agent app.
2.  From **More**, select **Asset**.
3.  Select Asset Lookup.
4.  Scan a QR code.

 Expected behavior: The code is scanned and the details are shown on the app.

 Actual behavior: Nothing happens as the code doesn't get scanned.

</td></tr><tr><td>

Mobile iOS

 PRB1784226

</td><td>

Users in are reported as 'Anonymous' in the User Experience Analytics dashboard instead of appearing with a hashed user ID

</td><td>

When the user performs an activity in the app, they are reported as 'Anonymous' in the hashed user ID column in the User Experience Analytics dashboard.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1779258

</td><td>

The user is unable to hide the hamburger button \(three dots\) on the top right corner of the chat window

</td><td>

There is no provision to hide the hamburger button available on the top right corner of chat window and the user is unable to hide the empty choice.

</td><td>

1.  Open Virtual Agent.
2.  Observe whether the hamburger button \(three dots\) is there.

 Expected behavior: The button is not visible.

 Actual behavior: The button is visible, and when tapped, a message displays that says 'No support options available'.

</td></tr><tr><td>

Mobile iOS

 PRB1788898

</td><td>

The app crashes when previewing a photo uploaded for an attachment variable in Record Producer

</td><td>

The app crashes when the user takes and uploads a photo in Record Producer, then clicks the link to preview it.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1763948

</td><td>

The Asset lookup card doesn't display the background color for Asset Tags

</td><td>

Blue highlighted text is not visible.

</td><td>

1.  Open an Agent Mobile base instance.
2.  Navigate to the Asset tab.
3.  Select Asset lookup.
4.  Type something in.
5.  Submit.

 Expected behavior: Blue color highlighted text should be visible.

 Actual behavior: The blue text color is not visible.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](../now-mobile-available-versions.md)

