---
title: Now Mobile for iOS v18.4.0
description: The iOS v18.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v18-4-0.html
release: mobile
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v18.4.0

The iOS v18.4.0 release provides fixes for the application.

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

 PRB1813989

</td><td>

After upgrading Mobile Agent on iPad, scan functionality doesn't work for barcodes/QR codes

</td><td>

When scanning a barcode on an iPad with version 18.3 of Mobile Agent, the barcode or QR code isn't detected. The user observes a message such as 'Find Nearby Barcodes' or 'Slow down' even if the device is held steady and centered.

</td><td>

Pre-requisite: Asset management for Mobile is installed.

 1.  Log in to an instance with an iPad.
2.  Navigate to **Asset** &gt; **Asset Lookup**.
3.  Use an existing barcode/QR code, or generate one with an online generator.
4.  Attempt to scan.

 Observe that the device will not scan, and notice messages such as 'Find Nearby Barcodes' or 'Slow down'.

</td></tr><tr><td>

Mobile iOS

 PRB1785371

</td><td>

SVG images do not render in the Now Mobile app

</td><td>

The Now Mobile app is unable to display SVG images in the 'Popular topics' section within the Help Center Launcher screen.

</td><td>

1.  Upgrade the iOS Now Mobile app to v18.0.1.
2.  On Now Mobile, navigate to **Help Center** &gt; **Popular Topics**.
3.  In the platform desktop version, replace some of the Popular Topics icons with SVG icons.
4.  After replacing the topics with SVG icons, refresh the Help Center Launcher screen.

 Notice that the SVG icons do not render.

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

 PRB1804331

</td><td>

A 'No data available' error appears on iOS devices

</td><td>

The user observes the message, 'No data available please pull down to refresh' on app launch.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

