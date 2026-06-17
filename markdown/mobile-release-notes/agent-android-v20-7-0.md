---
title: Mobile Agent for Android v20.7.0
description: The Android v20.7.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-01-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for Android v20.7.0

The Android v20.7.0 release provides fixes for the application.

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

 PRB1970897

</td><td>

The **Submit** button is not disabled when mandatory fields are not filled

</td><td>

The **Submit** button should be disabled when the mandatory fields are not filled in.

</td><td>

1.  Log in to Agent.
2.  Navigate to **My Work**.
3.  Open the incident.
4.  Select **Reassign** from the Top menu function.
5.  Clear the value of the Assignment group.

 Observe 'Assigned to' is not cleared and the user can submit the record.

</td></tr><tr><td>

Android Mobile

 PRB1943779

</td><td>

Images cannot be downloaded or saved from a Service Portal web page

</td><td>

Images can't be downloaded/saved on the Now Mobile / Agent app.

</td><td>

1.  Create a new mobile screen of type 'Mobile web'. Use any portal URL \(for example '/sp'\).
2.  On either the Mobile Agent or Now Mobile app configuration, create a new 'Navigation' tab configuration and associate the screen created in step 1.
3.  Open the mobile app on an Android Device.
4.  Attempt to save any image from the portal to the device.

 Notice that the images cannot be saved on an android device.

</td></tr><tr><td>

Android Mobile

 PRB1967470

</td><td>

On Android, a fixed color is set by the field label instead of the field ID due to the wrong color being loaded

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1968835

</td><td>

Improve image upload performance using new ImageMaxDimensionPreset property to scale images

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1909510

</td><td>

Issues with Talk Back announcement and highlighting elements on a carrousel

</td><td>

The screen reader announces a slide's data but does not specify that it is a button. Also, once the user reaches the carousal, they are unable to navigate back to previous content.

</td><td>

1.  In the mobile app, navigate to More &gt; Campaigns regression.
2.  Start swiping and hear the announcement of the carrousel elements.

 Notice that the screen reader fails to specify that content is labeled as a button. Also, notice that the user is unable to navigate back to previous content on a carousel.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

