---
title: Now Mobile for Android v17.6.0
description: The Android v17.6.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-android-v17-6-0.html
release: mobile
topic_type: reference
last_updated: "2024-06-06"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for Android v17.6.0

The Android v17.6.0 release provides fixes for the application.

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

 PRB1749164

</td><td>

The **Cost** field on the Log Incidental Input form screen has discrepancies in certain values between iOS and Android

</td><td>

This discrepancy only occurs during the creation process of logging an incidental. Once the user submits, the same value is displayed on both iOS and Android clients.

</td><td>

1.  Provision a Vancouver instance.
2.  Select **More** &gt; **Field Service**.
3.  Open any active wm\_task record from All tasks.
4.  Select the top menu function and select **Log incidental**.
5.  Create one incidental Record.
    1.  Type: Mileage
    2.  Cost per mile: 0.34
    3.  Quantity: 10
6.  Look at the **Cost** field.

 In iOS, the user observes the value 3.4 in the **Cost** field. In Android, the user observes the value 3.4000000000000004.

</td></tr><tr><td>

Mobile Android

 PRB1759490

</td><td>

The Activity Stream crashes if a comment contains HTML with an IMG tag that doesn't have a source link

</td><td>

A malformed image tag passes an unexpected null URL parameter to the code. This results in a crash.

</td><td>

1.  Log in to the Agent mobile app.
2.  Search for a case record and open it.
3.  Navigate to the tab **Activity Stream**.
4.  Scroll to the bottom.

 Observe that the app crashes and closes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

