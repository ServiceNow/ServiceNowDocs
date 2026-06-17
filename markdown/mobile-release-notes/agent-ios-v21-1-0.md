---
title: Mobile Agent for iOS v21.1.0
description: The iOS v21.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v21.1.0

The iOS v21.1.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

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

iOS Mobile

 PRB1989747

</td><td>

The activity stream is not sorted in descending order

</td><td>

This occurs after upgrading the Agent app.

</td><td>

1.  Open the Agent app on an iOS device.
2.  Open any case record with activity stream entries.

 Notice that entries are not properly sorted as per date.

</td></tr><tr><td>

iOS Mobile

 PRB1984480

</td><td>

Performing write-back actions on a work order task progressively reduces app performance

</td><td>

After closing multiple tasks consecutively in the same session, the iOS app begins to slow down and the app becomes unusable.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1993847

</td><td>

Category icons on Now Mobile do not load properly on iOS devices

</td><td>

Item icons appear differently than expected.

</td><td>

1.  Log in to a Now Mobile instance.
2.  Navigate to the 'Services' tab.
3.  Note the Item's icons.
4.  Manually refresh by swiping down from the top of the screen.

 Expected behavior: The icons should be the same between step 2 and step 3.

 Actual behavior: Icons are different between step 2 and step 3.

</td></tr><tr><td>

iOS Mobile

 PRB1992190

</td><td>

ItemViews don't respond to Dynamic Font Size

</td><td>

Some cards have increased font sizes while others don't respond to the font selection made by the user.

</td><td>

1.  Navigate to the Home Tab.
2.  Search the text 'Software' in the Search Bar in the Navigation Header.
3.  Change the device font size either from the System Settings or by using the Accessibility Inspector.

 Notice that some cards have increased font sizes while a lot of them don't respond to the font selection made by the user.

</td></tr><tr><td>

iOS Mobile

 PRB1979098

</td><td>

Highlight color does not appear around carousel card

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1968350

</td><td>

Remove welcome image from Instance screen

</td><td>

When a new app instance is added, a welcome image appears at the top when it should be removed.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1980354

</td><td>

On an iOS device, an 'else' condition is evaluated even when the 'if' condition is evaluated to true

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1980823

</td><td>

A field remains highlighted in the iOS app after dismissing a confirmation message

</td><td>

When the user opens a function instance in the iOS Agent app and dismisses the confirmation message, the field remains highlighted.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1984047

</td><td>

The carriage return suffix is not removed on barcode scans

</td><td>

Currently the app supports removing a tab suffix from a barcode scan, but does not support removing a carriage return suffix.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1968714

</td><td>

The 'Set to Ready' option is missing for IGT task in Guided Task screen

</td><td>

The 'Set to Ready' option should be available in the three dots menu when the task is in an 'On Hold' state. Instead of the 'Set to Ready' option, the menu still shows 'Put on Hold'.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1976062

</td><td>

Issue opening a record address from a URL link in Apple Maps

</td><td>

The user observes a 'No matching places found' error on the Apple Maps app.

</td><td>

1.  Navigate to a Work Order Task.
2.  Using the top right ellipsis menu, tap **Open map**.

 Observe a 'No matching places found' error on the Apple Maps app.

</td></tr><tr><td>

iOS Mobile

 PRB1978843

</td><td>

Barcode input text of type 'Accessibility' isn't visible when text is large

</td><td>

If the user enables large text in the iOS accessibility settings and enters text in the barcode input, the text is not completely visible if the 'label' contains a large amount of text that forces it to a new line.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

