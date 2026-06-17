---
title: Now Mobile - Intune for iOS v17.6.0
description: The iOS v17.6.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-06-06"
reading_time_minutes: 1
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v17.6.0

The iOS v17.6.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_uw1_y14_31c" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS

 PRB1759561

</td><td>

Analytics UserID is only set to service initialization and is not updated if the user information changes

</td><td>

The setUserId call is called once following the initialization of the analytics service and is not called again.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1740552

</td><td>

A UI Rule is not applied consistently on the 'Details' screen after updating from an input form

</td><td>

When the user edits a record by adding a note, the red background of the note text disappears. This only occurs the second time the user edits a record and navigates back to the home screen.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](../nowmobile-intune-available-versions.md)

