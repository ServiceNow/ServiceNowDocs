---
title: Now Support for Android v17.5.0
description: The Android v17.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-05-09"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v17.5.0

The Android v17.5.0 release provides fixes for the application.

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

 PRB1751891

</td><td>

Clicking the **Accept** footer button multiple times causes a server error

</td><td>

When the user clicks the **Accept** or **Mark as complete** button, there is no indication to the user that the action was submitted. If the user clicks one of these buttons again, an 'Insufficient privileges' error displays because the button was already clicked.

</td><td>

1.  Navigate to Home.
2.  Under the section 'My Onboarding', click any open task.
3.  The user is redirected to the 'Active set' page.
4.  Click **Post-Offer**.
5.  Click any task.
6.  Click **Accept**.

 Observe the 'Insufficient privileges' error.

</td></tr><tr><td>

Mobile Android

 PRB1751431

</td><td>

The Agent Mobile App crashes when opening an applet

</td><td>

The app crashes when opening an applet using a button in a card template referring to Next Experience CSS variables if Next Experience UI is disabled

</td><td>

1.  Set the system property glide.ui.polaris.experience to false to disable the Next Experience UI.
2.  Log in to the Agent Mobile App.
3.  Navigate to **My work** &gt; **My tasks**. Tap to open a record.

 Expected behavior: The record should be opened successfully in the Agent Mobile App.

 Actual behavior: The record is opened but the Agent Mobile App crashes.

</td></tr><tr><td>

Mobile Android

 PRB1748251

</td><td>

The 'Uploading' dialog is not dismissed

</td><td>

 

</td><td>

1.  Open **My work** &gt; **My Tasks** and select a task.
2.  Navigate to the 'Maintenance Checklist' related list and open the maintenance record.
3.  Select Update.
4.  Attach a couple photos.
5.  Tap **Submit**.

 Observe that the number of 'Uploading files' is incorrect.

</td></tr><tr><td>

Mobile Android

 PRB1744211

</td><td>

A comma character is not accepted in a **Number** input field in an Agent Mobile instance with the language set to German

</td><td>

In German, a comma is used instead of a period as a decimal separator. However, a comma character is not accepted in a **Number** field.

</td><td>

1.  Provision an instance with the language set to German.
2.  Navigate to the Meine Arbeit tab.
3.  Select the first work order task.
4.  Click the three dots and select the last option.
5.  In the **Gearbeitete Zeit** field, try to enter a comma.

 Observe that a comma is not allowed in the field.

</td></tr><tr><td>

Mobile Android

 PRB1754838

</td><td>

Multiple barcode scans get appended instead of being processed separately using an external barcode scanner connected through bluetooth

</td><td>

 

</td><td>

1.  Use the Scan-To-Connect Utility App on Android device to pair the Zebra DS2278-SR via bluetooth.
2.  Tap the **Inventory** tab.
3.  Tap **Add asset multiscan**.

Note that the first field is not automatically focused on. The user has to tap it.

4.  Scan barcodes using Zebra DS2278-SR.

 Expected behavior: Multiple barcode scans should be processed separately. After one barcode is scanned, the app should automatically move to scan for the next value instead appending the next value to the first scan.

 Actual behavior: Multiple barcode scans get appended instead of being processed separately. This occurs for multiscan and groupscan.

</td></tr><tr><td>

Mobile Android

 PRB1761248

</td><td>

Offline related lists don't display multiple pages

</td><td>

Only the first 20 records in a related list are shown because multiple pages can't be loaded in offline mode.

</td><td>

1.  Provision a Vancouver instance.
2.  Create a related lists screen and mark it for offline.
3.  Ensure that the destination screen from the related list is marked for offline and has more than 20 records.
4.  Go offline.
5.  Open the related list while offline.

 Expected behavior: The user can scroll to view all records.

 Actual behavior: Only the first 20 records are returned and no additional pages are loaded.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../now-support-available-versions.md)

