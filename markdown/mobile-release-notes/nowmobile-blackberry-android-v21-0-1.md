---
title: Now Mobile for BlackBerry for Android v21.0.1
description: The Android v21.0.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-blackberry-android-v21-0-1.html
release: mobile
topic_type: reference
last_updated: "2026-02-11"
reading_time_minutes: 2
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for Android v21.0.1

The Android v21.0.1 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.fulfiller). Users can launch a demo to try the ServiceNow Agent app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Android Mobile

 PRB1985917

</td><td>

Support a new mobile property 'disableAppFeedbackPrompt'

</td><td>

When the user opens the mobile app and navigates to 'Settings', they notice a **Give feedback** cell that, when tapped, navigates the user to the app store to write a review. The **Give feedback** cell should be configurable so that users can hide it.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1986986

</td><td>

Update the **Give Feedback** text in Settings

</td><td>

**Give Feedback** is updated to **App Feedback** and **Legal** is updated to **App Legal &amp; Privacy**.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1986201

</td><td>

Question text is truncated when completing a survey for an HR task on mobile

</td><td>

When the user completes an Employee Form for an HR Task on mobile, the question text is truncated.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1990055

</td><td>

Uploaded images from MESP via Cabrillo change .jpeg file extensions to .jpg

</td><td>

This behavior may not be expected, as admins should have the option to not show the Gallery option.

</td><td>

1.  Log in to Now Mobile.
2.  Navigate to **Home** &gt; **Access People Services** &gt; **My Workplace** &gt; **Name Card Request** &gt; **Name Cards**.
3.  Scroll down to **Attachment** &gt; **Upload** &gt; **Gallery**.
4.  Upload a file of type .jpeg with less than 1mb.

 Notice that Android OS Gallery chooses the file with the extension '.jpg'.

</td></tr><tr><td>

Android Mobile

 PRB1986342

</td><td>

The **Next** button on the Input Form Screen freezes when the previous page is a duplicate

</td><td>

This defect occurs when an input form screen has at least three pages, with two of those pages being duplicate pages \(for example, two pages with identical IDs within the same input form screen\).

</td><td>

1.  Configure an Input Form Screen with duplicate pages \(for example, configure 4 pages, with pages 2 and 3 as the duplicate pages.\)
2.  Launch the Input Form Screen.
3.  While filling out any mandatory inputs, select the **Next** button until the second duplicate page is reached.
4.  Select **Next** on the duplicate page.

 Expected Behavior: An input form screen should proceed through all pages in the input form screen.

 Actual behavior: Navigation freezes on the second duplicate page.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-blackberry-available-versions.md)

