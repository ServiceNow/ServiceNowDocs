---
title: Mobile Onboarding for iOS v13.4.0
description: The iOS v13.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-02-03"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v13.4.0

The iOS v13.4.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS \(non-classic\)

 PRB1549808

</td><td>

The attachment modal swipe dismiss does not re-enable the **Attachment** button

</td><td>

As a result, users are unable to upload using the attachment variable.

</td><td>

1.  From the 'For Me' tab, scroll down and start the 'Report Vaccination' flow.
2.  Select any vaccination status to enable the next stage of the form.
3.  Press the **Upload** button and select **Open Library** to launch the gallery.
4.  Press **Cancel** in the modal to dismiss.

Observe that **Upload** can be pressed again.

5.  Select **Open Library** again, but swipe from the top of the modal to dismiss the gallery.

 Observe that **Upload** no longer responds to taps.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1544154

</td><td>

A negative value in the decimal type of a field does not populate the report in the Now Mobile app

</td><td>

 

</td><td>

1.  Log in to any Rome instance.
2.  Navigate to any table \(for example, incident\) and create a decimal type of field.
3.  Create any record with a negative value in the decimal field and another record with a positive value.
4.  Create a report that shows the positive value and another report with a negative value.
5.  Create an applet and attach the report to it.
6.  Attach the applet to an applet launcher.
7.  Log in to the instance from the Now Mobile app.
8.  Navigate to the home, test the report, and check that the report doesn't show any value.
9.  Navigate to the home, test the report with the positive value, and check that the report shows the data correctly.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1547267

</td><td>

iOS Now Mobile app artifact element exposed to VoiceOver

</td><td>

There is a 'What application is down/unavailable undefined' element that is exposed to VoiceOver. Exposure of elements that are covered, hidden, a duplicate, or otherwise should not be visible to the user causes confusion for users attempting to navigate the UI of the application and may cause input and control errors.

</td><td>

1.  Log in to the instance on the Now Mobile app.
2.  Using VoiceOver, perform the following navigations.
3.  Select the 'Services navigation' tab.
4.  Scroll down to 'Browse services'.
5.  Select the **Can we help you?** item.
6.  Open the 'Report outage' item.
7.  Navigate to the **What application is down...** field and open it.
8.  Let VoiceOver describe the available choices.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

