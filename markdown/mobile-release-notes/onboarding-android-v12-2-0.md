---
title: Mobile Onboarding for Android v12.2.0
description: The Android v12.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-06-17"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v12.2.0

The Android v12.2.0 release provides fixes for the application.

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

 PRB1491805

</td><td>

Users receive push notifications for the impersonated user

</td><td>

This issue occurs even after ending the impersonation and closing the app.

</td><td>

1.  Log in to an instance as an admin user.
2.  Make sure that the user has push notification enabled.
3.  Log in to an Android device as admin.
4.  Check the sys\_push\_notif\_app\_install table.

One active record with the following values is inserted:

    -   User: System Administrator
    -   Push App: ServiceNow Mobile Application
    -   Push Platform: Google
5.  On the mobile device, impersonate Abel Tuter.
6.  Check the sys\_push\_notif\_app\_install table.

The admin's record is deactivated and another active record with the following values is inserted:

    -   User: Abel Tuter
    -   Push App: ServiceNow Mobile Application
    -   Push Platform: Google
7.  End the impersonation.

 Expected behavior: After the impersonation ends, the admin record should be reactivated and Abel's record should be deactivated.

 Actual behavior: There are two active records in the sys\_push\_notif\_app\_install table for admin and Abel. As a result, the admin receives notifications sent to Abel.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1482314

</td><td>

The **Next** and **Submit** buttons are disabled, even when the user uploads an attachment to the mandatory attachment question type

</td><td>

 

</td><td>

1.  In the Now Mobile app for Android, log in as admin.
2.  Navigate to **My Tasks** &gt; **Mandatory Attachment Question Issue**.
3.  Click the **Short description** field.

It loads the survey.

4.  Navigate to the question 'New attachment' and upload the attachment.

 Even though you added the attachment, the **Submit** and **Next** buttons are disabled.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

