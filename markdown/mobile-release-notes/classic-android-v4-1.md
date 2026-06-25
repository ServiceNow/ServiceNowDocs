---
title: Mobile Classic Android v4.1
description: The Mobile Classic Android v4.1 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-android-v4-1.html
release: mobile
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic Android v4.1

The Mobile Classic Android v4.1 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.servicenow&hl=en).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mobile

 PRB1246551

</td><td>

User continues to receive notifications after they have logged out of ServiceNow mobile app

</td><td>

Users of the Android mobile app still receive push notifications when they are logged out. This issue does not occur with the iOS mobile app.

</td></tr><tr><td>

Mobile

 PRB1245039

</td><td>

Activity stream can enter an inconsistent state, with apparently duplicate items

</td><td>

Duplicate entries can get posted in the Android app's activity stream.

</td></tr><tr><td>

Mobile

 PRB1242227

</td><td>

Theme issue on native applications

</td><td>

If users use capital letters for colors on the theme page, the app defaults the color to black.

</td></tr><tr><td>

Mobile

 PRB1262210

</td><td>

Opening SIGNON instance redirects the user to the SN mobile instead of the SSO login page, which is a public UI page on the instance

</td><td>

Some users have a SIGNON instance, which provides SSO. When a user clicks on a link which has a href to the login flow, it takes the user to an SN application, where the flow is lost. The user is stuck in an attempt to log in.

 SIGNON instances with a public UI page do not need to get redirected to the mobile application for login.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

