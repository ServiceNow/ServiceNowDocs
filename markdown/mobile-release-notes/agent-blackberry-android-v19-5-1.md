---
title: Mobile Agent - BlackBerry for Android v19.5.1
description: The Android v19.5.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-blackberry-android-v19-5-1.html
release: mobile
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 1
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for Android v19.5.1

The Android v19.5.1 release provides fixes for the application.

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

Mobile Android

 PRB1884005

</td><td>

Users can share attachments even after attachment sharing has been disabled by the system property 'glide.sg.block\_mobile\_attachments\_sharing'

</td><td>

When 'glide.sg.block\_mobile\_attachments\_sharing' is true, the app should prevent files from being downloaded or saved by third party apps. However, the user is able to open unsupported file-types in third party apps even when this property is true, and therefore can download and share the attachments.

</td><td>

1.  Set 'glide.sg.block\_mobile\_attachments\_sharing' to true.
2.  Navigate to a list or form that contains an attachment for an unsupported file type, such as a PDF.
3.  Select the attachment.

 Expected behavior: The app blocks the third party app from opening unsupported file type.

 Actual behavior: If a third party app is installed it is able to open the file type, and users are then able to save it to their device.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-blackberry-available-versions.md)

