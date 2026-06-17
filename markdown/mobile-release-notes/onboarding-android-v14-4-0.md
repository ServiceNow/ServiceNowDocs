---
title: Mobile Onboarding for Android v14.4.0
description: The Android v14.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-08-04"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v14.4.0

The Android v14.4.0 release provides fixes for the application.

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

 PRB1577594

</td><td>

A form applet with a data item shows a blank screen when there are no results

</td><td>

A parameterized form applet shows a blank screen when there is no data. The issue is only on Android, and works as expected on iOS devices.

</td><td>

1.  Log in to any San Diego base instance.
2.  Configure a data item to accept a parameter and filter the data based on the parameter.
3.  Create a form screen and configure an input parameter and complete the necessary parameter mapping to the data item.
4.  Connect the screen to any applet launcher on Now Mobile app.
5.  Open the Now Mobile app and select the screen created in step 3.
6.  Scan a bar code that represents a valid record.

 The scan works as expected and the form loads with details. When scanning an invalid bar code, the Android app shows a blank screen. However, on an iOS device, the user observes a message saying 'no data found'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1576622

</td><td>

Selecting a category clears the subcategory on the incident creation page

</td><td>

 

</td><td>

1.  Navigate to **More** &gt; **Old Param Test** &gt; **Incident** &gt; **Top menu** &gt; **New**.
2.  Select **Category** &gt; **Software**.
3.  Select **Sub Category** &gt; **Email**.

The **Sub Category** field is dependent on the **Category** field.

4.  Change **Category** to 'Inquiry / Help'.

 Expected behavior: **Sub Category** should not be cleared because 'Inquiry / Help' also contains a value for **Email Sub Category**.

 Actual behavior: **Sub Category** is cleared.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1576741

 [KB1122108](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1122108)

</td><td>

UI rules are not applied on the form screen of the mobile global result

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

