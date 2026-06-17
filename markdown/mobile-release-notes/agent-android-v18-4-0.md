---
title: Mobile Agent for Android v18.4.0
description: The Android v18.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for Android v18.4.0

The Android v18.4.0 release provides fixes for the application.

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

 PRB1793478

</td><td>

A barcode scanner value is not correctly processed when the scanner is opened from CellsFragment

</td><td>

The data for a scanned barcode is replaced by the data for the next barcode scanned.

</td><td>

1.  Log in to the Agent app.
2.  Navigate to **Jump to Barcode** under the Rounds section.
3.  Scan barcode1.png.
4.  Select **Healthy/ Unhealthy** and submit \(if the **Healthy/Unhealthy** buttons are not visible, skip this step\).
5.  Tap **Jump to Next Barcode**.
6.  Scan barcode2.png.

 Expected behavior: The data for barcode 2 shows on the CellsFragment. Hitting the Back button shows the user the FormScreenFragment for barcode 1's data, and then hitting it again takes the user back to the ALP.

 Actual behavior: The data for barcode 2 shows on the CellsFragment, then is replaced by the data for barcode 1 after a few seconds \(when client refresh finishes\). Also, hitting the back button takes the user to the ALP instead of back to a previous FormScreenFragment.

</td></tr><tr><td>

Mobile Android

 PRB1806088

</td><td>

Special characters such as **&lt;** **&gt;** and **&amp;** do not render/escape properly in the Activity Stream

</td><td>

The characters render incorrectly in the output.

</td><td>

1.  Log in to Agent Mobile as a user assigned to a Work Order task \(or impersonate a user who is assigned to one\).
2.  Open a WOT record.
3.  Type **&lt;&gt;&amp;** into the Work Notes in the Activity Stream of the record.

 Notice that it renders as **&amp;lt;&amp;gt;&amp;amp;**.

</td></tr><tr><td>

Mobile Android

 PRB1814112

</td><td>

A pre-filled instance URL is not populated when the optional **Nickname** field is empty

</td><td>

On a mobile publishing Android build, the instance URL should be populated regardless of whether the **Nickname** field is empty or not.

</td><td>

1.  Submit a mobile publishing Android build.
2.  In the Login Management section, fill in the **Default app instance** field but leave the optional **Nickname** field empty.
3.  Once the build is ready, install and check the pre-filled instance.

 Expected behavior: The instance is populated because the instance URL was provided.

 Actual behavior: The instance is not populated.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

