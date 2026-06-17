---
title: Mobile Agent - Intune for iOS v17.5.0
description: The iOS v17.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-intune-ios-v17-5-0.html
release: mobile
topic_type: reference
last_updated: "2024-05-09"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for iOS v17.5.0

The iOS v17.5.0 release provides fixes for the application.

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

 PRB1733952

</td><td>

Content publishing mobile banners disappear or don't load in Now Mobile

</td><td>

The contents of the content publishing campaign section disappear as the user scrolls through them. This occurs when there is an empty record section above the campaign section that is hidden when empty.

</td><td>

1.  Set up an ALP with a campaign section that has more than one record \(for example, more than one banner image\).
2.  Add a record section above the campaign section that is hidden when empty and ensure that there are no records in this section.

 Expected Behavior: The images load properly on the carousel.

 Actual behavior: The images don't load or disappear when swiping through the carousel. They only appear when the user starts scrolling down.

</td></tr><tr><td>

Mobile iOS

 PRB1743247

</td><td>

The user cannot select between paged carousel images with Voice Over in Now Mobile

</td><td>

Swiping on the page doesn't do anything.

</td><td>

1.  Provision an instance with Voice Over enabled.
2.  Navigate to **More** &gt; **Campaigns**.
3.  Using VoiceOver, focus on the paging component.

Notice that Voice Over says 'Page 1 of X, adjustable, Swipe up or down with one finger to adjust the value'.

4.  While focused on the component, swipe up or down with one finger.

 Expected behavior: Swiping up or down changes to the previous or next image in the carousel.

 Actual behavior: The current image in the carousel is not changed.

</td></tr><tr><td>

Mobile iOS

 PRB1756605

</td><td>

'My Task Map' crashes the Mobile Agent app on iPad

</td><td>

Crashing only occurs on certain map locations, yet when the location is updated it does not fix the issue in all instances.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1743865

</td><td>

Extra sessions are created for unreadMessage transactions

</td><td>

After enabling the **Chat** quick action in the Now Mobile app, requests are sent to /api/now/v1/cs/ consumerAccount /unreadMessage. These occur when the user is navigating around the app \(for example, refreshing the screen, switching tabs, etc.\). These transactions create new sessions.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1749472

</td><td>

Barcode scanning doesn't focus on the crosshair

</td><td>

Because the scanning area isn't well-defined, it's difficult to catch a specific barcode when there are multiple barcodes caught in the frame.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-intune-available-versions.md)

