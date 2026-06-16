---
title: Mobile Onboarding for iOS v15.0.0
description: The iOS v15.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-ios-v15-0-0.html
release: mobile
topic_type: reference
last_updated: "2022-10-06"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v15.0.0

The iOS v15.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS \(non-classic\)

 PRB1599956

</td><td>

Fatal Exception: NSInternalConsistencyException and completion handler not called

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1597559

</td><td>

VoiceOver does not announce that a page is loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1596366

</td><td>

Mobile VA chat request returns 401 error when the authorizeByCookieFirst is set to true

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1595736

</td><td>

UI rules are not applied on the Form screen of the global mobile results

</td><td>

 

</td><td>

1.  Create a Mobile UI Rule where the Incident Priority is highlighted in yellow, if priority is 3.
2.  Open an incident record where priority is 3 and confirm that the priority is highlighted.
3.  Search for the same incident record in the Global Search.
4.  Open the incident record.

 Expected result: The priority is highlighted.

 Actual result: The priority is not highlighted.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1594204

</td><td>

My Requests Stage Status Timeline text does not display properly when the font size is increased to the Large Font setting

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1592476

</td><td>

When doing a search while impersonating a user, the top search results are obstructed by the impersonation banner

</td><td>

This affects iOS Mobile in Mobile Agent app.

</td><td>

1.  Go to Agent Mobile app \(IOS mobile\).
2.  Impersonate a user.
3.  In the search field at the top, search for any text.
4.  The first search results will overlap with the impersonation banner.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1566950

</td><td>

Accessibility issues with VoiceOver on native iOS screens

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1599903

</td><td>

Push execution in the NotificationListScreen is unnecessarily delayed by the analytics API call

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1606689

</td><td>

Custom deep link URL is not opening from the NOW mobile app on iOS \(webview\)

</td><td>

 

</td><td>

1.  Install the RouteMatic application from the app store.
2.  Configure the web page containing a hyperlink with rmapp://employee.
3.  Click on the link from the app.

 Expected behavior: The app should redirect to the RouteMatic application.

 Actual behavior: App remains idle.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

