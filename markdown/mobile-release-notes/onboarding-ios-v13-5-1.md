---
title: Mobile Onboarding for iOS v13.5.1
description: The iOS v13.5.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-ios-v13-5-1.html
release: mobile
topic_type: reference
last_updated: "2022-03-18"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v13.5.1

The iOS v13.5.1 release provides fixes for the application.

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

 PRB1560126

</td><td>

The form screen menu shows no actions for certain user roles

</td><td>

The action sheet is created with a **Cancel** action, but due to the 'externalAttachmentAccess' flag being set to false, no further actions are added to the menu.

</td><td>

1.  Log in to the instance.
2.  Navigate to **My work** &gt; **My tasks** and open any WOT.
3.  Click the top menu function.

Notice that the other functions are missing.

4.  Remove the 'sn\_customerservice.customer' role \(this has the snc\_external role\) from the above user.
5.  Log in to the app again.
6.  Test using the above steps.

 Notice that the functions are visible.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

