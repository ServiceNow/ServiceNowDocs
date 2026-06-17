---
title: Now Mobile for Android v19.4.0
description: The Android v19.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-android-v19-4-0.html
release: mobile
topic_type: reference
last_updated: "2025-04-03"
reading_time_minutes: 2
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for Android v19.4.0

The Android v19.4.0 release provides fixes for the application.

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

 PRB1864255

</td><td>

The notification category list appears blank

</td><td>

A default theme with a white text color is applied, which appears blank against a white background.

</td><td>

Navigate to **More** &gt; **Settings** &gt; **Preferences** &gt; **Notifications**.

 Observe that notification categories titles are blank.

</td></tr><tr><td>

Mobile Android

 PRB1862459

</td><td>

The app crashes while uploading larger images

</td><td>

High megapixel images \(50MB\) uploaded as attachments cause the app to crash.

</td><td>

1.  Log in into Now Mobile.
2.  On the home page, select **Request IT assistance** under 'Quick links'.
3.  Select **Add attachments**.

The camera opens.

4.  Change image resolution to 50MB and capture the image.
5.  Select **OK**.

 Observe that the app crashes.

</td></tr><tr><td>

Mobile Android

 PRB1853593

</td><td>

alm\_hardware records are not successfully created when using the Create Asset or Retire Asset buttons in Now Agent

</td><td>

The serial number entered is not submitted to the back-end. Therefore, the record is not successfully created.

</td><td>

1.  Select the **Create Asset** icon under the Asset tab.
2.  Fill the form and proceed to the bar code scanning page.
3.  Enter a random serial number and **Submit**.

 Observe that the record is not created and a success message is not displayed.

</td></tr><tr><td>

Mobile Android

 PRB1868822

</td><td>

CabrilloBackPressHandler.flowEnded\(\) can inadvertently back the user out of the entire application

</td><td>

When a catalog item is submitted and the **Close** button is selected, the app crashes and sends the user back to the Android home screen.

</td><td>

1.  Log in to the Agent app.
2.  Select the Home-web tab.
3.  Select the Marketing channel and select **Raise Request**.
4.  Select the catalog items \(for example, "MySales \(SFDC\) functional..."\) and follow the screen instructions to submit the catalog item.
5.  Select the **Close** button.

 Expected behavior: The catalog item page is closed and sends the user back to the previous screen.

 Actual behavior: The app is closed/crashed and sends the user back to the Android home screen.

</td></tr><tr><td>

Mobile Android

 PRB1865339

</td><td>

Default list and form screens open instead of URLs with base instance configuration

</td><td>

A fix for URL transformation inadvertently brings in default list and form screen builders when a URL matches a well-known platform list or record URL.

</td><td>

1.  Add a link to a standard form or list URL such as incident\_list or incident.do?sys\_id=\{sys\_id\} using a link URL function.
2.  Open the link in the app.

 Expected behavior: The URL opens in an internal web browser.

 Actual behavior: A default native list or form screen is opened.

</td></tr><tr><td>

Mobile Android

 PRB1866637

</td><td>

A custom map's single input doesn't display in full-screen mode

</td><td>

When a custom map input is a single visible input, an input form screen should always display in full-screen mode.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

