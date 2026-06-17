---
title: Mobile Agent for iOS v19.4.0
description: The iOS v19.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-04-03"
reading_time_minutes: 2
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v19.4.0

The iOS v19.4.0 release provides fixes for the application.

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

 PRB1863121

</td><td>

A push notification with universal links doesn't open the destination screen

</td><td>

When a push notification with an internal link is selected, the screen is not opened.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1858857

</td><td>

Placeholder text is not visible on an IT Asset Management asset

</td><td>

The **Scheduled Retirement** field on an IT Asset Management asset does not contain placeholder text.

</td><td>

1.  Log in to Agent Mobile.
2.  Navigate to the Asset tab.
3.  Navigate to **IT Asset Management** &gt; **Create Asset**.
4.  Select **Submit** \(no details are needed at this stage\).
5.  Select the three dots in the upper right corner and select **Create Asset**.

 Observe that the **Scheduled Retirement** field does not contain placeholder text.

</td></tr><tr><td>

Mobile iOS

 PRB1855289

</td><td>

The user cannot end an impersonation if the username of the logged in user and the impersonated user contain a '\\' character

</td><td>

The user observes an error message reading 'Unable to end impersonation' when attempting to end an impersonation.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1843346

</td><td>

The Mobile App doesn't display special characters in file names

</td><td>

Special characters, such as @, are not displayed in file names.

</td><td>

1.  Open the Now Mobile app in a base instance.
2.  Navigate to the Home tab.
3.  Under **My items**, select **My tasks**.
4.  Open a record.
5.  Navigate to **Updates**.

 Notice that any attachment names with special characters do not display the special characters.

</td></tr><tr><td>

Mobile iOS

 PRB1860053

</td><td>

UPC-A \(12 digits\) barcode scans are not supported

</td><td>

iOS doesn't support UPC-A codes \(12 digits\) explicitly even though they are considered a subset of EAN-13 \(13 digit\) with a leading zero in the stringValue.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1863014

</td><td>

Input form screen survey shows incorrect choices when scrolling on device running iOS 18

</td><td>

After scrolling down the list of questions, the selected value of a choice at the top of the page is lost and the choice values are changed.

</td><td>

Pre-requisites: iPhone must be running iOS 18+. Use a small phone or an instance with an input form screen that is very large.

 1.  Open a survey that uses an input form screen with multiple single select choice cells. Note the options in the first few cells.
2.  Scroll to the bottom of the form.
3.  Scroll back to the top of the form.

 Notice that one or more of the first few cells has changed to match the options of a lower cell.

</td></tr><tr><td>

Mobile iOS

 PRB1868544

</td><td>

Data visualization sources fail to decode JSON that does not contain a label

</td><td>

DAVisualization.VisualizationProperties.DataSource, expects to receive labeled JSON, so when JSON is received without a label, decoding fails and an error appears reading, 'Content couldn't be displayed'.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

