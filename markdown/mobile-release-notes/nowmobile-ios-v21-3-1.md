---
title: Now Mobile for iOS v21.3.1
description: The iOS v21.3.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v21-3-1.html
release: mobile
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v21.3.1

The iOS v21.3.1 release provides fixes for the application.

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

 PRB1949448

</td><td>

Focus does not start at the beginning of page

</td><td>

When user selects location card, the focus does not consistently start at the top of the page.

</td><td>

1.  Navigate to **Asset tab** &gt; **Location audits** &gt; **More options** &gt; **New location audit** &gt; **Select a location**.
2.  Navigate to the list of locations and submit a location.
3.  Select a location card.
4.  Navigate back to the 'Location audits' page and select the location card again.

 Expected behavior: Focus starts at the beginning of page.

 Actual behavior: Notice that the focus start location is inconsistent.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

