---
title: Now Mobile for iOS v20.0.0
description: The iOS v20.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v20-0-0.html
release: mobile
topic_type: reference
last_updated: "2025-06-05"
reading_time_minutes: 4
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v20.0.0

The iOS v20.0.0 release provides fixes for the application.

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

Mobile iOS

 PRB1850147

</td><td>

The application theme changes after closing and reopening the app

</td><td>

The theme goes back to normal after pulling to refresh.

</td><td>

1.  Open mobile \(requester\) app and log in to an instance.
2.  Terminate the app.
3.  Open the app again.

 Expected behavior: The theme is the same as before.

 Actual behavior: Theme is changed.

</td></tr><tr><td>

Mobile iOS

 PRB1886478

</td><td>

Certain colors are not rendered by iOS

</td><td>

The DefaultColors are constructed directly from the class VisualizationColorService.java, which has a null hexValue. iOS's code expects the key 'hexValue' to be present in 'DefaultColors'.

</td><td>

1.  Log in to an instance.
2.  Tap the My team bar and scroll to the section 'My team dashboard'.

 Notice that content is not displayed properly.

</td></tr><tr><td>

Mobile iOS

 PRB1843346

</td><td>

Special characters are not displayed in file names

</td><td>

Special characters such as @ are not displayed in file names.

</td><td>

1.  Open the Now Mobile app in a base instance.
2.  Navigate to the Home tab.
3.  Under My Items, select My tasks.
4.  Open a record.
5.  Navigate to Updates.

 Notice that any attachment names with special characters do not display the special characters.

</td></tr><tr><td>

Mobile iOS

 PRB1888240

</td><td>

Problem with updating barcode input forms with multiple inputs

</td><td>

Barcode inputs that are not the first in an input form page behave incorrectly. After scanning a new value, the barcode input screen is updated with the first input in the form page.

</td><td>

1.  Open an input form where the barcode input is not the first field on the page \(or one with multiple barcode inputs\).
2.  Select any barcode input that is not the first one on the screen.
3.  Perform a scan.

 Expected behavior: In the case of a multi scan input, the scanned value should be added to the Review tab. In the case of a single scan input, the scanned value should be added to the scan input field.

 Actual behavior: The barcode view is updated to display the first input on the input form screen page. This can result in either the barcode input view going blank or showing the information for the wrong barcode input.

</td></tr><tr><td>

Mobile iOS

 PRB1868935

</td><td>

The user can only view a small subset of list options in a Virtual Agent chat

</td><td>

When the pagination break is less than 10, infinite scrolling doesn't work.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1868544

</td><td>

Data visualization sources fail to decode JSON that does not contain a label

</td><td>

DAVisualization.VisualizationProperties.DataSource expects to receive labeled JSON, so when JSON is received without a label, decoding fails and an error appears reading, 'Content couldn't be displayed'.

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

 PRB1863014

</td><td>

Input form screen survey shows incorrect choices when scrolling on device running iOS 18

</td><td>

After scrolling down the list of questions, the selected value of a choice at the top of the page is lost and the choice values are changed.

</td><td>

Pre-requisites: iPhone must be running iOS 18+.

 1.  Use a small phone or an instance with an input form screen that is very large.
2.  Open a survey that uses an input form screen with multiple single select choice cells.

Note the options in the first few cells.

3.  Scroll to the bottom of the form.
4.  Scroll back to the top of the form.

 Notice that one or more of the first few cells changes to match the options of a lower cell.

</td></tr><tr><td>

Mobile iOS

 PRB1861461

</td><td>

The app gets stuck on blank screen when the user opens a push notification with redirection

</td><td>

The app should open to the destination screen.

</td><td>

1.  Set glide.sg.blur\_ui\_when\_backgrounded = true.
2.  Launch the app and put it in the app switcher.
3.  Send a push notification with redirection.
4.  Tap the notification.

 Expected behavior: The app opens on the destination screen.

 Actual behavior: The app opens and the destination screen appears for a moment, but then it disappears and the app gets stuck on a blank screen.

</td></tr><tr><td>

Mobile iOS

 PRB1879703

</td><td>

Deep links from QR code don't work when the blur app option is enabled and UX analytics is disabled

</td><td>

For instances with the 'blur app' option enabled and UX analytics disabled, scanning deep links from QR codes doesn't work properly.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1884278

</td><td>

The wrong URL is loaded into the URL screen when switching between clone instances

</td><td>

When the first tab contains a URL browser screen, the URL from one instance is still used when switching to the other instance.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1866315

</td><td>

A 'Date' type input sends an incorrect time on iOS

</td><td>

When using 'Date' input type, the current time is sent on a request from a parameter screen. The correct time should always be midnight.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

