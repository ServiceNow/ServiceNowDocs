---
title: Mobile Agent - Intune for Android v20.6.0
description: The Android v20.6.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-intune-android-v20-6-0.html
release: mobile
topic_type: reference
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for Android v20.6.0

The Android v20.6.0 release provides fixes for the application.

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

 PRB1952335

</td><td>

Attachments uploaded in offline mode are not visible once back online

</td><td>

Attachments uploaded in offline mode are not visible once back online.

</td><td>

1.  Make sure the offline functionality is enabled on the instance.
2.  Navigate to **Offline mode**.
3.  Open a record with activity.
4.  Attach an image via Camera.
5.  Set the app to 'Online'.

 Observe that the attached images are not visible.

</td></tr><tr><td>

Android Mobile

 PRB1956837

</td><td>

Input form multi-choice screen pickers act erratically when scrolling

</td><td>

Items are deselected.

</td><td>

1.  On **My Work**, open the quick action **Open Test Multi Select**.
2.  Select **See All**.
3.  Select the first few, scroll down to the bottom, and scroll back up again.

 Expected behavior: Selected items should not get un- or re-selected when scrolling.

 Actual behavior: First item\(s\) deselected.

</td></tr><tr><td>

Android Mobile

 PRB1956877

</td><td>

A record created offline isn't updated immediately when opened directly from an item section

</td><td>

Items are not visible in the activity stream.

</td><td>

1.  Navigate to **Offline mode** &gt; **Create a record** with activity stream, such as an incidental that will appear in the related item section of a record.
2.  Tap to open the record directly rather than through the **See All** redirection.
3.  Add a comment or attachment to the activity stream.

 Expected behavior: The item should be visible in the activity stream after adding it.

 Actual behavior: The item is not visible in the activity stream, and the user must navigate out and back in to see it.

</td></tr><tr><td>

Android Mobile

 PRB1956146

</td><td>

Add offline declarative support for adding attachment inputs to activity streams

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1954422

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1952072

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1952846

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-intune-available-versions.md)

