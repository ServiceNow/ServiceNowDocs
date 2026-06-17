---
title: Mobile Agent - BlackBerry for Android v20.2.0
description: The Android v20.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-blackberry-android-v20-2-0.html
release: mobile
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for Android v20.2.0

The Android v20.2.0 release provides fixes for the application.

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

 PRB1913393

</td><td>

Activity stream doesn't update after adding a comment in low memory conditions

</td><td>

 

</td><td>

1.  Navigate to developer options and set "Don't keep activities" to simulate battery performance mode and memory pressure.
2.  Open the Agent app.
3.  Open any WOT.
4.  Navigate to the Activity Stream.
5.  Add a comment.

 Expected Behavior: The comment is added successfully.

 Actual Behavior: A white screen is displayed.

</td></tr><tr><td>

Android Mobile

 PRB1906767

</td><td>

After closing a task, the screen doesn't navigate to a newly created follow-up task

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1894874

</td><td>

A photo taken in landscape mode is transformed to portrait when uploaded

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1901109

</td><td>

Attachment upload from web view doesn't work

</td><td>

Images fail to upload.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1909110

</td><td>

Input form screen new choice UI doesn't apply UI rules

</td><td>

Buttons that should not be enabled, such as **Next**, are enabled.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1911445

</td><td>

The user is unable to log in to the GitHub mobile app and is repeatedly directed to the Platform UI

</td><td>

Android OS kills the app during the authentication/login process.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1901697

</td><td>

KB article pages in Cabrillo refresh constantly

</td><td>

When the user opens an article, the screen refreshes automatically, making it impossible for the user to read the article.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-blackberry-available-versions.md)

