---
title: Mobile Onboarding for Android v14.1.0
description: The Android v14.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-05-05"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v14.1.0

The Android v14.1.0 release provides fixes for the application.

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

 PRB1559270

</td><td>

Deep links to a list using UI parameters do not work as expected

</td><td>

A deep link to a list screen with a UI parameter shows an empty list.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1559308

</td><td>

The text cursor resets to the default position when typing quickly and selecting suggestions from the keyboard on Android devices

</td><td>

 

</td><td>

1.  Open the Agent application.
2.  Click **More** in the navigation tab and navigate to 'My work'.
3.  In 'My tasks', select any task.
4.  Click the three dots on top and select **Questionnaires**.
5.  Click **Inspection Questionnaire**.
6.  Complete the details.
7.  In the **Provide a reason for not providing cooling** field, start typing quickly and choose suggestions from keyboard.

 Expected behavior: The cursor should not move to the first position.

 Actual behavior: The cursor moves to the first position.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1568696

</td><td>

Performance degradation from CabrilloFragment.java

</td><td>

From the Cabrillo page, when the user tries to download files, they observer a spinner. For 'onComplete', the spinner is dismissed, but the 'onComplete' listener is called from the IO thread instead of the main thread. This causes a 'CalledFromWrongThreadException'.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

