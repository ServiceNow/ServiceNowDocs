---
title: Mobile Classic iOS v3.0.2
description: The Mobile Classic iOS v3.0.2 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-ios-v3-0-2.html
release: mobile
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v3.0.2

The Mobile Classic iOS v3.0.2 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Apple App Store](https://itunes.apple.com/us/app/servicenow/id1044428492?mt=8).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB690540

</td><td>

Using iOS 9.3 or newer and SSO throws a -999 error

</td><td>

Attempting to connect to a ServiceNow instance configured to use SSO with an iOS device with OS 9.3.2 or newer results in a "NSURLErrorDomain error -999" error.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB690863

</td><td>

SSO sign in fails if the IDP redirects to a non-root path

</td><td>

If an IDP redirects the instance back to a non-root path \(e.g. instance.service-now.com/ESS\), then the SSO-OAuth handshake silently fails.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB690967

</td><td>

Native map markers should be consistent with mobile web

</td><td>

Map marker labels are not positioned correctly in the native app and do not automatically reload correctly when the map is zoomed.

</td><td>

1.  View a map with custom labels markers that have a custom label offset.
2.  Ensure the map supports live reloading when zooming.
3.  Zoom around on the map.

 Expected result: Markers should live-reload when zooming. Custom marker labels should be correctly positioned.

 Actual result: Markers do not reload in the native app. Marker labels are positioned with inverted label offsets compared to the mobile web experience.

</td></tr><tr><td>

Mobile

 PRB691868

</td><td>

In the iOS app, the backward slash \( \\ \) is not shown in the keyboard for the username field, unlike password

</td><td>

 

</td><td>

In the iOS app: 1.  Type something in the username field.
2.  Note that the user needs to hold the forward slash \( / \) to enter a backward slash \( \\ \).

This is inconvenient for customers who use ' \\ ' in their user names.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

