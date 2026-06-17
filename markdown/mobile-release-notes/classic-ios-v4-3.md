---
title: Mobile Classic iOS v4.3
description: The Mobile Classic iOS v4.3 release provides problem fixes.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v4.3

The Mobile Classic iOS v4.3 release provides problem fixes.

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

 PRB802370

</td><td>

HTML in journal fields displays tags on native apps

</td><td>

When HTML code blocks are used in activity stream journal fields, the native applications do not render the HTML. Instead, the HTML tags are displayed as inline text.

</td><td>

1.  Create an HTML code block within an activity stream.
2.  View that activity stream from the native mobile applications.

 Expected result: The HTML tags are stripped from the text block, leaving only "human readable" text.

 Actual result: The HTML tags are displayed inline.

</td></tr><tr><td>

Mobile

 PRB828571

</td><td>

iOS app can crash intermittently

</td><td>

The app crashes when it attempts to get cookies for an invalid instance or instance URL.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB831289

</td><td>

During SSO flow, iOS app needs to handle auth\_redirect.do in the same manner as logout\_redirect.do

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB877202

</td><td>

iOS app should support links with a new target window during SSO flow

</td><td>

The iOS app does not support new windows during the SSO flow. The \`target="\_blank"\` HTML attribute requests that the link is opened in a new window.

 For example: &lt;a href="https://my-idp.com" target="\_blank"&gt;My Link&lt;/a&gt;

 The iOS app does not open the window or navigate to the URL.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](../classic-available-versions.md)

