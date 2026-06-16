---
title: Now Mobile for iOS v21.0.1
description: The iOS v21.0.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v21-0-1.html
release: mobile
topic_type: reference
last_updated: "2026-02-11"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v21.0.1

The iOS v21.0.1 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

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

iOS Mobile

 PRB1974402

</td><td>

Scale question text is truncated when completing a survey for an HR task on mobile

</td><td>

When the user completes an Employee Form for an HR Task on mobile, the question text is truncated.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1985699

</td><td>

SVG images are not rendered on an image choice list

</td><td>

When the user configures IFS with an image choice list and uses SVG images, the images are not rendered correctly.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1985918

</td><td>

Support a new mobile property 'disableAppFeedbackPrompt'

</td><td>

When the user opens the mobile app and navigates to **Settings**, they notice a **Give feedback** cell that, when tapped, navigates the user to the app store to write a review. The **Give feedback** cell should be configurable so that users can hide it.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1986985

</td><td>

Update the **Give Feedback** text in Settings

</td><td>

**Give Feedback** is updated to **App Feedback** and **Legal** is updated to **App Legal &amp; Privacy**.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1973764

</td><td>

Single/Multi Reference list value are not displayed after selecting **Resolve**

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1990054

</td><td>

Uploaded images from MESP via Cabrillo are changed from .jpeg to .jpg file extensions

</td><td>

This behavior may not be expected, as admins should have the option to not show the **Gallery** option.

</td><td>

1.  Log in to Now Mobile.
2.  Navigate to **Home** &gt; **Access People Services** &gt; **My Workplace** &gt; **Name Card Request** &gt; **Name Cards**.
3.  Scroll down to **Attachment** &gt; **Upload** &gt; **Gallery**.
4.  Upload a file of type .jpeg with less than 1mb.

 Notice that Android OS Gallery chooses the file with the extension '.jpg'.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

