---
title: Now Mobile - Intune for iOS v22.3.1
description: The iOS v22.3.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-ios-v22-3-1.html
release: mobile
topic_type: reference
last_updated: "2026-11-09"
reading_time_minutes: 2
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v22.3.1

The iOS v22.3.1 release provides fixes for the application.

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

 PRB2133986

</td><td>

The 'Notifications' tab doesn't show the unread badge count on iPad with iPadOS 26, though it's shown on iPhone

</td><td>

On iPadOS 26 at regular width, the native tab bar appears at the top of the screen and doesn't show the unread badge on the 'Notifications' tab. The same account on iPhone shows the badge \(for example, '4'\). This issue occurs in version 22.0.0 and later.

</td><td>

1.  Log in to a fulfiller environment that uses the native tab bar \(not AIUX\) as a user with unread notifications.
2.  On an iPad running iPadOS 26 in full screen, observe the tab bar at the top of the screen.
3.  Compare with an iPhone running iOS 26.

Expected behavior: The 'Notifications' tab shows the unread count on both devices.

Actual behavior: The iPhone shows the count, and the iPad shows nothing.

</td></tr><tr><td>

Mobile iOS

 PRB2126902

</td><td>

A deep link in a push notification banner is ignored when the app is launched from a closed state, and the app stays on the home screen

</td><td>

When the mobile app on iOS is closed and then launched by tapping a push notification banner that contains a deep link \(for example, a link to a knowledge base \(KB\) article\), the app opens on the home screen and never navigates to the target screen. This issue affects version 22.2.0 and doesn’t occur in version 22.0.1. Any deep link that opens a screen from the home tab \(for example, a record form\) is likely affected too.

</td><td>

1.  Install version 22.2.0 of the app and log in to an instance whose home tab is a web view.
2.  Force-quit the app.
3.  Send a push notification whose link is a /mobileapplink URL for a knowledge base \(KB\) article.
4.  Tap the notification banner.

Observe that the app opens on the home screen and doesn't navigate to the KB article.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

