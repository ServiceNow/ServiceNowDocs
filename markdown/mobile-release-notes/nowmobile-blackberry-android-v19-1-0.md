---
title: Now Mobile for BlackBerry for Android v19.1.0
description: The Android v19.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-blackberry-android-v19-1-0.html
release: mobile
topic_type: reference
last_updated: "2025-01-02"
reading_time_minutes: 2
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for Android v19.1.0

The Android v19.1.0 release provides fixes for the application.

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
4.  Select **Healthy/ Unhealthy** and submit \(if **Healthy/Unhealthy** buttons are not visible, skip this step\).
5.  Select **Jump to Next Barcode**.
6.  Scan barcode2.png.

 Expected behavior: The data for barcode 2 shows on the CellsFragment. Selecting the **Back** button shows the user the FormScreenFragment for barcode 1's data. Selecting **Back** again takes the user back to the ALP.

 Actual behavior: The data for barcode 2 shows on the CellsFragment, then is replaced by the data for barcode 1 after a few seconds \(when the client refresh finishes\). Also, selecting the **Back** button takes the user to the ALP instead of back to a previous FormScreenFragment.

</td></tr><tr><td>

Mobile Android

 PRB1822056

</td><td>

A page reload script doesn't work properly

</td><td>

A script that reloads a webpage when the user switches between tabs does not work on Android.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1827801

</td><td>

The word 'Deutsch' is mispelled under the instance language settings

</td><td>

'Deutsch' is misspelled as 'Deutch' when the device language is set to German.

</td><td>

1.  Set the language setting on an Android device to 'German'.
2.  Open the Now Mobile app.
3.  Navigate to **Settings** &gt; **Preferences** &gt; **Language**.

 Notice that the language is displayed as 'Deutch' when it should be spelled 'Deutsch'.

</td></tr><tr><td>

Mobile Android

 PRB1797131

</td><td>

Now Mobile shows 'No data available' when the user opens a bookmarked employee profile

</td><td>

 

</td><td>

1.  Log in to any Washington DC base instance on a desktop.
2.  Enable employee profile.
3.  Add a 'Saved' applet to Now Mobile navigation.
4.  Log in to the Now Mobile app on a mobile device.
5.  Search for any employee profile \(for example, system administrator\).
6.  Select the **Save** icon in the employee profile.
7.  Navigate to the saved applet.
8.  Try to open the employee profile that was saved.

 Expected behavior: The saved profile is shown.

 Actual behavior: 'No data available' is shown.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-blackberry-available-versions.md)

