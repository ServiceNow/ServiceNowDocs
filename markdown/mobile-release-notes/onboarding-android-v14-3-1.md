---
title: Mobile Onboarding for Android v14.3.1
description: The Android v14.3.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v14-3-1.html
release: mobile
topic_type: reference
last_updated: "2022-07-15"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v14.3.1

The Android v14.3.1 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android \(non-classic\)

 PRB1590126

 [KB1123524](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123524)

</td><td>

Some Android users cannot log in and experience an infinite loading spinner

</td><td>

Affected users will have experienced a database migration that added the forceSsoId column with a null value. The issue is observed when those users upgrade to versions where the Android code does not handle those null values properly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1590171

</td><td>

The app crashes when adding an instance for some Android users

</td><td>

After being unable to access their previously-added instance, if the user tries to add the same URL as a new instance, the app crashes.

</td><td>

1.  Install an app and add an instance.
2.  Verify that it appears on the instance list screen.
3.  Upgrade the app.
4.  Select an instance and observe an infinite spinner.
5.  Select the **+** button.
6.  Add same instance that you added in step 1 and select **Save** and log in.

 Expected behavior: The app works as expected.

 Actual behavior: The app crashes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

