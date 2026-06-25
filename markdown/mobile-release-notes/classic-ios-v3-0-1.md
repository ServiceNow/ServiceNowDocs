---
title: Mobile Classic iOS v3.0.1
description: The Mobile Classic iOS v3.0.1 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-ios-v3-0-1.html
release: mobile
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v3.0.1

The Mobile Classic iOS v3.0.1 release provides problem fixes.

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

 PRB681533

</td><td>

Better error messaging required when the SSO IDP is unreachable

</td><td>

iOS error messages do not appear when the SSO IDP is unreachable.

</td><td>

1.  Attempt to log in to an instance with an invalid SSO IDP entry.
2.  Note the app shows infinite loading spinner during log in.

The app should show an error message when the IDP fails to load.

</td></tr><tr><td>

Mobile

 PRB681541

</td><td>

"No Network" indicator in iOS app can sometimes incorrectly be repeated multiple times

</td><td>

 

</td><td>

1.  Turn on airplane mode.
2.  Rotate the device into landscape view.
3.  Rotate the device back into portrait view.

Note the "No Network Connection" message is displayed twice instead of once.

</td></tr><tr><td>

Mobile

 PRB681126

</td><td>

Presence needs to be fixed in the iOS app after the presence API was changed on the server

</td><td>

How presence works on the server has changed recently. The presence API contract changed, and the iOS app needs to be updated to work with the new presence API.

</td><td>

The following is one of many ways to reproduce this problem. 1.  Log in as a user on the desktop.
2.  Log in as a different user on the app.
3.  Navigate to an incident form.
4.  Click on the magnifying glass.
5.  Search for the user logged onto the desktop.

Note there is no green system presence icon, even though online users should have a green presence dot on their avatar.

</td></tr><tr><td>

Mobile

 PRB681273

</td><td>

When logging in to iPhone mobile app, using local login prompts the user to provide SSO credentials

</td><td>

 

</td><td>

1.  Set the system property glide.authentication.external.disable\_local\_login to **false**.
2.  Enable Multi-SSO provider.
3.  Access the instance from the iPhone mobile application.
4.  Use local login \(i.e. log in as a local user\).
5.  Select **Continue**.

It redirects to the SSO login page, prompting the user to provide SSO credentials.

</td></tr><tr><td>

Mobile

 PRB681209

</td><td>

Whitespace or newlines in primary IDP property can cause SSO to fail to load

</td><td>

 

</td><td>

1.  On the instance, set the glide.authenticate.sso.redirect.idp system property to a value with some extra whitespace at the end.
2.  In the app, attempt to log in to the instance.

 Actual behavior: The user gets an infinite spinner as the instance attempts to load the IDP.

 Expected behavior: The app should strip out the extra whitespace.

</td></tr><tr><td>

Mobile

 PRB681693

</td><td>

Native App count widget will show infinite spinner if count fails to load

</td><td>

If the request to get the count of records fails, the count favorite widget shows a loading spinner indefinitely.

</td><td>

1.  Create a favorite for a list.
2.  Enable the count visualization for that favorite.
3.  Somehow fail the HTTP request to**/api/now/v1/stats**.

 Actual behavior: The user gets an infinite spinner on the count widget.

 Expected behavior: The count widget should show an ellipses in place of the number upon failure.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

