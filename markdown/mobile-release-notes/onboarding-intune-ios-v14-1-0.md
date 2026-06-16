---
title: ServiceNow Onboarding - Intune for iOS v14.1.0
description: The iOS v14.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v14-1-0.html
release: mobile
topic_type: reference
last_updated: "2022-04-26"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v14.1.0

The iOS v14.1.0 release provides fixes for the application.

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

 PRB1560033

</td><td>

When scrolling through a long filter list for a reference field, the pagination breaks and restarts at the beginning of the list

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1562934

</td><td>

In iOS Mobile Agent, the confirmation message while clearing a filter from a list is different from Android

</td><td>

The confirmation message is translated incorrectly.

</td><td>

1.  Log in as an admin user.
2.  Change the OS language to Japanese.
3.  Log in the Agent mobile app as a user with breached incidents.
4.  Open the breached incident list.
5.  Use the filter to limit to Priority = critical.
6.  Confirm the message when clearing the above filter.

 Expected behavior: 'Yes' should be translated to 'はい'.

 Actual behavior: In iOS, it is translated incorrectly.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

