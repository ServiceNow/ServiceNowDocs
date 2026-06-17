---
title: Now Support for iOS v21.2.0
description: The iOS v21.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowsupport-ios-v21-2-0.html
release: mobile
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for iOS v21.2.0

The iOS v21.2.0 release provides fixes for the application.

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

 PRB1992112

</td><td>

Catalog icons are not displayed when the short description is long

</td><td>

Catalog icons should be visible.

</td><td>

Pre-requisite: Service Catalog for mobile plugin is installed.

 1.  Open the Agent Mobile app.
2.  Select **Services**.
3.  Select any option from **Browse services**.

 Observe that Catalog icons are not displayed when the short description is long.

</td></tr><tr><td>

iOS Mobile

 PRB1993860

</td><td>

Catalog items without icons don't align with catalog items that have them

</td><td>

Now Mobile users experience an issue in 'Workplace Safety Services' where catalog items without icons do not align with the catalog items that do.

</td><td>

1.  Log in to an instance via Now Mobile.
2.  On the Home launcher tab, scroll down to 'Workplace Safety Services'.
3.  Select **See all**.

 Notice that the catalog items without an icon do not align with the catalog items that do have icons.

</td></tr><tr><td>

iOS Mobile

 PRB1954340

</td><td>

The user observes 'Error 153 Video player configuration error' when opening a Campaign

</td><td>

When the user opens a 'Campaign' with a YouTube video embedded, they observe an error.

</td><td>

Pre-condition: Install fresh clean app. 1.  Open mobile \(requester\) app and log in to an instance.
2.  Select **More** &gt; **Campaigns**.

Expected behavior: The video displays the play button and background image.

Actual behavior: There is error Error 153 Video player configuration error.

</td></tr><tr><td>

iOS Mobile

 PRB2002217

</td><td>

The 'Start travel' and 'Start work' footer actions don't work properly

</td><td>

The buttons are not functional.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2001299

</td><td>

The error 'Agent.NowAPIError' appears intermittently

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2000187

</td><td>

The Quick Action Function instance not visible on the launcher screen

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1976084

</td><td>

The date type value is displayed incorrectly on the Input Form screen

</td><td>

Date type value is displayed as yyyy-mm-dd HH:MM:SS on the Input Form screen in iOS. It should be displayed as yyyy-mm-dd.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

