---
title: Now Mobile for iOS v20.3.1
description: The iOS v20.3.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v20-3-1.html
release: mobile
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v20.3.1

The iOS v20.3.1 release provides fixes for the application.

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

 PRB1934663

</td><td>

IntuneMAMConfigurator doesn't execute on a build step

</td><td>

Intune 20.3.0 build is missing some Queried URL Schemes that are injected by IntuneMAMConfigurator during a build step. This can affect certain app protection policies.

</td><td>

1.  Log in to Company Portal.

Notice that portal prompts the user to install Microsoft Edge browser.

2.  Install Edge from the pop-up.
3.  Launch the Now Mobile Intune app.
4.  Accept the prompt asking to launch from Edge.
5.  Sign in with Microsoft credentials.

 Observe an error pop-up message.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

