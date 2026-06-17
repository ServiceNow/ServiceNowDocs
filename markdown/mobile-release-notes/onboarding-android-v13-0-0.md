---
title: Mobile Onboarding for Android v13.0.0
description: The Android v13.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-android-v13-0-0.html
release: mobile
topic_type: reference
last_updated: "2021-10-14"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v13.0.0

The Android v13.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.requestor). Users can launch a demo to try the Now Mobile app. You can use a demo account from the initial post-download screen or the instance list screen.

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

 PRB1498491

</td><td>

The video **Play** button is not consistent in the Now Mobile video campaign

</td><td>

The Vimeo video **Play** button is not visible from the Now Mobile app when creating it as mobile video content. This makes it difficult to identify the content as video content.

</td><td>

1.  Install the Content Automation plugin.
2.  Navigate to mobile content.
3.  Create mobile content and complete the form as follows:
    -   Title: Your title
    -   Content type: Mobile video
4.  In the **Video link** field, add a new video link as follows:
    -   Name: Vimeo
    -   Type: Video
    -   URL: &lt;enter a Vimeo URL&gt;
5.  Save the mobile content record.
6.  Navigate to **Now Mobile app** &gt; **Applet Launchers** &gt; **Homepage** &gt; **Body**.
7.  In the mobile content section, make sure that the added video content will be displayed by checking that the filter condition has no restrictions.
8.  Log in for the Now Mobile app and navigate to 'For Me'.

 Notice that the content video is added, but with no **Play** button. You have to tap the image section to see that it is a video.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

