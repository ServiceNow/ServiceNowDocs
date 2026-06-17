---
title: Now Mobile for Android v21.1.0
description: The Android v21.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for Android v21.1.0

The Android v21.1.0 release provides fixes for the application.

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

 PRB1988016

</td><td>

App crashes when the assignment property type is null

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1977070

</td><td>

The Portal page keeps reloading in the Now mobile app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1975175

</td><td>

Barcode scan camera/externalscan toggle state is reset if the app is force-closed or the userClient is refreshed

</td><td>

 

</td><td>

1.  Set up mobile property on instance externalScanEnabled = true.
2.  In the app, tap **Inventory** then **+** then **Single** or **Group** or **Multi-scan**.
3.  Toggle **Use camera** to on.
4.  Select **Back** and navigate back into the single scan.

Observe that the state of the toggle is preserved.

5.  Select **Back** to navigate to the home tab and pull to refresh.
6.  Navigate back to single scan.

 Expected behavior: The toggle state should have retained and been on.

 Actual behavior: The toggle state is reset.

</td></tr><tr><td>

Android Mobile

 PRB1981160

</td><td>

True/false text is shown incorrectly when Japanese translation is enabled

</td><td>

Text displays incorrectly as 1 or 0 instead of 'True' or 'False'

</td><td>

1.  On the Agent app, Navigate to **More** &gt; **Settings** &gt; **Preferences** &gt; **Language**.
2.  Set Preferred language to Japanese.
3.  Navigate to 'My work', open a WOT detail screen and look for the boolean field.

 Expected behavior: True or False text.

 Actual behavior: The text displays as 1 or 0.

</td></tr><tr><td>

Android Mobile

 PRB1979888

</td><td>

Tabs don't load properly on a Utah instance

</td><td>

Only default tabs load when all configured tabs should load.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](../now-mobile-available-versions.md)

