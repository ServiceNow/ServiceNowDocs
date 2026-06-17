---
title: ServiceNow Onboarding - Intune for iOS v14.3.0
description: The iOS v14.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v14-3-0.html
release: mobile
topic_type: reference
last_updated: "2022-07-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v14.3.0

The iOS v14.3.0 release provides fixes for the application.

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

 PRB1583673

</td><td>

On iOS 15, a UI rule doesn't work as expected

</td><td>

When the user edits a field, the 'Mandatory' disclaimer next to the field takes longer than expected to appear or disappear.

</td><td>

1.  Navigate to **My work** &gt; **My incidents** on a device running iOS 15.
2.  Click any open incident and then click **Resolve**.

An input form screen opens.

3.  Populate the **There was an outage** field and set it to 'Yes'.

 Notice that the outage start/end fields do not display the 'Mandatory' disclaimer.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1560091

</td><td>

The Intune instance nickname field is not populated

</td><td>

Normally, a preconfigured instance contains pre-populated default URL and nickname fields. In iOS, only the URL field is populated.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1557743

</td><td>

Geolocation tracking settings on the Agent Mobile app are reset after each logout/login

</td><td>

If the user logs out and logs back in after Geolocation tracking is set, the tracking time is reset to eight hours by default.

</td><td>

1.  Log in to the Agent Mobile App on iOS.
2.  Navigate to **Settings** &gt; **Location tracking**.
3.  Enable Location Tracking and set the **Track For** field to 23 hours.
4.  Navigate back to the Settings page and confirm that Location tracking is set to 23 hours.
5.  Log out of the mobile app and then log back in.

 Expected behavior: The location setting of 23 hours is retained.

 Actual behavior: The location setting is reset to 8 hrs.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1573468

 [KB1117239](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117239)

</td><td>

Impersonation does not work when the session token is unavailable

</td><td>

The instance resets the Glide user session cookie and kicks the user to the logged in user.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

