---
title: Mobile Agent - BlackBerry for iOS v20.1.0
description: The iOS v20.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-07-10"
reading_time_minutes: 3
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for iOS v20.1.0

The iOS v20.1.0 release provides fixes for the application.

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

 PRB1887761

</td><td>

File attachments using a Unicode filename show a percentage encoded

</td><td>

A filename containing Unicode characters is sent as a percentage encoded by the instance. As such, for presentation purposes, the filename should have the percentage encoding removed / decoded. This is caused by FileAttachmentView's using the FileMetaData.filename in the UI.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1897716

</td><td>

The user is unable to upload a catalog item with a 'Variable' type attachment

</td><td>

The user can't upload 'Attachment' type variables. The variable must map to a field of sys\_dictionary type 'Image'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1903899

</td><td>

Data visualization is broken on iOS

</td><td>

Dashboards do not work on iOS devices.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1898263

</td><td>

WebView reloads when the app goes from background to foreground even if the session is not expired

</td><td>

This issue occurs with a client on version 20.x and an instance earlier than Zurich.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1881945

</td><td>

A deep link URL is loaded on an external browser instead of inside the Mobile App

</td><td>

When a deep link is opened from inside the chat, the link should load inside the app. However, an external browser opens and loads the URL.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1900982

</td><td>

Quick Links in the iOS Now Mobile App do not open properly

</td><td>

Quick Links function properly in the desktop version, but in the mobile version, selecting a link results in an 'Invalid URL' error.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1890821

</td><td>

Actionable notifications do not function properly on iOS

</td><td>

On iOS, actionable notifications do not function properly. If the user is logged into multiple instances in the app and an actionable notification is triggered from a development instance, the actions do not appear.

</td><td>

1.  Trigger an actionable push notification from a development instance.
2.  Have multiple instances opened in the app.

Notice that there is no push notification generated for the app in iOS devices.

3.  Remove other instances and keep the development instance logged in within the app.
4.  Trigger the actionable push notification from the development instance.

 Expected behavior: A push notification is seen when triggered, irrespective of single/multiple instances logged in.

 Actual behavior: There is no push notification action generated for the app in iOS devices.

</td></tr><tr><td>

Mobile iOS

 PRB1891026

</td><td>

Mobile UX analytics data collection fails due to a change in the certification authority

</td><td>

UX analytics data for mobile applications is not collected due to an unsupported certificate installed on the analytics API.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1891192

</td><td>

A seat number label is missing from an indoor map

</td><td>

A space name is not displayed when using 'Get directions' after making a reservation on iOS mobile

</td><td>

1.  Select Make a **Reservation** &gt; **See All**.
2.  Select **Desk** &gt; **Browse All**.
3.  Fill all details.
4.  Choose a Floor and uncheck **All day**, then select **Next** &gt; **Location** &gt; **Submit**.
5.  Select **Get Directions** on the created record.

 Expected behavior: The floor is opened and the seat number \(for example, 411B is displayed on the map\).

 Actual behavior: The text 411B is not displayed on the map.

</td></tr><tr><td>

Mobile iOS

 PRB1860594

</td><td>

UI rules are lost on a record form upon refresh

</td><td>

When a record is refreshed, the app looks for the record's parent which is the embedded form. The embedded form's ID cannot be used to reference the correct record in the cache because it is contained in the cached list screen.

</td><td>

1.  Create a list screen of embedded forms for the instance.
2.  Create a UI Rule that hides a certain element in the header of the record to be refreshed later.
3.  Navigate to one of the records.

Observe that the UI element is hidden \(The UI rule is observed\).

4.  Refresh the record.

 Observe that the previously hidden UI element is now visible.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](../agent-blackberry-available-versions.md)

