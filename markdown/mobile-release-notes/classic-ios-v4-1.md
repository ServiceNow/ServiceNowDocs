---
title: Mobile Classic iOS v4.1
description: The Mobile Classic iOS v4.1 release provides problem fixes.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v4.1

The Mobile Classic iOS v4.1 release provides problem fixes.

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

 PRB714483

</td><td>

Authentications fails using SSO when the property 'glide.security.csrf.strict.validation.mode' is set to 'true'

</td><td>

When the Multi-Provider SSO and OAuth plugins are enabled, and a user attempts to authenticate with the iOS app, they receive the following error message: "Error Completing OAuth Flow - Request failed with response code: 401".

</td><td>

1.  Configure SSO with the multi-provider plugin enabled.
2.  Follow [these steps](https://support.servicenow.com/kb_view.do?sysparm_article=KB0564232) to configure SSO for the iOS app.
3.  Set the property 'glide.security.csrf.strict.validation.mode' to **true**.
4.  Attempt to authenticate via SSO IDP with the iOS app.

 Note that you receive the error message: "Error Completing OAuth Flow - Request failed with response code: 401".

</td></tr><tr><td>

Mobile

 PRB732741

</td><td>

Actionable push notifications did not show error message

</td><td>

This issue occurs when the action failed if it was due to an invalid session.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB733630

</td><td>

Scorecard target color scheme is calculated incorrectly for maximizing indicators

</td><td>

When using Performance Analytics in the iOS app, the target color scheme is not being properly applied to maximizing indicators.

</td><td>

1.  Favorite some maximizing indicators.
2.  Compare the color scheme on the platform and the iOS app.

</td></tr><tr><td>

Mobile

 PRB734880

</td><td>

Users cannot be removed when creating a new chat conversation

</td><td>

When user A creates a new chat and adds user B to the conversation, user A cannot remove user B from the chat.

</td><td>

1.  Start a new Connect conversation.
2.  Add a user by typing in their name.
3.  Attempt to remove that user.

 Expected result: You should be able to remove the user.

 Actual result: You cannot remove a user once you have selected the user.

</td></tr><tr><td>

Mobile

 PRB736838

</td><td>

Native mobile apps should support "Accept / Decline" push notification buttons

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB737193

</td><td>

The fill gradient below iOS charts is incorrect

</td><td>

This issue occurs when using Performance Analytics in the iOS app.

 By default, iOS charts apply a fill gradient to the surface area of each individual dataset between the value line and the 0-line of the x-axis. This works as expected if all values are positive, but it becomes strange if there are negative values involved. When negative values are present, the fill gradient is below the value line for the positive values and above the value line for negative values.

 Users expect the fill gradient to always fill the surface below the value line, regardless if the values are positive or negative.

</td><td>

View an indicator that has negative values.

</td></tr><tr><td>

Mobile

 PRB737651

</td><td>

Gap, gap percentage and gap color should respect direction and negative targets

</td><td>

When using Performance Analytics in the iOS app,The gap, gap percentage, and gap color should respect the indicator direction.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB738454

</td><td>

Actionable push notifications should navigate to the record/web path if the action is a foreground action

</td><td>

 

</td><td>

1.  Receive a foreground actionable push notification \(e.g. approve\_reject\_foreground\).
2.  Tap an action \(e.g.**Approve**\).

 Expected result: App should launch and navigate to the record.

 Actual result: App launches and does not navigate to the record.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](../classic-available-versions.md)

